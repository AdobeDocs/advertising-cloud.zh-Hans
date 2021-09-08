---
title: ' [!DNL Analytics for Advertising Cloud]的JavaScript代码'
description: ' [!DNL Analytics for Advertising Cloud]的JavaScript代码'
feature: Integration with Adobe Analytics
exl-id: 184508ce-df8d-4fa0-b22b-ca0546a61d58
source-git-commit: 56ac178bf10d8c934297521ca3075783e1bc2c36
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 0%

---

# [!DNL Analytics for Advertising Cloud]的JavaScript代码

*仅具有Advertising Cloud-Adobe Analytics集成的广告商*

*仅使用Advertising Cloud DSP的广告商*

对于Advertising Cloud DSP,[!DNL Analytics for Advertising Cloud]集成会跟踪点进和点进网站的交互。 点进访问量由您网页上的标准Adobe Analytics代码进行跟踪；[!DNL Analytics]代码可捕获登陆页面URL中的AMO ID和EF ID参数，并在各自保留的eVar中跟踪它们。 您可以通过在网页中部署两行JavaScript代码来跟踪显示到达访问。

在访问网站的首次页面查看时，Advertising Cloud JavaScript代码会检查访客之前是否查看过或点击过广告。 如果用户之前通过点进方式进入网站，或者未看到广告，则访客将被忽略。 如果访客在Advertising Cloud中设置的[点击回顾窗口](/help/integrations/analytics/prerequisites.md#lookback-a4adc)期间看到广告，但未通过点进方式进入网站，则Advertising Cloud JavaScript代码会使用[Experience CloudID服务](https://experienceleague.adobe.com/docs/id-service/using/home.html)生成补充ID(`SDID`)，用于将来自Advertising Cloud的数据拼合到访客的Adobe Analytics点击中。 然后，Adobe Analytics会查询Advertising Cloud中与广告曝光关联的AMO ID和EF ID。 然后，AMO ID和EF ID会填充到其各自的eVar中。 这些值会在指定的时间段（默认为60天）内保留。

[!DNL Analytics] 每小时向Advertising Cloud发送网站流量量度（如页面查看次数、访问次数和逗留时间）以 [!DNL Analytics]  及任何自定义事件或标准事件，并使用EF ID作为键。然后，这些[!DNL Analytics]量度会通过Advertising Cloud归因系统来将转化与点击和曝光历史记录关联起来。

>[!NOTE]
>
>Advertising Cloud JavaScript跟踪逻辑发生在Adobe端，因此几乎不会影响页面加载时间。
>
>相反，客户端会出现[!DNL DCM]数据连接器到[!DNL Analytics]（使用[!DNL Google Campaign Manager 360]）的Advertising Cloud DSP逻辑。 客户端拼合会减缓页面加载速度，并增加数据丢失的风险。 之所以出现这种情况，是因为[!DNL Analytics] JavaScript必须ping [!DNL DoubleClick]并等待[!DNL DoubleClick]将上次点击/展示数据传回[!DNL Analytics]。 当您的[!DNL DSP]团队设置[!DNL DCM]数据连接器时，必须指定您愿意延迟页面的时长。

## 部署JavaScript代码

JavaScript库包含两行，它们允许[!DNL Analytics]和Advertising Cloud相互通信。 如果[!DNL Analytics for Advertising Cloud]集成在Advertising Cloud实施期间完成，则您应该已经收到此代码，其中包含有关如何部署该代码的说明。

如果您还没有代码，请联系Advertising Cloud支持团队。

### 代码放置位置

[!DNL Analytics for Advertising Cloud] JavaScript函数必须位于Experience CloudID服务之后，但位于您的Analytics App Measurement代码之前，以便将补充ID(`SDID`)包含在您的Analytics调用中。

![代码放置](/help/integrations/assets/a4adc-code-placement.png)

### 验证代码部署

您可以使用任何数据包探查器类型的工具（如[!DNL Charles]、[!DNL Fiddler]或[!DNL Chrome Developer Tools]）通过比较发往Advertising Cloud的请求与发往[!DNL Analytics]的请求之间的四个ID的值来执行验证，如下所述。

#### 如何使用[!DNL Chrome Developer Tools]确认代码 {#validate-js-chrome}

1. 打开[!DNL Chrome Developer Tools]并单击&#x200B;**Network**&#x200B;选项卡。
1. 加载包含[!DNL Analytics for Advertising Cloud] JavaScript的网站页面。
1. 按`last`筛选[!UICONTROL Network]选项卡，并查看两行：

   ![最后过滤](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * 第一行是对JavaScript库的调用，其标题为`last-event-tag-latest.min.js`。
   * 第二行是向Advertising Cloud发送请求的调用。 开始如下：`_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

      如果您没有看到对Advertising Cloud的调用，则它可能不是您访问的第一个页面查看。 出于测试目的，您可以删除Cookie，以便下次调用将是相应访问的第一个页面查看：

      1. 在“应用程序”选项卡上，找到`adcloud` Cookie，并验证该Cookie是否包含值为`y`的`_les_v`（上次访问）和30分钟后过期的UTC纪元时间戳。
      1. 删除`ad cloud` Cookie并刷新页面。
1. 在`/b/ss`上筛选，以查看Analytics点击。

   ![筛选条件  `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. 比较两次点击之间的ID值。 所有值都将位于查询字符串参数中，但Analytics点击中的报表包ID除外，该ID是紧靠`/b/ss/`之后的URL路径。

   | ID | Analytics参数 | Advertising Cloud参数 |
   |--- |--- |--- |
   | Experience CloudIMS组织 | `mcorgid` | `_les_imsOrgid` |
   | 补充数据ID | sdid | `_les_sdid` |
   | Analytics报表包 | `/b/ss/`之后的值 | `_les_rsid` |
   | Experience Cloud访客ID | mid | `_les_mid` |

   如果ID值匹配，则确认JavaScript实施。 Advertising Cloud将向[!DNL Analytics]服务器发送任何点进或显示到达跟踪详细信息（如果存在）。

#### 如何使用[!DNL Adobe Experience Cloud Debugger]确认代码

1. 在您的主页上打开[[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using/run-debugger.html)。
1. 转到[!UICONTROL Network]选项卡。
1. 在[!UICONTROL Solutions Filter]工具栏中，单击[!UICONTROL Advertising Cloud]和[!UICONTROL Analytics]。
1. 在[!UICONTROL Request URL – Hostname]参数行中，找到`lasteventf-tm.everesttech.net`。
1. 在[!UICONTROL Request – Parameters*]行中，审核生成的信号，类似于“[How to Confirm the Code with [!DNL Chrome Developer Tools]](#validate-js-chrome)”中的步骤3。
   * 检查以确保`SDID`参数与Adobe Analytics筛选器中的`Supplemental Data ID`参数匹配。
   * 如果未生成代码，请检查以确保在[!UICONTROL Application]选项卡中删除了Advertising Cloud Cookie。 删除后，刷新页面并重复该过程。

   ![审核 [!DNL Analytics for Advertising Cloud] 中的JavaScript代码  [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [实施的先决条件和关键信息 [!DNL Analytics for Advertising Cloud]](prerequisites.md)

