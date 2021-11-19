---
title: Advertising Cloud ID使用者 [!DNL Analytics]
description: Advertising Cloud ID使用者 [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ed1aab7b-9bd0-4d42-9bfb-9c6fa6db76bc
source-git-commit: 1ba45d789c4ad365166df829ac74e0200cdc8851
workflow-type: tm+mt
source-wordcount: '1156'
ht-degree: 0%

---

# Advertising Cloud ID使用者 [!DNL Analytics]

*仅具有Advertising Cloud-Adobe Analytics集成的广告商*

*适用于Advertising Cloud DSP和Advertising Cloud Search*

Advertising Cloud使用两个ID进行现场性能跟踪：the *EF ID* 和 *AMO ID*.

在出现广告展示时，Advertising Cloud会创建AMO ID和EF ID值并进行存储。 当访客在未点击广告的情况下进入网站时， [!DNL Analytics] 通过 [!DNL Analytics for Advertising Cloud] JavaScript代码。 对于显示到达流量， [!DNL Analytics] 生成补充ID(`SDID`)，用于将EF ID和AMO ID拼合到 [!DNL Analytics]. 对于点进流量，这些ID会使用 `s_kwcid` 和 `ef_id` 查询字符串参数。

Advertising Cloud使用以下条件区分网站的点进或显示到达条目：

* 当用户在查看广告但未单击广告后访问网站时，即会捕获显示到达条目。 [!DNL Analytics] 如果满足以下两个条件，则记录显示到达：
   * 访客没有 [!DNL DSP] 或 [!DNL Search] 广告时段 [点击回顾窗口](#lookback-a4adc).
   * 访客至少已看到一次 [!DNL DSP] 广告时段 [展示回顾窗口](#lookback-a4adc). 最后一次展示作为显示到达传递。
* 当网站访客在进入网站之前点击广告时，会捕获点进条目。 [!DNL Analytics] 在发生以下任一情况时捕获点进：
   * 该URL包含由Advertising Cloud添加到登陆页面URL的EF ID和AMO ID。
   * URL不包含跟踪代码，但Advertising Cloud JavaScript代码会在过去两分钟内检测到一次点击。

![Advertising Cloud视图 [!DNL Analytics] 集成](/help/integrations/assets/a4adc-view-through-process.png)

*图1:Advertising Cloud视图 [!DNL Analytics] 集成*

![Advertising Cloud点击基于URL [!DNL Analytics] 集成](/help/integrations/assets/a4adc-click-through-process.png)

*图2:Advertising Cloud点击基于URL [!DNL Analytics] 集成*

## Advertising Cloud EF ID

EF ID是Advertising Cloud用于将活动与在线点击或广告曝光关联的唯一令牌。 EF ID存储在 [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) 或rVar(保留eVar)维度(Advertising Cloud EF ID)，并跟踪单个浏览器或设备级别的每次广告点击或曝光。 EF ID主要用作发送密钥 [!DNL Analytics] 数据到Advertising Cloud，以便在Advertising Cloud中进行报告和竞价优化。

### EF ID格式

```<Advertising Cloud visitor ID>:<timestamp>:<channel type>```

<!-- <*Advertising Cloud visitor ID*>:<*timestamp*>:<*channel type*> -->

其中：

* &lt;*Advertising Cloud访客ID*>是每个访客的唯一ID（例如UhKVaAABCKJ0MDt）。 也称为 *冲浪ID*.

* &lt;*timestamp*>是格式为YYYYMMDDHHMMSS的时间(例如2019年的20190821192533，月08，第21天，时间19):25:33)。

* &lt;*渠道类型*>是负责点击或曝光的渠道类型：

   * `d` 点击DSP显示广告（显示点进）
   * `i` 显示DSP展示广告（显示显示显示到达）
   * `s` 搜索广告的点击（搜索点进）。

示例 `EF `ID:WcmibgAAAHJK1RyY:1551968087687:d

>[!NOTE]
>
>EF ID区分大小写。 如果 [!DNL Analytics] 实施会强制将URL跟踪设为小写，然后Advertising Cloud将无法识别EF ID。 这将影响Advertising Cloud的竞价和报告，但不会影响 [!DNL Analytics].

### 中的EF IDDimension [!DNL Analytics]

在 [!DNL Analytics] 报表，您可以通过搜索 [!UICONTROL EF ID] 维度和使用 [!UICONTROL EF ID Instance] 量度。

`EF IDs` 受Analysis Workspace中50万个唯一标识符限制的约束。 达到500k值后，所有新跟踪代码都将报告在单行项目标题“[!UICONTROL Low Traffic].&quot; 由于报告保真度可能缺失， `EF IDs` 未进行分类，因此您不应将其用于 [!DNL Analytics].

## Advertising Cloud AMO ID

AMO ID可在较小粒度级别跟踪每个唯一广告组合，用于 [!DNL Analytics] 数据分类和广告量度摄取（如展示次数、点击次数和成本）从Advertising Cloud获取。 AMO ID存储在 [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) 或rVar维度(AMO ID)，专门用于 [!DNL Analytics].

AMO ID也称为 `s_kwcid`，有时称为“squid”。

### 的AMO ID格式 [!DNL DSP]

```<Channel ID>!<Ad ID>!<Placement ID>```

其中：

* &lt;*渠道ID*>可能是：

   * `AC` = Advertising Cloud DSP
   * `AL` 对于Advertising Cloud Search

* &lt;*广告ID*>是Advertising Cloud生成的广告唯一标识符。 它用作将Advertising Cloud实体元数据转换为可读数据的键 [!DNL Analytics] 维度。

* &lt;*版面ID*>是Advertising Cloud生成的版面唯一标识符。 它用作将Advertising Cloud实体元数据转换为可读数据的键 [!DNL Analytics] 维度。

<!-- <*Channel ID*>!<*Ad ID*>!<*Placement ID*>

where:

* <*Channel ID*> may be:

    * `AC` = Advertising Cloud DSP
    * `AL` for Advertising Cloud Search

* <*Ad ID*> is used an Advertising Cloud-generated unique identifier for an ad. It serves as a key for translating Advertising Cloud entity metadata into readable [!DNL Analytics] dimensions.

* <*Placement ID*> is an Advertising Cloud-generated unique identifier for an placement. It serves as a key for translating Advertising Cloud entity metadata into readable [!DNL Analytics] dimensions.
 -->

AMO ID示例：AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

### 的AMO ID格式 [!DNL Search]

的AMO ID [!DNL Search] 对每个搜索引擎采用不同的格式。 所有搜索引擎的格式以下列内容开头：

```AL!{ef_userid}!{ef_sid}```

其中：

* `AL` 是搜索渠道的渠道ID。
* `{ef_userid}` 是Advertising Cloud分配给广告商的唯一数字用户ID。
* `{ef_sid}` 是Advertising Cloud用于指定搜索引擎的数字ID，例如 `3` 表示 [!DNL Google Ads] 或 `10` 表示 [!DNL Microsoft Advertising].

以下是几个搜索引擎的完整AMO ID格式。 有关其他搜索引擎的AMO ID格式，请联系您的 [!DNL Adobe] 客户经理。

的AMO ID格式 [!DNL Google Ads]:

```AL!{ef_userid}!{ef_sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}```

其中：

* `{creative}` 是 [!DNL Google Ads] 创作元素的唯一数字ID。
* `{matchtype}` 是触发广告的关键词的匹配类型： `e` 准确地说， `p` 对于短语，或 `b` 对宽。
* `{placement}` 是广告被点击的网站的域名。 对于定位版面的促销活动中的广告以及内容网站上显示的关键词定位促销活动中的广告，此值可用。
* `{network}` 指示发生点击的网络：  `g` 表示 [!DNL Google] 搜索（仅限关键词定向广告）、 `s` （仅用于关键词定向广告），或 `d` （针对关键词或投放目标广告）。
* `{keyword}` 是触发广告的特定关键词（在搜索网站上）或最佳匹配关键词（在内容网站上）。

的AMO ID格式 [!DNL Microsoft Advertising]:

```AL!{ef_userid}!{ef_sid}!{AdId}!{OrderItemId}```

其中：

* `{AdId}` 是 [!DNL Microsoft Advertising] 创作元素的唯一数字ID。
* `{OrderItemId}` 是 [!DNL Microsoft Advertising] 关键词的数字ID。

### AMO IDDimension [!DNL Analytics]

在Analytics报表中，您可以通过搜索 [!UICONTROL AMO ID] 维度和使用 [!UICONTROL AMO ID Instance] 量度。 的 [!UICONTROL AMO ID] 维度存储所有捕获的AMO ID值，而 [!UICONTROL AMO ID Instance] 量度指示网站捕获AMO ID值的频率。 例如，如果同一搜索广告被点击四次，而Analytics跟踪了七个网站条目，则 [!UICONTROL AMO ID Instance] 将为七(7)和 [!UICONTROL Clicks] 就是四(4)。

对于 [!DNL Analytics]，最佳实践是将AMO ID及其相应实例一起使用。 有关更多信息，请参阅[的数据验证 [!DNL Analytics for Advertising Cloud]](data-variances.md#data-validation)”中的“预期数据差异” [!DNL Analytics] 和Advertising Cloud。”

## 关于Analytics分类

在 [!DNL Analytics], a [分类](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) 是给定跟踪代码（如帐户、促销活动或广告）的一段元数据。 Advertising Cloud使用分类对Advertising Cloud原始数据进行分类，以便您在生成报表时可以通过不同方式（如按广告类型或促销活动）显示数据。 分类构成Advertising Cloud报表的基础，如 [!DNL Analytics] 和可与AMO量度一起使用，例如 [!UICONTROL AMO Cost], [!UICONTROL AMO Impressions]和 [!UICONTROL AMO Clicks]以及自定义和标准的现场事件(如 [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders]和 [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [之间的预期数据差异 [!DNL Analytics] 和Advertising Cloud](data-variances.md)

