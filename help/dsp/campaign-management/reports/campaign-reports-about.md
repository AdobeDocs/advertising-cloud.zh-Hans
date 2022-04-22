---
title: 关于平台内报表
description: 了解营销活动管理视图中包含的报表数据。
feature: DSP Campaign Data Views
exl-id: e9f7dafe-e0db-4fec-bf5b-858cbcfdde45
source-git-commit: 7d081583ff10675b515aafdd97ccb3053f19c32d
workflow-type: tm+mt
source-wordcount: '938'
ht-degree: 0%

---

# 关于平台内报表

<!-- rename "About Performance Reports in Campaign Management Views?" -->
营销活动管理视图包含全面的报表数据。 可用报表可帮助您识别性能良好的包和版面，以及需要您注意的包和版面。 快速操作按钮还可提高工作效率。

## 所有营销活动视图

的 [!UICONTROL Campaigns] 查看打开一组性能数据图表以及您帐户中所有营销活动的列表。

### 图表视图 {#chart-view}

您可以 [自定义时间系列趋势图](campaign-data-visualization-manage.md) 使用三个量度跨所有营销活动。 默认情况下， [!UICONTROL Net Spend], [!UICONTROL Impressions]和 [!UICONTROL Net CPM] 包含在单独的图表（网格图）中。 您可以选择更改量度。 要在时间系列趋势图中启用每小时数据，请将日期选择更改为一天([!UICONTROL Today], [!UICONTROL Yesterday]或特定日期)。

![三个量度的单独趋势图](/help/dsp/assets/trend-chart-separate.png)

您还可以选择覆盖这三个量度，以便轻松检测异常和提高规模或性能的区域。

![带有叠加图的趋势图](/help/dsp/assets/trend-chart.png)

### 表视图

![营销活动列表](/help/dsp/assets/campaigns-list.png)

默认情况下，每个促销活动行都包含步调和投放量度。 步调量度包括 [!UICONTROL Gross Spend (Lifetime)]，该量度包括营销活动中所有资源包的实际目标支出与预期目标支出的量度，以便您一目了然地识别效果不佳的营销活动。 您可以选择 [更改列视图](column-view-change.md) 或 [创建自定义列视图](column-view-create.md).

您可以进一步 [自定义数据表](campaign-data-views-about.md) 以其他方式和方式 [过滤可见数据](campaign-data-filter.md).

要查看营销活动的详细信息，请单击营销活动名称。

## 单个营销活动报告 {#single-campaign-reporting}

在营销活动中，您可以根据营销活动实体过滤数据： [!UICONTROL Packages], [!UICONTROL Placements]和 [!UICONTROL Ads]. 您可以进一步 [过滤可见数据](campaign-data-filter.md) 以仅包含您想要查看的包、版面或广告。

![促销活动实体选项卡](/help/dsp/assets/campaign-subtabs.png)

### 图表视图

对于每个营销活动，您可以 [自定义时间系列趋势图](campaign-data-visualization-manage.md) 包含三个量度，每个实体视图中均提供这些量度。 营销活动的所有趋势图中都会保留相同的量度。

请参阅 [关于跨促销活动量度的“图表视图”部分](#chart-view) 以了解更多信息。

### 表视图

在每个实体选项卡中，每行默认包含步调和投放量度，但您可以 [更改列视图](column-view-change.md) 或 [创建自定义列视图](column-view-create.md) 以应用于营销活动的所有子选项卡。 您可以进一步 [自定义数据表](campaign-data-views-about.md) 以其他方式。 每个数据表都包括 [!UICONTROL Subtotals] 行，显示所有可见行中每个量度的总和或平均值。

### 版面 [!UICONTROL Inspector] {#placement-inspector}

对于每个版面，您可以 [打开（详细信息视图） [!UICONTROL Inspector])](placement-details-view.md)，其中包括以下深入数据：

* **[!UICONTROL Sites]:** 版面具有展示次数的所有网站。

   的 [!UICONTROL Sites] 选项卡包含搜索和过滤功能、主页上提供的相同标准和自定义列视图选项，以及 [!UICONTROL Exclude] 按钮，以便您能够快速从版面中排除网站。

* **[!UICONTROL Ads]:** 版面中的所有广告。

   的 [!UICONTROL Ads] 选项卡包含搜索和过滤功能、主页上提供的相同标准和自定义列视图选项以及每行中的快速操作按钮，如 [!UICONTROL Pause] （以便您可以快速暂停广告）。

* **[!UICONTROL Frequency]:** 投放的每个广告频度级别的数据，包括：
   * 广告频度级别（如“1”，表示用户曾查看过广告的所有实例）
   * 设备/浏览器或人员的预计独特数量(取决于指定的 [!UICONTROL Cross Device Level] （在指定频度级别接收展示次数）
   * 在指定频率级别的预计展示次数
   * 指定频率级别的估计平均频率。 此值等于（预计展示次数）/（预计独特数）。

* **[!UICONTROL Inventory]:** 有关投放所定向的所有交易的信息。

   的 [!UICONTROL Inventory] 选项卡包含搜索和过滤功能、主页上提供的相同标准和自定义列视图选项以及每行中的快速操作按钮，如 [!UICONTROL Edit] 和 [!UICONTROL View Report]. 的 [!UICONTROL Inventory] 选项卡，可通过显示性能统计信息(如 [!UICONTROL Auctions], [!UICONTROL Bids]和 [!UICONTROL Win Rate].

#### 清单疑难解答

| 问题 | 可能的原因 | 要采取的操作 |
| -----------| ---------- | ---------- |
| [!UICONTROL Zero Auctions] | 发布者尚未开始发送竞价请求。 | 联系发布者以激活交易。 |
|  | 交易设置不正确，例如输入了不正确的外部交易ID。 | 确认交易详细信息并编辑交易。 |
| [!UICONTROL Auctions but no Bids] | 版面定位与交易的传入竞价请求不匹配。 <br><br> 例如，版面可能会定位不符合交易条件的地理位置。 | 根据需要编辑版面定位以避免定位不匹配。 |
|  | 投放没有具有交易所需媒体类型的活动广告。 | 创建具有正确媒体类型的广告并将其附加到投放。 |
|  | 这个职位没有足够的预算。 | 增加投放预算，以允许对传入的请求进行竞价。 |
|  | 版面投放日期与交易的展示投放日期不重叠。 | 根据需要编辑版面的投放日期。 |
| [!UICONTROL Low Win Rate] | 配售的最高出价（下限或固定）低于交易所要求的最低价。 | 增加投放 [!UICONTROL Max Bid] 根据需要。 |
|  | 版面使用限制竞价的预竞价过滤器。 | 降低投标前过滤器的阈值以允许进行更多投标。 |
|  | 投放的受众定位限制过大。 | 检查指定的受众目标是否具有足够的活动用户，并尽可能展开受众。 |

![版面检查器](/help/dsp/assets/placement-inspector.png)

您可以在 [!UICONTROL Sites], [!UICONTROL Ads]或 [!UICONTROL Frequency] 选项卡，以XLSM格式的报表形式显示浏览器的默认下载文件夹。

### 营销活动级别的其他报表类型

对于其他数据划分，请查看 [营销活动级别的报告页面](/help/dsp/campaign-management/campaigns/campaign-view-report.md). 的 <!--legacy --> 报表包含 [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability]和 [!UICONTROL Audience Performance] 数据。

>[!MORELIKETHIS]
>
>* [查看版面的网站、广告和频度详细信息](placement-details-view.md)
>* [关于Campaign数据视图](campaign-data-views-about.md)
>* [创建自定义列视图](column-view-create.md)
>* [更改列视图](column-view-change.md)
>* [管理数据可视化图表](campaign-data-visualization-manage.md)
>* [从Campaign Management视图导出数据](campaign-export-data.md)
>* [查看营销活动的详细报表](/help/dsp/campaign-management/campaigns/campaign-view-report.md)

