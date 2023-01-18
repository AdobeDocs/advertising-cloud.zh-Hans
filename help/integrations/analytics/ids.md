---
title: Adobe使用的广告ID [!DNL Analytics]
description: Adobe使用的广告ID [!DNL Analytics]
feature: Integration with Adobe Analytics
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '1186'
ht-degree: 0%

---

# Adobe使用的广告ID [!DNL Analytics]

*仅具有Adobe广告与Adobe Analytics集成的广告商*

*适用于Advertising DSP和[!DNL Advertising Search]*

Adobe广告使用两个ID进行网站性能跟踪：the *EF ID* 和 *AMO ID*.

在出现广告展示时，Adobe广告会创建AMO ID和EF ID值并进行存储。 当访客在未点击广告的情况下进入网站时， [!DNL Analytics] 从Adobe广告通过 [!DNL Analytics for Advertising] JavaScript代码。 对于显示到达流量， [!DNL Analytics] 生成补充ID(`SDID`)，用于将EF ID和AMO ID拼合到 [!DNL Analytics]. 对于点进流量，这些ID会使用 `s_kwcid` 和 `ef_id` 查询字符串参数。

Adobe广告可使用以下条件区分网站的点进或显示到达条目：

* 当用户在查看广告但未单击广告后访问网站时，即会捕获显示到达条目。 [!DNL Analytics] 如果满足以下两个条件，则记录显示到达：
   * 访客没有 [!DNL DSP] 或 [!DNL Search] 广告时段 [点击回顾窗口](#lookback-a4adc).
   * 访客至少已看到一次 [!DNL DSP] 广告时段 [展示回顾窗口](#lookback-a4adc). 最后一次展示作为显示到达传递。
* 当网站访客在进入网站之前点击广告时，会捕获点进条目。 [!DNL Analytics] 在发生以下任一情况时捕获点进：
   * 该URL包含由Adobe广告添加到登陆页面URL的EF ID和AMO ID。
   * URL不包含跟踪代码，但Adobe广告JavaScript代码会在过去两分钟内检测到一次点击。

![Adobe广告视图 [!DNL Analytics] 集成](/help/integrations/assets/a4adc-view-through-process.png)

*图1:Adobe广告视图 [!DNL Analytics] 集成*

![Adobe广告点击URL [!DNL Analytics] 集成](/help/integrations/assets/a4adc-click-through-process.png)

*图2:Adobe广告点击URL [!DNL Analytics] 集成*

## Adobe广告EF ID

EF ID是Adobe广告用来将活动与在线点击或广告曝光关联的唯一令牌。 EF ID存储在 [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) 或rVar(保留的eVar)维度(Adobe广告EF ID)，并跟踪单个浏览器或设备级别的每次广告点击或曝光。 EF ID主要用作发送密钥 [!DNL Analytics] Adobe广告中用于Adobe广告中报告和竞价优化的数据。

### EF ID格式

>[!NOTE]
>
>EF ID区分大小写。 如果 [!DNL Analytics] 实施会强制将URL跟踪设为小写，然后Adobe广告将无法识别EF ID。 这将影响Adobe广告的竞价和报告，但不会影响 [!DNL Analytics].

#### [!DNL Google Ads] 搜索广告

```{gclid}:G:s```

其中：

* `gclid` 是 [!DNL Google Click ID] (GCLID)。
* `s` 是用于搜索的网络类型(“s”)。

#### Microsoft广告搜索广告

```{msclkid}:G:s```

其中：

* `msclkid` 是 [!DNL Microsoft Click ID] (MSCLKID)。
* `s` 是用于搜索的网络类型(“s”)。

#### 在其他搜索引擎上显示广告和搜索广告

```<Adobe Advertising visitor ID>:<timestamp>:<channel type>```

其中：

* &lt;*Adobe广告访客ID*>是每个访客的唯一ID（例如UhKVaAABCKJ0MDt）。 也称为 *冲浪ID*.

* &lt;*timestamp*>是格式为YYYYMMDDHHMMSS的时间(例如2019年的20190821192533，月08，第21天，时间19):25:33)。

* &lt;*渠道类型*>是负责点击或曝光的渠道类型：

   * `d` 点击DSP显示广告（显示点进）
   * `i` 显示DSP展示广告（显示显示显示到达）
   * `s` 搜索广告的点击（搜索点进）。

示例 `EF `ID:WcmibgAAAHJK1RyY:1551968087687:d

### 中的EF IDDimension [!DNL Analytics]

在 [!DNL Analytics] 报表，您可以通过搜索 [!UICONTROL EF ID] 维度和使用 [!UICONTROL EF ID Instance] 量度。

EF ID受Analysis Workspace中50万个唯一标识符限制的约束。 达到500k值后，所有新跟踪代码都将报告在单行项目标题“[!UICONTROL Low Traffic].&quot; 由于可能缺少报表保真度，因此不会对EF ID进行分类，您不应将它们用于中的区段或报表 [!DNL Analytics].

## Adobe广告AMO ID

AMO ID可在较小粒度级别跟踪每个唯一广告组合，用于 [!DNL Analytics] 数据分类和从Adobe广告中摄取广告量度（例如展示次数、点击次数和成本）。 AMO ID存储在 [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) 或rVar维度(AMO ID)，专门用于 [!DNL Analytics].

AMO ID也称为 `s_kwcid`，有时发音为“[!DNL the squid].&quot;

### 的AMO ID格式 [!DNL DSP]

```<Channel ID>!<Ad ID>!<Placement ID>```

其中：

* &lt;*渠道ID*>可能是：

   * `AC` = Advertising DSP
   * `AL` 表示 [!DNL Advertising Search]

* &lt;*广告ID*>用于广告的Adobe广告生成的唯一标识符。 它用作将Adobe广告实体元数据转换为可读的关键 [!DNL Analytics] 维度。

* &lt;*版面ID*>是Adobe广告生成的版面唯一标识符。 它用作将Adobe广告实体元数据转换为可读的关键 [!DNL Analytics] 维度。

AMO ID示例：AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

### 的AMO ID格式 [!DNL Search]

的AMO ID [!DNL Search] 对每个搜索引擎采用不同的格式。 所有搜索引擎的格式以下列内容开头：

```AL!{userid}!{sid}```

其中：

* `AL` 是广告网络的渠道ID。
* `{userid}` 是Adobe广告分配给广告商的唯一数字用户ID。
* `{sid}` 是Adobe广告用于指定广告网络的数字ID，例如 `3` 表示 [!DNL Google Ads] 或 `10` 表示 [!DNL Microsoft Advertising].

以下是几个广告网络的完整AMO ID格式。 有关其他广告网络的AMO ID格式，请联系您的 [!DNL Adobe] 客户团队。

的AMO ID格式 [!DNL Google Ads]:

```AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}```

其中：

* `{creative}` 是 [!DNL Google Ads] 创作元素的唯一数字ID。
* `{matchtype}` 是触发广告的关键词的匹配类型： `e` 准确地说， `p` 对于短语，或 `b` 对宽。
* `{placement}` 是广告被点击的网站的域名。 对于定位版面的促销活动中的广告以及内容网站上显示的关键词定位促销活动中的广告，此值可用。
* `{network}` 指示发生点击的网络：  `g` 表示 [!DNL Google] 搜索（仅限关键词定向广告）、 `s` （仅用于关键词定向广告），或 `d` （针对关键词或投放目标广告）。
* `{keyword}` 是触发广告的特定关键词（在搜索网站上）或最佳匹配关键词（在内容网站上）。

的AMO ID格式 [!DNL Microsoft Advertising]:

```AL!{userid}!{sid}!{AdId}!{OrderItemId}```

其中：

* `{AdId}` 是 [!DNL Microsoft Advertising] 创作元素的唯一数字ID。
* `{OrderItemId}` 是 [!DNL Microsoft Advertising] 关键词的数字ID。

### AMO IDDimension [!DNL Analytics]

在Analytics报表中，您可以通过搜索 [!UICONTROL AMO ID] 维度和使用 [!UICONTROL AMO ID Instance] 量度。 的 [!UICONTROL AMO ID] 维度存储所有捕获的AMO ID值，而 [!UICONTROL AMO ID Instance] 量度指示网站捕获AMO ID值的频率。 例如，如果同一搜索广告被点击四次，而Analytics跟踪了七个网站条目，则 [!UICONTROL AMO ID Instance] 将为七(7)和 [!UICONTROL Clicks] 就是四(4)。

对于 [!DNL Analytics]，最佳实践是将AMO ID及其相应实例一起使用。 有关更多信息，请参阅[的数据验证 [!DNL Analytics for Advertising]](data-variances.md#data-validation)”中的“预期数据差异” [!DNL Analytics] 和Adobe广告。”

## 关于Analytics分类

在 [!DNL Analytics], a [分类](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) 是给定跟踪代码（如帐户、促销活动或广告）的一段元数据。 Adobe广告使用分类对原始Adobe广告数据进行分类，以便在生成报表时以不同方式（例如按广告类型或促销活动）显示数据。 分类构成Adobe广告报告的基础 [!DNL Analytics] 和可与AMO量度一起使用，例如 [!UICONTROL AMO Cost], [!UICONTROL AMO Impressions]和 [!UICONTROL AMO Clicks]，以及自定义事件和标准网站事件(例如 [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders]和 [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* [之间的预期数据差异 [!DNL Analytics] 和Adobe广告](data-variances.md)

