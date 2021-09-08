---
title: 使用Advertising Cloud ID创建 [!DNL Marketing Channels] 规则
description: 了解如何使用Advertising Cloud ID为 [!DNL Analytics Marketing Channels]创建处理规则。
feature: Integration with Adobe Analytics
exl-id: null
source-git-commit: 5224d891d665b901d076ff6a203e9ff3bab80f85
workflow-type: tm+mt
source-wordcount: '766'
ht-degree: 0%

---

# 使用Advertising Cloud ID创建[!DNL Marketing Channels]处理规则

*仅具有Advertising Cloud-Adobe Analytics集成的广告商*

您可以使用Advertising Cloud ID（[AMO ID和EF ID](../ids.md)）在Adobe Analytics中配置[!DNL Marketing Channels]处理规则。 将Advertising Cloud ID用于特定于您的Advertising Cloud促销活动的规则。

## 处理规则中的AMO ID

AMO ID是用于在[!DNL Analytics]内报告Advertising Cloud数据的主要跟踪代码。 AMO ID是由Adobe管理的动态值拼接而成，用于在[!DNL Analytics]内提供精细报表。 它存储在[!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html)或rVar维度(AMO ID)中。 AMO ID可通过两种方式在[!DNL Analytics]中设置：

* 点进跟踪：Advertising Cloud在链接中设置`s_kwcid`查询字符串参数，并在发生点进时从登陆页面URL中选取参数。[!DNL Analytics]
* 显示到达跟踪（仅限[!DNL DSP]）：上次事件服务在服务器端检测到显示到达，并将AMO ID发送到[!DNL Analytics]。 在这种情况下，URL不包含`s_kwcid`参数。

AMO ID中的动态值表示已跟踪的营销渠道：

* AMO ID中的前缀可用于标识[!DNL Marketing Channels]中的顶级渠道。

* AMO ID正文中的字符短语表示更具体的促销活动类型。

* [!DNL DSP]显示到达流量存在后缀“vt”，可用于创建单独的点进和显示到达[!DNL DSP]渠道。

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

[!UICONTROL Paid Search]渠道的[!DNL Marketing Channels]处理规则可能如下所示：

![规则示 [!UICONTROL Paid Search] 例](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

[!UICONTROL YouTube Video Ads]渠道的[!DNL Marketing Channels]处理规则可能如下所示：

![规则示 [!UICONTROL YouTube Video Ads] 例](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> 请务必按特定顺序运行规则。 如果按顺序运行上述两个规则，则[!DNL YouTube]视频广告流量都将属于[!UICONTROL Paid Search]渠道，因为AMO ID将以“AL！”开头 并包含“！ytv！”。

## 处理规则中的EF ID

AMO EF ID(EF ID)是[!DNL Analytics for Advertising Cloud]集成中使用的第二个跟踪代码。 其主要目的是跟踪[!DNL Analytics]事件数据并将其传递到Advertising Cloud。 每次发生点进或显示到达时，都会生成一个唯一的EF ID，即使它是同一访客的完全相同的广告。 EF ID未在[!DNL Analytics]报表用户界面中使用，因为它通常超过[!DNL Analytics]中每个变量限制的500k唯一值，使其无法用于报表。 Advertising Cloud量度和元数据未应用于EF ID;它们仅应用于AMO ID。 在Advertising Cloud中优化促销活动时需要添加跟踪粒度，因此需要两个ID。

尽管EF ID维度不直接用在[!DNL Analytics]报表中，但EF ID在创建营销渠道时可能会很有用。 EF ID后缀表示渠道（显示或搜索）以及访问是由点进还是显示到达驱动。 EF ID中的分隔符为冒号，而不是AMO ID中的感叹号。

| EF ID后缀 | 渠道 |
|-------|---------|
| :s | [!UICONTROL Paid Search] |
| :d | [!UICONTROL Display Click-through] |
| :i | [!UICONTROL Display View-through] |

### 使用EF ID的处理规则示例

#### 显示点进规则

通过仅捕获点进次数来创建显示点进营销渠道。 由于点进次数和显示到达次数的AMO ID相同，因此此规则使用EF ID变量和`ef_id`查询字符串参数。

有时，点进次数会通过URL（默认）进行跟踪。 在其他情况下，点进次数会通过服务器端的上一个事件服务进行跟踪，因此URL不包含`ef_id`参数。 因此，该规则会检查EF ID变量或`ef_id`查询字符串参数以“：d”结尾的条件。 使用“`Any`”运算符，因为您希望针对任一条件触发此规则。

![显示点进规则的示例](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### 显示显示显示到达规则

要创建显示显示显示显示通览渠道，请创建EF ID以“：i”结尾的规则。 由于访客未点击该广告，因此显示到达跟踪在URL中不包含`ef_id`或`s_kwcid`。 因此，只需要一个条件。

![显示显示显示显示到达规则的示例](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>* [的基本原理 [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [为何渠道数据在Advertising Cloud和 [!DNL Marketing Channels]](mc-data-variances.md)
>* [ [!DNL Analytics Marketing Channels] 使用Advertising Cloud数据](mc-ac-data.md)
>* [视频：使用Advertising Cloud报告 [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Advertising Cloud ID使用者 [!DNL Analytics]](/help/integrations/analytics/ids.md)

