---
title: 自定义报表设置
description: 请参阅自定义报表设置的描述。
feature: Custom Reports
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# 自定义报表设置

**[!UICONTROL Name]** 报表名称。最大长度为180个字符。

**[!UICONTROL Report Type]** 报表类型： *[!UICONTROL Custom]* （包括大多数可用选项）、  *[!UICONTROL Billing]*、  *[!UICONTROL Conversion]*、  *[!UICONTROL Device]*、  *[!UICONTROL Frequency (by Impression)]*、   *[!UICONTROL Frequency (by App/Site)]*、  *[!UICONTROL Geo]*、  *[!UICONTROL Margin]*、  *[!UICONTROL Media Performance]*&#x200B;或  *[!UICONTROL Segment]* *[!UICONTROL Site]*。

## [!UICONTROL Apply Filters] 区域

**[!UICONTROL Timezone]:** 报告的时区。

**[!UICONTROL Observe Daylight Savings Time]:** 将夏令时视为报告时间。

**\[日期范围\]:** 要为其生成数据的日期范围。可用的天数因报表和所选维度而异。 选择一个：

* **[!UICONTROL Previous N days]:** 包含今天之前特定天数的数据。

* **[!UICONTROL Custom]:** 包含特定开始日期和结束日期之间的数据。要报告前一天的数据，请选择&#x200B;**[!UICONTROL Present]**。

* **[!UICONTROL Last Calendar Month]:** 包含上一个日历月的数据。

**[!UICONTROL Add Filters]:** （可选）用于筛选数据的其他维度，无论这些维度是否作为列包含在报表中： *[!UICONTROL Account]*、\*  *[!UICONTROL Advertiser]*、  *[!UICONTROL Campaign]*、  *[!UICONTROL Placement]*、  *[!UICONTROL Ad]*、  *[!UICONTROL Ad Type]*、  *[!UICONTROL Video]*、  *[!UICONTROL Video Duration]*、  *[!UICONTROL Country]*&#x200B;和 *[!UICONTROL Package]*。

\* *[!UICONTROL Account]*&#x200B;仅当贵组织配置了[跨帐户报告](report-about.md#cross-account-reporting)时，才可用于以下报表类型： [!UICONTROL Custom]、[!UICONTROL Site]、[!UICONTROL Segment]、[!UICONTROL Geo]、[!UICONTROL Device]、[!UICONTROL Frequency (by Impression)]和[!UICONTROL Conversion]。 请联系您的Adobe客户经理，以了解有关跨帐户报告的更多信息。

要应用一个或多个过滤器，请执行以下操作：

* 选择一个维度，选择运算符（*等于*&#x200B;或&#x200B;*不等于*），然后选择适用的值。 例如，要仅返回前置广告的数据，请指定“[!UICONTROL Ad Type equals Preroll]”。
* （可选）向过滤器添加其他标准。
* （可选）添加其他过滤器，每个过滤器具有一个或多个标准。

## [!UICONTROL Build Your Report] 区域

**[!UICONTROL Select To Add As Report Headers]:**  要包含在报表中的数据列或标题。要添加列，请展开类别，然后选中列名称旁边的复选框。 所有不可用的量度均被禁用。 可用的数据类别包括：

* [!UICONTROL  Dimensions]
* [!UICONTROL Metrics]
* [!UICONTROL Conversion Metrics] （按广告商排序）
* [!UICONTROL Custom Goals] （按广告商排序）

**[!UICONTROL Drag to Re-Order Report Headers Below]:** 列标题的顺序。您可以拖放任何列以自定义顺序。

## [!UICONTROL Multi-Touch Conversion Options] 区域

**[!UICONTROL Format]:** 是以(逗号分 *[!UICONTROL CSV]* 隔值)还是(制 *[!UICONTROL Tab]* 表符分隔值)格式生成报表。

**[!UICONTROL Report Headers]:** 是列 *[!UICONTROL Include]* 标 *[!UICONTROL Do Not Include]* 题还是列标题。

**[!UICONTROL Attribution Rule Settings]:** (包含 [!UICONTROL Custom] [!UICONTROL Conversion]或 [!UICONTROL Device] [!UICONTROL Geo]列的所有 [!UICONTROL Segment]、 [!UICONTROL Site] 、 [!UICONTROL Conversion Metrics] 、 [!UICONTROL Custom Goals] 和报表);仅具有Advertising Cloud转化跟踪的广告商)在报表中，如何将转化数据归因于一系列可导致转化的事件。如果要比较规则之间的差异，可以选择多个规则。

>[!NOTE]
>
>转化路径包括广告商展示次数或点击回顾窗口中的任何展示次数和点击次数，这些窗口是在Advertising Cloud Search中配置的。 在转化归因期间，点击次数会优先于展示次数。 转化路径中的任何点击都会根据归因规则获得全部点数。 只有在转化路径中未跟踪任何点击量时，展示次数才会获得点数。

* *[!UICONTROL Last Event]:* 将转化归因到转化路径中的最后一次点击或展示。

* *[!UICONTROL Weight Last More]:* 将转化归因于转化路径中的所有事件，但赋予最后一个事件的最大权重，并相继减少对前一事件的权重。

* *[!UICONTROL Even Distribution]:* 对转化路径中每个事件的转化进行同等的属性。

* *[!UICONTROL Weight First More]:* 将转化归因于转化路径中的所有事件，但赋予第一个事件最大的权重，并相继减少对以下事件的权重。

* *[!UICONTROL First Event]:* 将转化归因于转化路径中的首次点击或展示。

* *[!UICONTROL U-shaped]:* 将转化归因于转化路径中的所有事件，但将最大权重赋予第一个事件和最后一个事件，并依次减轻转化路径中间事件的权重。

* *[!UICONTROL Display Only]:*  将转化归因于转化路径中最后一次DSP点击或展示。这包括视频和连接的电视广告，不包括对Advertising Cloud Search广告的点击。

* *[!UICONTROL Social Only]:* 已过时

<!-- See also [How Attribution Rules Are Calculated for Adobe Advertising Cloud](). -->

**[!UICONTROL Paths as Columns]:**  (包含 [!UICONTROL Custom] [!UICONTROL Conversion]或 [!UICONTROL Device]列的 [!UICONTROL Geo]、 [!UICONTROL Segment]、 [!UICONTROL Site]  [!UICONTROL Conversion Metrics] 和报表)在同 [!UICONTROL Custom Goals] 一设备上发生先前事件时要报告的转化类型。您最多可以包含三种类型。 对于每个选定的类型，每个转化量度都包含单独的列，并附加指定的后缀（[!UICONTROL (tl)]、[!UICONTROL (ct)]或[!UICONTROL (vt)]）：

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* 包括归因于点击（点进为CT）和展示（显示到达为VT）的转化。归因于展示次数的转化次数乘以指定的显示到达权重。 默认的显示到达权重为100%，这意味着归因于展示次数的转化将被计为归因于点击次数的转化值的100%。

* *[!UICONTROL With Clicks (CT)]:* 仅包含归因于点击的转化。

* *[!UICONTROL Impressions Only (VT)]:* 仅包含归因于展示次数的转化，因为转化路径中未跟踪任何点击。

**[!UICONTROL Cross Device Level]:**  (包含 [!UICONTROL Custom] [!UICONTROL Conversion]或 [!UICONTROL Device] [!UICONTROL Geo]列的所有 [!UICONTROL Segment]、 [!UICONTROL Site] 、 [!UICONTROL Conversion Metrics] 、 [!UICONTROL Custom Goals] 和报表);仅适用于具有跨设备归因的广告商)跟踪转化的级别： *[!UICONTROL People]* 或 *[!UICONTROL Household]*。

了解有关[跨设备解决方案](/help/dsp/introduction/features/cross-device-solutions.md)的更多信息。

**[!UICONTROL Cross-Device Breakout]:** (包含 [!UICONTROL Custom] [!UICONTROL Conversion]或 [!UICONTROL Device] [!UICONTROL Geo]列的所有 [!UICONTROL Segment]、 [!UICONTROL Site] 、 [!UICONTROL Conversion Metrics] 、 [!UICONTROL Custom Goals] 和报表);仅适用于具有跨设备归因的广告商)要包含在报表中的有关跨设备转化的详细信息级别。如果您想要详细的分组讨论，最多可以选择三个级别，每个级别都将包含在单独的列中。

* *[!UICONTROL Total People (TP)]:* 包括总转化，包括相同设备转化和跨设备转化（如果适用）。在报表中，“[!UICONTROL (tp)]”会附加到转化量度名称和规则类型中。

* *[!UICONTROL Same Device (SD)]:* 仅包含转化路径中仅跟踪了单个设备的转化。在报表中，“[!UICONTROL (sd)]”会附加到转化量度名称和规则类型中。

* *[!UICONTROL Cross Device (XD)]:* 仅包含转化路径中跟踪了多个设备的转化。在报表中，“[!UICONTROL (xd)]”会附加到转化量度名称和规则类型中。

**[!UICONTROL Conversion Reporting Based On]:**  如何报告转化数据：

* *[!UICONTROL Conversion Timestamp]:* （默认）转化将与转化日期关联。

* *[!UICONTROL Event Timestamp]:* 将根据导致转化的展示或点击日期（由指定的确定）报告转化 [!UICONTROL Attribution Rule Settings]。

## [!UICONTROL Add Email Recipients] 区域

**[!UICONTROL Email]:** 如果由于错误而取消了报表，则要将已完成的报表或通知发送到的电子邮件地址。要指定多个地址，请用逗号或空格将它们分隔开。

**[!UICONTROL Frequency]:** 多久发送一次报表： *[!UICONTROL Once]*、  *[!UICONTROL Daily]*、  *[!UICONTROL Weekly]*&#x200B;或 *[!UICONTROL Monthly]*。

## [!UICONTROL Save Report] 区域

**[!UICONTROL Send & Save]:** 何时发送报表： *[!UICONTROL On Schedule]* 或 *[!UICONTROL Run Now]*。计划报表将在帐户时区的09:00之前提交。

>[!NOTE]
>
>您可以从[!UICONTROL Reports]视图随时](report-run-now.md)运行自定义报表。[

>[!MORELIKETHIS]
>
>* [关于自定义报表](/help/dsp/reports/report-about.md)
>* [创建自定义报表](/help/dsp/reports/report-create.md)
>* [复制自定义报表](/help/dsp/reports/report-copy.md)
>* [编辑自定义报表](/help/dsp/reports/report-edit.md)
>* [运行自定义报表](/help/dsp/reports/report-run-now.md)
>* [自定义报表设置](/help/dsp/reports/report-settings.md)

* [可用报表列](/help/dsp/reports/report-columns.md)
