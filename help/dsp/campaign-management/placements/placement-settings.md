---
title: 版面设置
description: 请参阅可用版面设置的描述。
feature: DSP Placements
exl-id: 36097132-e589-4d49-bf86-54f61eae5b67
source-git-commit: c2fbaf3381ca4380c18d55931e9f4f662da892af
workflow-type: tm+mt
source-wordcount: '3278'
ht-degree: 0%

---

# 版面设置

## [!UICONTROL Basics]

**[!UICONTROL Placement name]** 版面名称。

>[!TIP]
>使用适合您情况的命名约定。 一种建议的命名约定是“*\&lt;campaign name=&quot;&quot;>:\&lt;ad unit=&quot;&quot;>:\&lt;duration>:\&lt;targeting>*.&quot;

**[!UICONTROL Status]:** 版面状态： *[!UICONTROL Active]* （默认）或 *[!UICONTROL Paused]*.

>[!TIP]
>最佳实践是暂停版面，直到您准备好启动它为止。

**[!UICONTROL Details]:** （只读）适用的广告类型、创建或创建版面的帐户以及父营销活动。 要查看更多详细信息，请单击 **[!UICONTROL Show more]**.

**[!UICONTROL Templates]:** 打开现有版面模板的列表。 要从模板自动填充定位设置，请执行以下操作：

1. 执行以下任一操作：

   * 要重复使用模板中的所有目标，请选中模板名称旁边的复选框。

   * 要从模板中重复使用单个目标类型，请展开模板名称，然后选中要重复使用的目标类型旁边的复选框。

1. 单击 **[!UICONTROL Apply]**.

**[!UICONTROL Ad specs for forecast]:** （仅限视频广告格式）广告持续时间和/或广告规范，用于计算右侧的预测投影。 字段因广告类型而异。

**[!UICONTROL Placement tags]:** （可选）用于帮助您查找此版面的关键字或昵称。

## 目标

**[!UICONTROL Package]:** （可选）分配了版面的包。 单击 ![编辑](/help/dsp/assets/edit.png) 选择和现有资源包或创建新资源包。 将版面分配给包时， [!UICONTROL Goals] 部分将更新为投放日期、投放目标和包中的预算。

**[!UICONTROL Flight Dates]:** 版面的开始日期和结束日期。 当投放处于活动状态并分配给活动包或营销策划时，已批准的广告有资格在投放期间运行。

默认情况下，资源包（如果适用）或营销活动的日期会自动填充。

>[!NOTE]
>
>* 投放日期必须包含在营销活动投放日期和包装投放日期中。


### 分配给具有包级别步调的包的位置

**[!UICONTROL Placement Funding]:** 如何预算版面：

* *[!UICONTROL Optimize based on performance]:* 在资源包级别控制预算。
* *[!UICONTROL Set a fixed budget cap]:* 允许您设置每日、每周、每月或全时版面预算。 输入值和持续时间(*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*)。

**[!UICONTROL Max Bid]:** 最多为1000次展示次数付费。

**[!UICONTROL Placement Pre-bid Filters]:** 要进行竞价，必须满足最多5个KPI阈值（如最低可见性量度或点进率）。 您可以将竞价前过滤器用作优化策略，但请了解每个规则可能会限制此版面可以竞价的机会。 添加或编辑过滤器：

1. 单击 ![编辑](/help/dsp/assets/edit.png).
1. 执行以下任一操作：
   * 添加过滤器：
      1. 单击 **[!UICONTROL Add Filter]**.
      1. 旁边 **[!UICONTROL Only bid if]**，选择一个量度，然后输入一个值。
   * 要删除过滤器，请单击 **[!UICONTROL X]** 中。
1. 单击 **[!UICONTROL Save]**.

请参阅“[版面级别的预竞价过滤器及其使用方法](/help/dsp/optimization/optimization-pre-bid-filters.md).&quot;

### 所有其他版面

**[!UICONTROL Budget Goal]:** 总预算上限和预算间隔(*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*)。

**[!UICONTROL Gross Budget Goal]:** （仅限使用毛利管理的促销活动中的版面）总预算上限和预算间隔(*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*)。

**[!UICONTROL Optimization Goal]:**  包的优化目标。 请参阅“[优化目标及其使用方法](/help/dsp/optimization/optimization-goals.md)&quot;

**[!UICONTROL Target Goal]:** 目标，用于跟踪性能。

>[!NOTE]
>
>此字段仅作为基准，不用于决策。

**[!UICONTROL Pace on]:** 步调将基于：

* **[!UICONTROL Budget goal]:** （默认）此选项在分配的预算内提供尽可能多的展示次数。

* **[!UICONTROL Impressions]:** 此选项提供展示次数，直到在指定的间隔内达到指定数量为止。 选择此选项时，请指定展示次数和间隔： *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* 或 *[!UICONTROL Weekly]*.

**[!UICONTROL Max Bid]:** 最多为1000次展示次数付费。

**[!UICONTROL Pacing Fill Strategy]:** （仅具有包级步调的包）如何调整和交付步调：

* *[!UICONTROL Even]:* （默认）在每次飞行中均匀地进行投放，目标是在上半段投放量的50%。

* *[!UICONTROL Frontload]:* 加快交付速度，使其在飞行途中完成65-75%。

* *[!UICONTROL Aggressive Frontload]:* 加快交付速度，使其在飞行途中完成75-85%。

**[!UICONTROL Placement Pre-bid Filters]:** （可选）最多必须满足5个过滤器才能进行竞价。 您可以将竞价前过滤器用作优化策略，但请记住，每个规则都可能会限制此投放可以竞价的机会。 添加或编辑过滤器：

1. 单击 ![编辑](/help/dsp/assets/edit.png).
1. 执行以下任一操作：
   * 添加过滤器：
      1. 单击 **[!UICONTROL Add Filter]**.
      1. 旁边 **[!UICONTROL Only bid if]**，选择一个量度，然后输入一个值。
   * 要删除过滤器，请单击 **[!UICONTROL X]** 中。
1. 单击 **[!UICONTROL Save]**.

## [!UICONTROL Geo-Targeting]

**[!UICONTROL Audience Location]:** （可选）要在版面中包含或排除广告的特定位置。 如果未指定任何位置，则会定位所有位置。

>[!NOTE]
>
>城市和DMA位置不适用于Roku位置。

要指定位置，请执行以下操作：

1. 单击 ![编辑](/help/dsp/assets/edit.png).
1. 执行以下任一操作：
   * 要包含或排除国家/地区、州、市、DMA、联邦立法区或州立法区，请执行以下操作：
      1. 在左列中选择位置类型。
      1. （根据需要）单击某个位置以展开该位置。
      1. 在位置旁边，单击 *[!UICONTROL Include]* 将其作为目标或 *[!UICONTROL Exclude]* 将其排除为目标。
   * 要搜索邮政编码并包含或排除所有选定的结果，请执行以下操作：
      1. 单击 **[!UICONTROL Search Postal Code]**.
      1. 选择国家/地区。
      1. 输入城市名称，然后单击 ![编辑](/help/dsp/assets/search.png).
      1. 单击正确的搜索结果。
      1. 单击 *[!UICONTROL Include All]* 将所有位置作为目标或 *[!UICONTROL Exclude All]* 将所有位置排除为目标。
   * 要输入或粘贴邮政编码，并将其全部包含或排除，请执行以下操作：
      1. 单击 **[!UICONTROL Paste Postal Code]**.
      1. 选择国家/地区。
      1. 输入或粘贴最多1000个邮政编码。
每行包含一个邮政编码，或输入多个值（以逗号分隔或制表符分隔）。
      1. 单击 *[!UICONTROL Include All]* 将所有位置作为目标或 *[!UICONTROL Exclude All]* 将所有位置排除为目标。
   * 从 [!UICONTROL Included] 或 [!UICONTROL Excluded] 列表，单击 **[!UICONTROL X]** 在右列的位置旁边。
1. 单击 **[!UICONTROL Done]**.

>[!NOTE]
>
>* 并非所有国家/地区都有州、市或邮政编码位置。
>* DMA（指定的市场区域）、联邦立法区和州立法区仅适用于美国地区。


## [!UICONTROL Inventory Targeting]

**[!UICONTROL Inventory Sources]:** 要包含或排除的库存来源作为目标。 对于大多数版面类型，默认包含所有库存类型和每种类型的所有来源。 对于 [!DNL Roku] 版面，您必须指定库存类型和来源。 您可以从以下类型的库存中进行选择：

* [!UICONTROL Public]:（除Roku之外的所有版面类型）Advertising Cloud有权访问的所有开放式Exchange库存。 您可以包含和排除公共库存。

   您可以按源或按信息源查看列表。 在按信息源查看列表时，可以按信息源名称、信息源密钥或选定的特征标记进行搜索。

* [!UICONTROL Private] | [!UICONTROL Roku Private]:您现有的私有交易（或现有的私有交易） [!DNL Roku] 交易 [!DNL Roku] 版面)与您在DSP中设置的发布者。 您可以包括但不排除公共库存。

   您可以按关键词、键值、交易ID或自定义标记搜索列表。

* [!UICONTROL On Demand] | [!UICONTROL Roku On Demand]:全部 [溢价，非担保 [!UICONTROL On Demand] 库存](/help/dsp/inventory/on-demand-inventory-about.md) (或 [!UICONTROL On Demand] [!DNL] Roku交易 [!DNL Roku] 版面) [!DNL DSP]. 您可以包含和排除 [!UICONTROL On Demand] 库存。

   您可以按源或按信息源查看列表。 在按信息源查看列表时，可以按信息源名称、信息源密钥或选定的发布者区域、类别标记或特征标记进行搜索。

要指定库存定位，请执行以下操作：

* 要排除库存类型，请清除该名称旁边的复选框。
* 要定位库存类型，请执行以下操作：
   1. 选中库存类型名称旁边的复选框。
   1. （可选）更改源以包括：
      1. 单击 ![编辑](/help/dsp/assets/edit.png).
      1. ([!UICONTROL Public] 和 [!UICONTROL On Demand] 清单)单击 *[!UICONTROL *View by Source]**或 **[!UICONTROL View by Feed]** 更改源的列表方式。
      1. （如果适用）根据需要筛选库存。
      1. 指定要包含和排除的源：
         * 包含 [!UICONTROL Public] 或 [!UICONTROL On Demand] 源，单击 **[!UICONTROL Include]** 源名称旁边。
         * 包含 [!UICONTROL Private] 源：
            * 要在交易中包含所有库存，请单击 **[!UICONTROL Include all]** 交易名称旁边。
            * 要包含单个库存来源，请展开交易名称，然后单击来源名称旁边的复选框。
         * 排除 [!UICONTROL Public] 或 [!UICONTROL On ] 源，单击 **[!UICONTROL Exclude]** 源名称旁边。
   1. （可选）要将包含定位信息的CSV文件下载到浏览器的下载位置，请单击 **[!UICONTROL Save & Export]**.
   1. 单击 **[!UICONTROL Save]**.

>[!TIP]
>
>如果您订阅了 [!UICONTROL On Demand] 清单，但无法找到要定位的发布者或交易，然后检查交易的状态。 有关状态的更多信息，请参阅 [关于 [!DNL On Demand] Premium Inventory](/help/dsp/inventory/on-demand-inventory-about.md).

**[!UICONTROL Exclude out-stream]:** （仅限视频放置）不包括流出流量。

外流广告通常在内容上显示为弹出窗口或填充到内容中（在本机体验中），而不是视频播放器中的常规视频广告。

## [!UICONTROL Site Targeting]

**[!UICONTROL Traffic type]:** 要定位的流量类型。 选项包括 **[!UICONTROL Websites]** 和 **[!UICONTROL Apps]**.

**[!UICONTROL Site tier]:** (在 **[!UICONTROL Paste list of targeted sites]** is *[!UICONTROL Off]*)要定位的网站的质量。 第1-3层都是品牌安全的，并且已经由DSP映射团队审查和批准。

* *[!UICONTROL Tier 1]:* 国家可识别的高级网站和应用程序。
* *[!UICONTROL Tier 2]:* 定位第1层，以及比第1层更不为人所知的高质量站点和应用程序。
* *[!UICONTROL Tier 3]:* 定位第1-2层，以及适合特定受众的合法且品牌安全的网站和应用程序。 使用第3层进行访问或数据定位购买。
* *[!UICONTROL All Sites]:* 目标层1-3和尚未筛选或分类的新库存，可用于访问。

>[!NOTE]
>
>库存特定于版面中的广告单位。

>[!TIP]
>
>对于效果促销活动，最佳做法是选择 *[!UICONTROL All Sites]*.

**[!UICONTROL Site Categories]:** (可选；可用时间 **[!UICONTROL Paste list of targeted sites]** is *[!UICONTROL Off]*)选定网站层中的网站类别，以包含或排除（但不同时排除）为目标。 从Advertising Cloud根据网站主题映射的垂直网站列表中进行选择：

1. 单击 ![编辑](/help/dsp/assets/edit.png).
1. 指定要包含或排除的网站类别：
   * 要包括网站类别，请执行以下操作：
      1. 单击 **[!UICONTROL Include categories]**.
      1. 选中每个要定位的类别旁边的复选框。
   * 要排除网站类别，请执行以下操作：
      1. 单击 **[!UICONTROL Exclude categories]**.
      1. 选中要排除的每个类别旁边的复选框。
1. （可选）要将包含定位信息的CSV文件下载到浏览器的下载位置，请单击 **[!UICONTROL Export]**.
1. 单击 **[!UICONTROL Save]**.

**[!UICONTROL Exclude Sites]:** (可选；可用时间 **[!UICONTROL Paste list of targeted sites]** is *[!UICONTROL Off]*)要排除的站点。 您可以搜索和选择站点，或输入或粘贴域名：

1. 单击 ![编辑](/help/dsp/assets/edit.png).
1. 指定站点：
   * 要搜索网站，请执行以下操作：
      1. 单击 **[!UICONTROL Search]**.
      1. 输入关键字、选择网站层和/或选择网站类别。
      1. 在搜索结果中，选择要排除的站点：
         * 要排除单个网站，请选中该网站旁边的复选框。
         * （当有50个以上的结果可用时）要排除前50个结果，请单击 **[!UICONTROL Exclude these 50]**. 要排除所有搜索结果，请单击 **[!UICONTROL Exclude these \<*NN *\>]**.
   * 要输入域名，请执行以下操作：
      1. 单击 **[!UICONTROL Paste]**.
      1. 在单独的行上输入一个或多个域名。
      1. 单击 **[!UICONTROL Exclude All]**.
1. 单击 **[!UICONTROL Done]** 等你完成。

>[!NOTE]
>
>* 除了Advertising Cloud DSP之外，还应用帐户级别和广告商级别的阻止网站列表 [全局阻止的站点列表](/help/dsp/introduction/features/brand-safety-media-quality.md)，包括被视为对广告不安全的网站。
>* 阻止的站点列表始终会覆盖目标站点列表。 如果版面同时排除和包含广告的相同目标，则会排除该目标。


**[!UICONTROL Language]:** （可选）要定位的单一语言。

**[!UICONTROL Site List Preview]:** （只读）用于版面的所有目标网站和阻止网站。

您可以选择将目标网站和阻止网站的列表导出为逗号分隔值(CSV)文件。 要导出列表，请单击 **[!UICONTROL Export full site list]**，然后根据浏览器的常规过程打开或保存文件。

<!-- **[!UICONTROL Allow unscreened sites]:** (XXX placements only) Allows you to XXXX.   Optional available for https://advertising.adobe.com/configurator/placement/edit/2432022 -->

**[!UICONTROL Paste list of targeted sites]:** 允许您仅定位特定站点。 启用此选项后，其他网站定位选项将被禁用。

**[!UICONTROL Sites]:** (在 **[!UICONTROL Paste list of targeted sites]** is *[!UICONTROL On]*)要定位的站点。 您可以搜索和选择站点，或输入或粘贴域名：

1. 单击 ![编辑](/help/dsp/assets/edit.png).
1. 指定站点：
   * 要搜索网站，请执行以下操作：
      1. 单击 **[!UICONTROL Search]**.
      1. 输入关键字、选择网站层和/或选择网站类别。
      1. 在搜索结果中，选择要包含的站点：
         * 要排除单个网站，请选中该网站旁边的复选框。
         * （当有超过50个结果可用时）要包含前50个结果，请单击 **[!UICONTROL Include these 50]**. 要包含所有搜索结果，请单击 **[!UICONTROL Include these \<*NN *\>]**.
   * 要输入域名，请执行以下操作：
      1. 单击 **[!UICONTROL Paste]**.
      1. 在单独的行上输入一个或多个域名。
      1. 单击 **[!UICONTROL Include All]**.
1. 单击 **[!UICONTROL Done]**.

## [!UICONTROL Audience Targeting]

**[!UICONTROL Included Audiences]:** 版面的任何受众目标，包括 [第三方区段、第一方区段、Adobe区段、自定义区段和保存的受众](/help/dsp/audiences/audience-settings.md). 此外，还将显示所有选定区段和已保存受众中已消除重复的受众总数和活动受众数量。 您可以选择现有受众、创建稍后可重复使用的新受众，或选择特定受众区段：

* 要选择现有受众，请单击 ![选择](/help/dsp/assets/chevron-down.png) 下一页 [!UICONTROL Included Audiences]，然后选择受众。
* 要创建新受众，请单击 ![选择](/help/dsp/assets/chevron-down.png) 下一页 [!UICONTROL Included Audiences]，然后选择 **[!UICONTROL + Create Audience]**. 有关说明，请参阅 [创建可重用受众](/help/dsp/audiences/reusable-audience-create.md)，从步骤3开始。
* 要选择特定受众区段，请单击 **[!UICONTROL Select segments for this placement only]**. 选择区段逻辑；有关说明，请参阅“[创建可重用受众](/help/dsp/audiences/reusable-audience-create.md).&quot; 完成后，单击 **保存**.

**[!UICONTROL Excluded Audiences]:** 要排除的版面受众，包括 [第三方区段、第一方区段、Adobe区段、自定义区段和保存的受众](/help/dsp/audiences/audience-settings.md). 此外，还将显示所有排除的受众中已消除重复的受众总数和活动受众数量。 您可以选择现有受众或创建新受众以供以后重复使用：

* 要选择现有受众，请单击 ![选择](/help/dsp/assets/chevron-down.png) 下一页 [!UICONTROL Excluded Audiences]，然后选择受众。
* 要创建新受众，请单击 ![选择](/help/dsp/assets/chevron-down.png) 下一页 [!UICONTROL Excluded Audiences]，然后选择 **+创建受众**. 有关说明，请参阅 [创建可重用受众](/help/dsp/audiences/reusable-audience-create.md)，从步骤3开始。

**[!UICONTROL Cross Device Targeting]:** (当您至少选择一个区段或受众，并且 [为基于人员的跨设备定位配置了营销活动](/help/dsp/campaign-management/campaigns/campaign-settings.md). 允许您扩展定位，涵盖人员的所有已知设备（根据促销活动设置中指定的设备图），甚至是不在指定区段中的设备。 根据为营销活动指定的图表，可能会收取费用。 设备图数据当前仅在北美地区可用。

**[!UICONTROL Placement Cap]:** （可选）独特设备或人员的次数(取决于指定的 [!UICONTROL Cross Device Level])将在投放中提供广告。 选项包括 *[!UICONTROL Unlimited]* 或每天、每周或每月的特定金额。

>[!NOTE]
>
> 您可以在营销活动、资源包和版面级别设置频率上限。 DSP将遵循营销活动层级中最严格的频率上限。

**[!UICONTROL Secondary Cap]:** (可选；当包含数字时可用 [!UICONTROL Placement Cap])主放置上限范围内的其他限制。 选择展示次数和时间段（例如每12小时3次）。

**[!UICONTROL Day Parting]:** （可选）在一周中的特定日期以及可能运行广告的时间。 要指定分时段间隔，请执行以下操作：
1. 单击 ![编辑](/help/dsp/assets/edit.png).
1. 选择适用的时区。
1. 指定间隔：
   * 要选择预设间隔，请单击其中一个间隔按钮。 选项包括*[!UICONTROL Weekends]**, *[!UICONTROL Weekdays]*, *[!UICONTROL Morning]*, *[!UICONTROL Lunch]*, *[!UICONTROL Dinner]*&#x200B;或 *[!UICONTROL Prime]* (primetime)。
   * 要手动选择间隔，请在单元格内单击，然后（可选）拖动以选择间隔。
1. 单击 **[!UICONTROL Save]**.

**[!UICONTROL Topic Targeting]:** (可选；可用于配置了 [!DNL Comscore] 和 [!DNL Grapeshot] 区段)特定区段名称或ID [!DNL Comscore] 和 [!DNL Grapeshot] 作为目标。 此功能可能需要额外付费。 要激活此功能并设置主题区段，请联系 [!DNL Adobe] 客户团队。

要指定主题定位，请执行以下操作：

1. 单击 ![编辑](/help/dsp/assets/edit.png).
1. 指定要定位的区段：
   1. 在左列中，选择合作伙伴(*[!UICONTROL Comscore]* 或 *[!UICONTROL Grapeshot]*)。
   1. 在输入字段中，输入区段名称或区段ID。
1. （可选）要将包含主题信息的CSV文件下载到浏览器的下载位置，请单击 **[!UICONTROL Export]**.
1. 单击 **[!UICONTROL Save]**.

>[!TIP]
>
>* 主题定位会限制版面可竞价的库存，因此，主题定位仅适用于整个购买量的一小部分。
>
>* 在的区段内设置任何负面定位 [!DNL Comscore] 或 [!DNL Grapeshot].


**[!UICONTROL Device Targeting]:** （可选）要包含和排除的特定设备信息，包括设备类型、制造商、操作系统、浏览器和连接类型。 要指定设备定位，请执行以下操作：

1. 单击 ![编辑](/help/dsp/assets/edit.png).
1. 指定要包含和排除的设备详细信息：
   1. 在左列中，选择类别。
   1. 指定定位：
      * 要包含值，请单击 **[!UICONTROL Include]** 值名称旁边的。
      * 要排除值，请单击 **[!UICONTROL Exclude]** 值名称旁边的。
1. （可选）要将包含设备定位信息的CSV文件下载到浏览器的下载位置，请单击 **[!UICONTROL Export]**.
1. 单击 **[!UICONTROL Save]**.

**[!UICONTROL ISP Targeting]:** （可选）特定互联网服务提供商(ISP)，可将其包括或排除（但不包括两者）作为目标。 要指定ISP定位，请执行以下操作：

1. 单击 ![编辑](/help/dsp/assets/edit.png).
1. 指定要包含或排除的ISP:
   * 要包括ISP，请执行以下操作：
      1. 单击 **[!UICONTROL Include ISPs]**.
      1. （可选）按关键字过滤列表。
      1. 选中每个要定位的ISP旁边的复选框。
   * 要排除ISP，请执行以下操作：
      1. 单击 **[!UICONTROL Exclude ISPs]**.
      1. （可选）按关键字过滤列表。
      1. 选中要排除的每个ISP旁边的复选框。
1. （可选）要将包含ISP定位信息的CSV文件下载到您浏览器的下载位置，请单击 **[!UICONTROL Export]**.
1. 单击 **[!UICONTROL Save]**.

## [!UICONTROL Brand Safety and Media Targeting]

**[!UICONTROL Contextual filtering]:** 类型 [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science]和 [!DNL Peer39] 要应用的上下文过滤器。 为新版面选择广告商级别的默认值，但您可以更改以下设置：

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block sites that are]:** （可选）默认情况下，要阻止的一种或多种类型的库存上下文。 可能需要支付额外费用。

* [!UICONTROL Peer 39]:

   * **定位以下站点：** （可选）默认情况下，要定位的一个或多个库存属性类型。 可能需要支付额外费用。

* [!UICONTROL ComScore]:

   * **阻止以下站点：** （可选）默认情况下，要阻止的一种或多种类型的库存属性。 可能需要支付额外费用。

* [!UICONTROL Integral Ad Science]

   * **[!UICONTROL Adult Content]:** （可选）默认情况下要阻止广告的成人内容的程度： *[!UICONTROL Do Not Block]* （默认）、 *[!UICONTROL Standard]*&#x200B;或 *[!UICONTROL Strict]*. 可能需要支付额外费用。

   * **[!UICONTROL Alcohol Content]:** （可选）默认情况下要阻止广告的酒精含量程度： *[!UICONTROL Do Not Block]* （默认）、 *[!UICONTROL Standard]*&#x200B;或 *[!UICONTROL Strict]*. 可能需要支付额外费用。

**[!UICONTROL Pre-bid fraud blocking]:** 基于通过测量的欺诈性流量和可疑活动而阻止的网站类型 [!DNL DoubleVerify], [!DNL Integral Ad Science]和 [!DNL Peer39]. 为新版面选择广告商级别的默认值，但您可以更改以下设置：

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** 默认情况下，会阻止所有新投放的100%无效流量，包括高速报文设备上的流量。 可能需要支付额外费用。

   * **[!UICONTROL Also block sites with]:** （可选）默认情况下，会导致DSP阻止广告的额外级别欺诈和无效流量：  *[!UICONTROL None]* （默认设置，不阻止其他流量）， *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]*&#x200B;或 *[!UICONTROL >25% Average Fraud/IVT levels]*. 可能需要支付额外费用。

* [!UICONTROL Peer 39]:

   * **[!UICONTROL Block sites that are]:** （可选）默认情况下，一种或多种类型的欺诈将导致DSP阻止广告： *[!UICONTROL Fraud]* （它阻止所有网站出现欺诈） *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]*&#x200B;和/或 *[!UICONTROL Fraud: Zero Ads]*. 可能需要支付额外费用。

* [!UICONTROL Integral Ad Science]:

   * **[!UICONTROL Block sites that are]:** （可选）默认导致DSP阻止广告的可疑网站或应用程序活动类型： *[!UICONTROL None]* （默认，不会基于可疑活动阻止广告）， *[!UICONTROL Suspicious Activity - High Risk]*&#x200B;或 *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. 可能需要支付额外费用。

**[!UICONTROL Ads.txt filtering]:**

哪个级别 [Ads.txt](https://iabtechlab.com/ads-txt-about/) 竞价前过滤，以便通过利用每个出版商的授权数字销售商列表来使用。 已为新版面选择广告商级别的默认设置，但您可以更改以下设置：

* *[!UICONTROL Opt out of ads.txt (default)]*:从所有卖家处购买库存。
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*:优先从域的授权直销商和转销商购买库存。
* *[!UICONTROL Ads.txt sellers only]*:仅向域的授权直销商和经销商购买库存。
* *[!UICONTROL Ads.txt sellers only]*:仅从域的授权直销商处购买库存。

**[!UICONTROL DoubleVerify Authentic Brand Safety]:** (使用 [!UICONTROL DoubleVerify Authentic Brand Safety] 选项)启用 [!DNL DoubleVerify Authentic Brand Safety]，使用为指定的区段ID配置的自定义品牌安全规则阻止投标后展示次数。 DSP会向您的帐户收取账单，以了解在广告商设置中指定的区段ID的使用情况。

## [!UICONTROL Tracking]

>[!NOTE]
>
>([!DNL Roku] 版面)经过批准的第三方跟踪供应商 [!DNL Roku] 包含 [!DNL Acxiom], [!DNL comScore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk]和 [!DNL Research Now].

**[!UICONTROL Event Pixels]:** （可选）默认附加到版面中所有新广告的第三方事件跟踪像素。 要指定事件像素，请执行以下操作：

1. 单击 ![编辑](/help/dsp/assets/edit.png).
1. 执行以下任一操作：
   * 要选择现有像素，请选中像素行中的复选框。
   * 要创建新像素，请执行以下操作：
      1. 单击 **[!UICONTROL Create]**.
      1. 输入以下信息：
         * **[!UICONTROL Pixel name]:** 像素名称；最大长度为500个字符。 使用有助于您轻松识别像素的名称。
         * **[!UICONTROL Pixel event fires on]:** 触发像素的事件。 可用事件因广告类型而异。
         * **[!UICONTROL Pixel type]:** 像素是否为 *[!UICONTROL IMG URL]* （1x1像素图像文件）， *[!UICONTROL HTML]*&#x200B;或 *[!UICONTROL JavaScript URL]*.
         * **[!UICONTROL Pixel URL]:** 像素图像的URL。
      1. 单击 **[!UICONTROL Create and attach]**.
   1. 单击 **[!UICONTROL Save]**.

**[!UICONTROL Conversion Pixels]:** （可选）默认情况下将附加到版面中所有新广告的转化跟踪像素。 要指定转换像素：

1. 单击 ![编辑](/help/dsp/assets/edit.png).
1. 执行以下任一操作：
   * 要选择现有像素，请选中像素行中的复选框。
   * 要创建新像素，请执行以下操作：
      1. 单击 **[!UICONTROL Create]**.
      1. 输入以下信息：
         * **[!UICONTROL Conversion pixel name]:** 像素名称；最大长度为500个字符。 使用有助于您轻松识别像素的名称。
         * **[!UICONTROL Conversion category]:** 转化的类型。
         * **[!UICONTROL Impression conversion window]:** 广告展示后可将展示归因于转化的天数。 默认为30天。
         * **[!UICONTROL Click conversion window]:** 广告点击后，点击可归因于转化的天数。 默认为30天。
         * **[!UICONTROL Notes]:** （可选）有关像素的描述或其他信息。
      1. 单击 **[!UICONTROL Create and attach]**.
      1. 在相关网页上实施转换像素：
         1. 在主菜单中，转到 **[!UICONTROL Resources]>[!UICONTROL Conversion pixels]**.
         1. 在像素行中，单击 **[!UICONTROL edit]**.
         1. 复制 [!UICONTROL HTML Tag] 和 [!UICONTROL Flash Tag] 字段，以便向广告商或网站联系人提供。

            广告商的IT部门或其他组可能需要安排或告知标记部署。
   1. 单击 **[!UICONTROL Save]**.

**[!UICONTROL 3rd-party Fees]:** （可选）要作为每千次展示次数不可计费成本进行跟踪的第三方静态费用率。 除非您输入其他值，否则在适用时，将自动为新版面应用包级别的默认值。

>[!NOTE]
>
>计费费用反映在 [!UICONTROL Net CPM] 量度。

>[!MORELIKETHIS]
>
>* [关于版面管理](placement-about.md)
>* [创建版面](placement-create.md)
>* [编辑版面](placement-edit.md)
>* [键盘快捷键](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [关于Campaign Management的常见问题解答](/help/dsp/campaign-management/campaign-management-faq.md)

