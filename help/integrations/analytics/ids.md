---
title: Advertising Cloud [!DNL Analytics]使用的ID
description: Advertising Cloud [!DNL Analytics]使用的ID
feature: Integration with Adobe Analytics
exl-id: ed1aab7b-9bd0-4d42-9bfb-9c6fa6db76bc
source-git-commit: 185fc7d79798a0a3a9ad5829b701aeb53a4a47c1
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Advertising Cloud [!DNL Analytics]使用的ID

*仅具有Advertising Cloud-Adobe Analytics集成的广告商*

*适用于Advertising Cloud DSP和Advertising Cloud Search*

Advertising Cloud使用两个ID进行现场性能跟踪： EF ID和AMO ID。

在出现广告展示时，Advertising Cloud会创建AMO ID和EF ID值并进行存储。 如果访客在未点击广告的情况下就进入了网站，则[!DNL Analytics]会通过[!DNL Analytics for Advertising Cloud] JavaScript代码从Advertising Cloud中调用这些值。 对于显示到达流量，[!DNL Analytics]会生成一个补充ID(`SDID`)，用于将EF ID和AMO ID拼合到[!DNL Analytics]中。 对于点进流量，使用`s_kwcid`和`ef_id`查询字符串参数将这些ID包含在登陆页面URL中。

Advertising Cloud使用以下条件区分网站的点进或显示到达条目：

* 当用户在查看广告但未单击广告后访问网站时，即会捕获显示到达条目。 [!DNL Analytics] 如果满足以下两个条件，则记录显示到达：
   * 在[点击回顾窗口](#lookback-a4adc)期间，访客没有对[!DNL DSP]或[!DNL Search]广告的点进次数。
   * 在[展示回顾窗口](#lookback-a4adc)期间，访客至少看到了一个[!DNL DSP]广告。 最后一次展示作为显示到达传递。
* 当网站访客在进入网站之前点击广告时，会捕获点进条目。 [!DNL Analytics] 在发生以下任一情况时捕获点进：
   * 该URL包含由Advertising Cloud添加到登陆页面URL的EF ID和AMO ID。
   * URL不包含跟踪代码，但Advertising Cloud JavaScript代码会在过去两分钟内检测到一次点击。

![Advertising Cloud基于视图的集 [!DNL Analytics] 成](/help/integrations/assets/a4adc-view-through-process.png)

*图1:Advertising Cloud基于视图的集 [!DNL Analytics] 成*

![Advertising Cloud基于点击URL的集 [!DNL Analytics] 成](/help/integrations/assets/a4adc-click-through-process.png)

*图2:Advertising Cloud基于点击URL的集 [!DNL Analytics] 成*

## Advertising Cloud EF ID

EF ID是Advertising Cloud用于将活动与在线点击或广告曝光关联的唯一令牌。 EF ID存储在[!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html)或rVar(保留eVar)维度(Advertising Cloud EF ID)中，并跟踪单个浏览器或设备级别的每次广告点击或曝光。 EF ID主要用作将[!DNL Analytics]数据发送到Advertising Cloud以在Advertising Cloud中进行报告和竞价优化的键值。

### EF ID格式

```<Advertising Cloud visitor ID>:<timestamp>:<channel type>```

<!-- <*Advertising Cloud visitor ID*>:<*timestamp*>:<*channel type*> -->

其中：

* &lt;>Advertising Cloud访客ID *>是每个访客的唯一ID（例如UhKVaAABCKj0mDt）。*&#x200B;也称为&#x200B;*冲浪ID*。

* &lt;>timestamp *>是格式为YYYYMMDDHHMMSS的时间(例如2019年的20190821192533、月08、第21天、时间19:25:33)。*

* &lt;>channel type *>是负责点击或曝光的渠道类型：*

   * `d` 点击DSP显示广告（显示点进）
   * `i` 显示DSP展示广告（显示显示显示到达）
   * `s` 搜索广告的点击（搜索点进）。

示例`EF `ID:WcmibgAAAHJK1RyY:1551968087687:d

>[!NOTE]
>
>EF ID区分大小写。 如果[!DNL Analytics]实施强制将URL跟踪设为小写，则Advertising Cloud将无法识别该EF ID。 这将影响Advertising Cloud的竞价和报告，但对[!DNL Analytics]内的Advertising Cloud报表没有影响。

### [!DNL Analytics]中的EF IDDimension

在[!DNL Analytics]报表中，您可以通过搜索[!UICONTROL EF ID]维度并使用[!UICONTROL EF ID Instance]量度来查找EF ID数据。

`EF IDs` 受Analysis Workspace中50万个唯一标识符限制的约束。达到500k值后，所有新跟踪代码都将报告在单行项目标题“[!UICONTROL Low Traffic]”下。 由于可能缺少报表保真度，因此未对`EF IDs`进行分类，您不应将它们用于[!DNL Analytics]中的区段或报表。

## Advertising Cloud AMO ID

AMO ID在较小粒度级别跟踪每个唯一广告组合，用于[!DNL Analytics]数据分类和从Advertising Cloud摄取广告量度（如展示次数、点击次数和成本）。 AMO ID存储在[!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html)或rVar维度(AMO ID)中，专门用于在[!DNL Analytics]中报告。

AMO ID也称为`s_kwcid`，有时称为“squid”。

### [!DNL DSP]的AMO ID格式

```<Channel ID>!<Ad ID>!<Placement ID>```

其中：

* &lt;>渠道ID *>可以是：*

   * `AC` = Advertising Cloud DSP
   * `AL` 对于Advertising Cloud Search

* &lt;>广告ID *>用于由Advertising Cloud生成的广告唯一标识符。*&#x200B;它用作将Advertising Cloud实体元数据转换为可读[!DNL Analytics]维度的键。

* &lt;>版面ID *>是Advertising Cloud生成的版面唯一标识符。*&#x200B;它用作将Advertising Cloud实体元数据转换为可读[!DNL Analytics]维度的键。

<!-- <*Channel ID*>!<*Ad ID*>!<*Placement ID*>

where:

* <*Channel ID*> may be:

    * `AC` = Advertising Cloud DSP
    * `AL` for Advertising Cloud Search

* <*Ad ID*> is used an Advertising Cloud-generated unique identifier for an ad. It serves as a key for translating Advertising Cloud entity metadata into readable [!DNL Analytics] dimensions.

* <*Placement ID*> is an Advertising Cloud-generated unique identifier for an placement. It serves as a key for translating Advertising Cloud entity metadata into readable [!DNL Analytics] dimensions.
 -->

AMO ID示例：AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

### [!DNL Search]的AMO ID格式

[!DNL Search]的AMO ID遵循每个搜索引擎的不同格式。 所有搜索引擎的格式以下列内容开头：

```AL!{ef_userid}!{ef_sid}```

其中：

* `AL` 是搜索渠道的渠道ID。
* `{ef_userid}` 是Advertising Cloud分配给广告商的唯一数字用户ID。
* `{ef_sid}` 是Advertising Cloud用于指定搜索引擎的数字ID，如 `3`  [!DNL Google Ads] 或 `10`  [!DNL Microsoft Advertising]。

以下是几个搜索引擎的完整AMO ID格式。 有关其他搜索引擎的AMO ID格式，请联系您的Adobe客户经理。

[!DNL Google Ads]的AMO ID格式：

```AL!{ef_userid}!{ef_sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}```

其中：

* `{creative}` 是创 [!DNL Google Ads] 作的唯一数字ID。
* `{matchtype}` 是触发广告的关键词的匹配类型： `e` 对于精确， `p` 对于短语，或 `b` 者广泛。
* `{placement}` 是广告被点击的网站的域名。对于定位版面的促销活动中的广告以及内容网站上显示的关键词定位促销活动中的广告，此值可用。
* `{network}` 指示发生点击的网络：  `g` 搜索( [!DNL Google] 仅限关键词定向广告)、 `s` 搜索合作伙伴（仅限关键词定向广告）或 `d` 显示网络（针对关键词或定位广告）。
* `{keyword}` 是触发广告的特定关键词（在搜索网站上）或最佳匹配关键词（在内容网站上）。

[!DNL Microsoft Advertising]的AMO ID格式：

```AL!{ef_userid}!{ef_sid}!{AdId}!{OrderItemId}```

其中：

* `{AdId}` 是创 [!DNL Microsoft Advertising] 作的唯一数字ID。
* `{OrderItemId}` 是关 [!DNL Microsoft Advertising] 键词的数字ID。

### [!DNL Analytics]中的AMO IDDimension

在Analytics报表中，您可以通过搜索[!UICONTROL AMO ID]维度并使用[!UICONTROL AMO ID Instance]量度来查找AMO ID数据。 [!UICONTROL AMO ID]维度存储捕获的所有AMO ID值，而[!UICONTROL AMO ID Instance]量度指示网站捕获AMO ID值的频率。 例如，如果同一搜索广告被点击四次，而Analytics跟踪了七个网站条目，则[!UICONTROL AMO ID Instance]将为七(7),[!UICONTROL Clicks]将为四(4)。

对于[!DNL Analytics]中的任何报告或审核，最佳做法是将AMO ID及其相应实例一起使用。 有关更多信息，请参阅[!DNL Analytics]和Advertising Cloud之间的预期数据差异中的“[ [!DNL Analytics for Advertising Cloud]](data-variances.md#data-validation)的数据验证”。

## 关于Analytics分类

在[!DNL Analytics]中，[分类](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html)是给定跟踪代码（如帐户、营销活动或广告）的一段元数据。 Advertising Cloud使用分类对Advertising Cloud原始数据进行分类，以便您在生成报表时可以通过不同方式（如按广告类型或促销活动）显示数据。 分类构成了[!DNL Analytics]中Advertising Cloud报表的基础，可与AMO量度（如[!UICONTROL AMO Cost]、[!UICONTROL AMO Impressions]和[!UICONTROL AMO Clicks]）以及自定义和标准现场事件（如[!UICONTROL Visits]、[!UICONTROL Leads]、[!UICONTROL Orders]和[!UICONTROL Revenue]）一起使用。

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [和之间的预期数 [!DNL Analytics] 据差异Advertising Cloud](data-variances.md)

