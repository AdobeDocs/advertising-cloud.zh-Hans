---
title: 使用Advertising Cloud ID创建 [!DNL Marketing Channels] 规则
description: 了解如何使用Advertising Cloud ID为 [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 4fcdd586-e9c5-4405-a6dc-7799d2bac93e
source-git-commit: d136b1fe6f6fd3861d0850e07efe7c320da4a7cc
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 0%

---

# 使用Advertising Cloud ID创建 [!DNL Marketing Channels] 处理规则

*仅具有Advertising Cloud-Adobe Analytics集成的广告商*

您可以使用Advertising Cloud ID([AMO ID和EF ID](../ids.md))配置 [!DNL Marketing Channels] 处理规则。Adobe Analytics 将Advertising Cloud ID用于特定于您的Advertising Cloud促销活动的规则。

## 处理规则中的AMO ID

AMO ID是用于在 [!DNL Analytics]. AMO ID是由Adobe管理的动态值拼接而成，可在 [!DNL Analytics]. 它存储在 [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) 或rVar维度(AMO ID)。 可以在 [!DNL Analytics] 有两种方式：

* 点进跟踪：Advertising Cloud设置 `s_kwcid` 链接中的查询字符串参数，以及 [!DNL Analytics] 发生点进时，会从登陆页面URL中选取参数。
* 显示到达跟踪([!DNL DSP] 仅):上次事件服务会检测服务器端的显示到达，并将AMO ID发送到 [!DNL Analytics]. 在这种情况下，URL不包含 `s_kwcid` 参数。

AMO ID中的动态值表示已跟踪的营销渠道：

* AMO ID中的前缀可用于标识 [!DNL Marketing Channels].

* AMO ID正文中的字符短语表示更具体的促销活动类型。

* 后缀“vt”存在 [!DNL DSP] 显示到达流量，可用于创建单独的点进和显示到达 [!DNL DSP] 渠道。

可以忽略AMO ID的其余部分。

| AMO ID | 渠道 | 规则逻辑 |
|--------|---------|--------------------|
| 艾尔！ （前缀） | [!UICONTROL Paid Search] | 开头 |
| AC! （前缀） | [!UICONTROL DSP] | 开头 |
| !g! (body) | [!UICONTROL Google Search] | 包含 |
| !s! (body) | [!UICONTROL Search Partner] | 包含 |
| !d! (body) | [!UICONTROL Display Network] | 包含 |
| !u! (body) | [!UICONTROL Smart Shopping Campaign] | 包含 |
| !ytv! (body) | [!UICONTROL YouTube Video Ad] | 包含 |
| !yts! (body) | [!UICONTROL YouTube Search Ad] | 包含 |
| !vp! (body) | [!UICONTROL Google Video Partners] | 包含 |
| !vt（后缀） | [!UICONTROL DSP View-through] | 结束于 |

### 使用AMO ID的处理规则示例

的 [!DNL Marketing Channels] 处理规则 [!UICONTROL Paid Search] 渠道可能如下所示：

![示例 [!UICONTROL Paid Search] 规则](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

的 [!DNL Marketing Channels] 处理规则 [!UICONTROL YouTube Video Ads] 渠道可能如下所示：

![示例 [!UICONTROL YouTube Video Ads] 规则](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> 请务必按特定顺序运行规则。 如果上述两个规则按顺序运行，则 [!DNL YouTube] 视频广告流量都会被计入 [!UICONTROL Paid Search] 渠道，因为AMO ID将均以“AL！”开头 并包含“！ytv！”。

## 处理规则中的EF ID

AMO EF ID(EF ID)是 [!DNL Analytics for Advertising Cloud] 集成。 其主要目的是跟踪和传递 [!DNL Analytics] 事件数据导入Advertising Cloud。 每次发生点进或显示到达时，都会生成一个唯一的EF ID，即使它是同一访客的完全相同的广告。 EF ID未在 [!DNL Analytics] 报告用户界面，因为它通常超过 [!DNL Analytics]，使其无法用于报表。 Advertising Cloud量度和元数据未应用于EF ID;它们仅应用于AMO ID。 在Advertising Cloud中优化促销活动时需要添加跟踪粒度，因此需要两个ID。

尽管EF ID维度不会直接在 [!DNL Analytics] 报表时，EF ID可用于创建营销渠道。 EF ID后缀表示渠道（显示或搜索）以及访问是由点进还是显示到达驱动。 EF ID中的分隔符为冒号，而不是AMO ID中的感叹号。

| EF ID后缀 | 渠道 |
|-------|---------|
| :s | [!UICONTROL Paid Search] |
| :d | [!UICONTROL Display Click-through] |
| :i | [!UICONTROL Display View-through] |

### 使用EF ID的处理规则示例

#### 显示点进规则

通过仅捕获点进次数来创建显示点进营销渠道。 由于点进次数和显示到达的AMO ID相同，因此此规则使用EF ID变量和 `ef_id` 查询字符串参数。

有时，点进次数会通过URL（默认）进行跟踪。 在其他情况下，点进次数会通过服务器端的上一个事件服务进行跟踪，因此URL不包含 `ef_id` 参数。 因此，该规则会检查EF ID变量或 `ef_id` 查询字符串参数以“：d”结尾。 使用“`Any`“运算符，因为您希望针对任一条件触发此规则。

![显示点进规则的示例](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### 显示显示显示到达规则

要创建显示显示显示显示通览渠道，请创建EF ID以“：i”结尾的规则。 由于访客未点击广告，因此显示到达跟踪不包括 `ef_id` 或 `s_kwcid` ，因此规则只需要一个条件。

![显示显示显示显示到达规则的示例](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>* [的基本原理 [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [为何渠道数据在Advertising Cloud和 [!DNL Marketing Channels]](mc-data-variances.md)
>* [使用 [!DNL Analytics Marketing Channels] 使用Advertising Cloud数据](mc-ac-data.md)
>* [视频：使用Advertising Cloud报告 [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Advertising Cloud ID使用者 [!DNL Analytics]](/help/integrations/analytics/ids.md)

