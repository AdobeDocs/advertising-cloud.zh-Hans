---
title: 已下载/已上载电子表格中的列
description: 引用下载和上传的Excel QA电子表格中的列。
feature: DSP Placements
exl-id: 8a8dceed-f77d-4b6b-a842-f57528125c92
source-git-commit: 0c3984d755131ad98b7ddecfd9567ff4be54b64e
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 0%

---

# 已下载/已上载电子表格中的列

<!-- rename -- not specific enough - I think you can download Excel files of other things too -->

<!-- see notes within the table about descriptions that need to be edited -->

>[!TIP]
>
> 在下载的电子表格中，所有可编辑的列都以蓝色突出显示。

| 区域 | 列 | 描述 | 可编辑？ |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic] | [!UICONTROL Placement ID] | 版面的数字ID。 | — |
| [!UICONTROL Basic] | [!UICONTROL Placement Name] | 版面的名称。 | 是 |
| [!UICONTROL Basic] | [!UICONTROL Labels] | 任何已应用的标签，用于报表。 | — |
| [!UICONTROL Basic] | [!UICONTROL Edit Link] | 用于在编辑模式下打开版面的链接。 | — |
| [!UICONTROL Basic] | [!UICONTROL Status] | 版面状态： *[!UICONTROL active]* 或 *[!UICONTROL inactive]*. | 是 |
| [!UICONTROL Basic] | [!UICONTROL Placement Type] | 版面类型。 | — |
| [!UICONTROL Basic] | [!UICONTROL Package Name] | 父包的名称（如果适用）。 | — |
| [!UICONTROL Goals] | [!UICONTROL Start Date] | 版面的开始日期。 | — |
| [!UICONTROL Goals] | [!UICONTROL End Date] | 版面的结束日期。 | — |
| [!UICONTROL Goals] | [!UICONTROL Day parting] | 分时段是否为 *[!UICONTROL ON]* 或 *[!UICONTROL OFF]*.<br><b>注意：</b> 要检查实际的分时段计划，请在 [!DNL DSP]. | — |
| [!UICONTROL Goals] | [!UICONTROL Budget] | 版面预算（如果有）。 | 是 |
| [!UICONTROL Goals] | [!UICONTROL Budget Interval] | 预算间隔： &lt;i span=&quot;&quot; id=&quot;0&quot; translate=&quot;no&quot; />*、 *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*&#x200B;或 *[!UICONTROL All Time]*.[!UICONTROL >Daily] | 是 |
| [!UICONTROL Goals] | [!UICONTROL Optimization Goal] | 包的目标。 | — |
| [!UICONTROL Goals] | [!UICONTROL Optimization Target] | 目标的目标值。 | — |
| [!UICONTROL Goals] | [!UICONTROL Pace on] | 投放是否在朝 *[!UICONTROL Budget]* 或 *[!UICONTROL Impressions]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Max Bid] | 版面的最高竞价。 | 是 |
| [!UICONTROL Goals] | [!UICONTROL Pacing Fill Strategy] | 投放的步调填充策略： *[!UICONTROL evenly]*, *[!UICONTROL frontload]*&#x200B;或 *[!UICONTROL aggressive frontload]*. | 是 |
| [!UICONTROL Goals] | [!UICONTROL  Pre-Bid Filters] | 要应用的任何竞价前筛选条件。 | — |
| [!UICONTROL Goals] | [!UICONTROL Bidding Rules] | 是否包含竞价规则（已弃用） *[!UICONTROL ON]* 或 *[!UICONTROL OFF]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap] | 指定期间放置的主频率上限 [!UICONTROL Frequency Cap Interval]. | 是 |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap Interval] | 主频率上限的间隔： *[!UICONTROL Day]*, *[!UICONTROL Week]*&#x200B;或 *[!UICONTROL Month]*. | 是 |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap] | 指定期间放置的次频上限 [!UICONTROL Secondary Frequency Cap Interval] | 是 |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval] | 次频上限的间隔类型： *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]*&#x200B;或 *[!UICONTROL Minute]*. 适用的周数、天数、小时数或分钟数由 [!UICONTROL Secondary Frequency Cap Interval Value]. | 是 |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval Value] | 周数、天数、小时数或分钟数 [!UICONTROL Secondary Frequency Cap] 应用。 例如，如果次数量上限为每六小时3次展示次数，则此处的值将为 <b>6&lt;/>。 | 是 |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included #] | 目标地理位置的数量， *[!UICONTROL All]*&#x200B;或 *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included] | 目标地理位置，以分号分隔，或 *[!UICONTROL All Locations]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded #] | 排除的地理位置或 *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded] | 排除的地理位置，以分号分隔，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Included #] | 指定目标公共清单交易数（如果有）， *[!UICONTROL All]*&#x200B;或 *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Excluded #] | 已排除的公共清单交易（如果已指定）的数量，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Included #] | 指定目标专用库存交易（如果有）的数量， *[!UICONTROL All]*&#x200B;或 *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Excluded #] | 已排除的专用清单交易（如果已指定）的数量，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Included #] | 目标数量 [!UICONTROL On-Demand Inventory] 交易，如有指定， *[!UICONTROL All]*&#x200B;或 *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Excluded #] | 已排除的按需库存交易（如果已指定）的数量，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Traffic Type] | 目标流量类型： *[!UICONTROL Website]* 和/或 *[!UICONTROL Apps]* | — |
| [!UICONTROL Sites] | [!UICONTROL Exclude out-stream] | 排除流量的库存定位选项是否为 &lt;i span=&quot;&quot; id=&quot;0&quot; translate=&quot;no&quot; />*或 *[!UICONTROL OFF]*.[!UICONTROL >ON]<br>外流广告通常在内容上显示为弹出窗口或填充到内容中（在本机体验中），而不是视频播放器中的常规视频广告。 | — |
| [!UICONTROL Sites] | [!UICONTROL Site Tier] | 要定位的网站质量： *[!UICONTROL Tier 1]*, *[!UICONTROL Tier 2]*, *[!UICONTROL Tier 3]*&#x200B;或 *[!UICONTROL All Sites]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Included #] | 目标网站类别（如果已指定）的数量，或 *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Excluded #] | 排除的网站类别（如果已指定）的数量，或 *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Excluded Sites] | 排除的站点（如果已指定），或 *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Language] | 目标站点语言。 | — |
| [!UICONTROL Sites] | [!UICONTROL Allow unscreened sites] | （仅限标准显示版面）是否允许在未审核的网站上投放广告： *[!UICONTROL ON]* 或 *[!UICONTROL OFF]*. 当投放目标为私有内容库时，此选项可能会在被阻止的网站上投放广告。 | — |
| [!UICONTROL Sites] | [!UICONTROL Targeted Sites] | 目标站点的数量（如果已指定），或 *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Included] | 目标受众（如果已指定），或 *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Excluded] | 排除的受众（如果已指定），或 *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Demographic booster] | 是否 [!DNL Comscore] 为版面（和营销活动中的其他版面）启用了人口统计区段： *[!UICONTROL ON]* 或 *[!UICONTROL OFF]*. 此功能只能为 [!DNL Audience Verification] 的 [!DNL Nielsen] 和/或 [!DNL Comscore].  这会产生额外的费用。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Extend across screens] | 是否跨设备扩展广告定位： *[!UICONTROL ON]* 或 *[!UICONTROL OFF]*.<!-- Whether or not the Cross Device Targeting setting is enabled for the placement : *ON* or *OFF*. Cross-device targeting extends your targeting across all of a person's known device, per the device graph specified in the campaign settings.--> | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting]  — 包含# | 目标主题代码（如果已指定）的数量，或 *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting - Excluded #] | 排除的主题代码（如果已指定）的数量，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Included #] | 目标设备目标（如果已指定）的数量，或 *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Excluded #] | 已排除的设备目标（如果已指定）的数量，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Included #] | 目标ISP提供商的数量（如果已指定），或*[!UICONTROL All]/i>。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Excluded #] | 已排除的ISP提供商（如果已指定）的数量，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Contextual Filtering #] | 已应用的品牌安全过滤器数量（如果已指定），或 *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Fraud blocking #] | 已应用的投标前欺诈阻止过滤器（如果已指定）的数量，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Viewability #] | 已应用的竞价前可视性过滤器（如果已指定）的数量，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Site Safety Block] | 是否启用“站点安全块”： *[!UICONTROL ON]* 或 *[!UICONTROL OFF]*.<!-- Whether or not the advertiser-level setting Enable Site Safety Block is enabled: *ON* or *OFF*.I don’t see this option at the placement level. Should there be one? --> | — |
| [!UICONTROL Tracking] | [!UICONTROL Tracking Pixels #] | 附加到位置的第三方事件跟踪像素的数量，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL Conversion Pixels #] | 附加到位置的转化跟踪像素的数量，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL 3rd-party fees] | 要作为每1000次展示次数不可计费成本进行跟踪的第三方静态费用率（如果适用）。 | — |
| [!UICONTROL Ads] | [!UICONTROL # of Ads Attached] | 附加到版面的广告数（如果有），或 *[!UICONTROL None]*. | — |
| [!UICONTROL Ads] | [!UICONTROL Ad Names] | 附加到版面的广告名称（如果有），或 *[!UICONTROL None]*. | — |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [关于使用电子表格更正促销活动的版面设置](qa-about.md)
>* [下载营销活动的版面设置](qa-sheet-download.md)
>* [营销活动的上传版面设置](qa-sheet-upload.md)
>* [版面设置](/help/dsp/campaign-management/placements/placement-settings.md)

