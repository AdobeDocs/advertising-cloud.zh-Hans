---
title: 自定义报表设置
description: 请参阅自定义报表设置的描述。
feature: DSP Custom Reports
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '966'
ht-degree: 0%

---

# 自定义报表设置

**[!UICONTROL Name]** 报表名称。 最大长度为180个字符。

**[!UICONTROL Report Type]** 报表类型： *[!UICONTROL Custom]* （其中包括大多数可用选项）， *[!UICONTROL Billing]*, *[!UICONTROL Conversion]*, *[!UICONTROL Device]*, *[!UICONTROL Frequency (by Impression)]*,  *[!UICONTROL Frequency (by App/Site)]*, *[!UICONTROL Geo]*, *[!UICONTROL Margin]*, *[!UICONTROL Media Performance]*,  *[!UICONTROL Segment]*&#x200B;或 *[!UICONTROL Site]*.

## [!UICONTROL Apply Filters] 区域

**[!UICONTROL Timezone]:** 报告时区。

**[!UICONTROL Observe Daylight Savings Time]:** 将夏令时视为报告时间。

**\[日期范围\]:** 要生成数据的日期范围。 可用的天数因报表和所选维度而异。 选择一个：

* **[!UICONTROL Previous N days]:** 包括今天之前特定天数的数据。

* **[!UICONTROL Custom]:** 包括特定开始日期和结束日期之间的数据。 要报告前一天的数据，请选择 **[!UICONTROL Present]**.

* **[!UICONTROL Last Calendar Month]:** 包括上一个日历月的数据。

**[!UICONTROL Add Filters]:** （可选）用于过滤数据的其他维度，无论这些维度是否作为列包含在报表中： *[!UICONTROL Account]*,\* *[!UICONTROL Advertiser]*, *[!UICONTROL Campaign]*, *[!UICONTROL Placement]*, *[!UICONTROL Ad]*, *[!UICONTROL Ad Type]*, *[!UICONTROL Video]*, *[!UICONTROL Video Duration]*, *[!UICONTROL Country]*&#x200B;和 *[!UICONTROL Package]*.

\* *[!UICONTROL Account]* 仅当贵组织在 [跨帐户报告](report-about.md#cross-account-reporting):  [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)]和 [!UICONTROL Conversion]. 联系您的 [!DNL Adobe] 帐户团队以了解有关跨帐户报告的更多信息。

要应用一个或多个过滤器，请执行以下操作：

* 选择维，选择运算符(*等于* 或 *不等于*)，然后选择适用的值。 例如，要仅返回前置广告的数据，请指定“[!UICONTROL Ad Type equals Preroll].&quot;
* （可选）向过滤器添加其他标准。
* （可选）添加其他过滤器，每个过滤器具有一个或多个标准。

## [!UICONTROL Build Your Report] 区域

**[!UICONTROL Select To Add As Report Headers]:**  要包含在报表中的数据列或标题。 要添加列，请展开类别，然后选中列名称旁边的复选框。 所有不可用的量度均被禁用。 可用的数据类别包括：

* [!UICONTROL  Dimensions]
* [!UICONTROL Metrics]
* [!UICONTROL Conversion Metrics] （按广告商排序）
* [!UICONTROL Custom Goals] （按广告商排序）

**[!UICONTROL Drag to Re-Order Report Headers Below]:** 列标题的顺序。 您可以拖放任何列以自定义顺序。

## [!UICONTROL Multi-Touch Conversion Options] 区域

**[!UICONTROL Format]:** 是否在中生成报表 *[!UICONTROL CSV]* （逗号分隔值）或 *[!UICONTROL Tab]* （制表符分隔值）格式。

**[!UICONTROL Report Headers]:** 是否 *[!UICONTROL Include]* 或 *[!UICONTROL Do Not Include]* 列标题。

**[!UICONTROL Attribution Rule Settings]:** (全部 [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment]和 [!UICONTROL Site] 报告 [!UICONTROL Conversion Metrics] 或 [!UICONTROL Custom Goals] 列；仅具有Adobe广告转化跟踪的广告商)在报表中，如何将转化数据归因于一系列可导致转化的事件。 如果要比较规则之间的差异，可以选择多个规则。

>[!NOTE]
>
>转化路径包括广告商展示次数或点击回顾窗口中的任何展示次数和点击次数，这些窗口在 [!DNL Adobe Advertising Search]. 在转化归因期间，点击次数会优先于展示次数。 转化路径中的任何点击都会根据归因规则获得全部点数。 只有在转化路径中未跟踪任何点击量时，展示次数才会获得点数。

* *[!UICONTROL Last Event]:* 将转化归因到转化路径中的最后一次点击或展示。

* *[!UICONTROL Weight Last More]:* 将转化归因到转化路径中的所有事件，但对最后一个事件赋予的权重最大，对前一个事件的权重依次减小。

* *[!UICONTROL Even Distribution]:* 对转化路径中每个事件的转化进行同等的属性。

* *[!UICONTROL Weight First More]:* 将转化归因到转化路径中的所有事件，但赋予第一个事件最大的权重，并相继减少对以下事件的权重。

* *[!UICONTROL First Event]:* 将转化归因于转化路径中的首次点击或展示。

* *[!UICONTROL U-shaped]:* 将转化归因于转化路径中的所有事件，但将最大权重赋予第一个和最后一个事件，并相继减少了转化路径中间事件的权重。

* *[!UICONTROL Display Only]:*  将转化归因到转化路径中最后一次DSP点击或展示。 这包括视频和连接的电视广告，不包括 [!DNL Adobe Advertising Search] 广告。

* *[!UICONTROL Social Only]:* 过时

<!-- See also [How Attribution Rules Are Calculated for Adobe Advertising](). -->

**[!UICONTROL Paths as Columns]:**  (全部 [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment]和 [!UICONTROL Site] 报告 [!UICONTROL Conversion Metrics] 或 [!UICONTROL Custom Goals] 列)在同一设备上发生先前事件时要报告的转化类型。 您最多可以包含三种类型。 对于每个选定的类型，每个转化量度都包含一个单独的列，并附加指定的后缀([!UICONTROL (tl)], [!UICONTROL (ct)]或 [!UICONTROL (vt)]):

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* 包括归因于点击量（点进为CT）和展示次数（显示到达为VT）的转化。 归因于展示次数的转化次数乘以指定的显示到达权重。 默认的显示到达权重为100%，这意味着归因于展示次数的转化将被计为归因于点击次数的转化值的100%。

* *[!UICONTROL With Clicks (CT)]:* 仅包括归因于点击的转化。

* *[!UICONTROL Impressions Only (VT)]:* 仅包括归因于展示次数的转化，因为转化路径中未跟踪任何点击。

**[!UICONTROL Conversion Reporting Based On]:**  如何报告转化数据：

* *[!UICONTROL Conversion Timestamp]:* （默认）转化将与转化日期关联。

* *[!UICONTROL Event Timestamp]:* 将根据导致转化的展示或点击日期(由指定的 [!UICONTROL Attribution Rule Settings].

## [!UICONTROL Add Report Destinations] 区域

**[!UICONTROL Destination Type]:** 选择以下目标类型之一：

* *[!UICONTROL S3]:* 将完成的报表发送到一个或多个 [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3])位置，您将在 **[!UICONTROL Destination Name]** 字段。
* *[!UICONTROL sFTP]:* 要将完成的报表发送到一个或多个SFTP位置，您将在 **[!UICONTROL Destination Name]** 字段。
* *[!UICONTROL FTP]:* 要将完成的报表发送到一个或多个FTP位置，您将在 **[!UICONTROL Destination Name]** 字段。
* *[!UICONTROL FTP SSL]（目前为测试版）：* 要将完成的报表发送到一个或多个FTP SSL位置，您将在 **[!UICONTROL Destination Name]** 字段。
* *[!UICONTROL Email]:* 指定在由于错误而取消报表时将已完成的报表或通知发送到的电子邮件地址。 要指定多个地址，请用逗号或空格将它们分隔开。

>[!NOTE]
>
> 保存报表后，便无法更改目标类型。

**[!UICONTROL Destination Name]:** （仅限S3、FTP、sFTP和FTP SSL目标类型）将自定义报表发送到的报表目标的名称。

* 要指定现有目标，请从列表中选择目标名称。 您可以单独选择多个目标名称。

* 要创建新目标，请执行以下操作：

   1. 单击 **添加新目标**.

   1. 输入 [报告目标设置](/help/dsp/reports/report-destinations/report-destination-settings.md)，然后单击 **保存**.

   1. 返回报表设置，单击 **刷新目标名称。**

      现在，新目标可从现有目标列表中获取，您可以选择将其添加到报表。

**[!UICONTROL Frequency]:** (对于 [!UICONTROL Destination Name] 多久将报表发送到一次目标： *[!UICONTROL Once]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*&#x200B;或 *[!UICONTROL Monthly]*.

## [!UICONTROL Save Report] 区域

**[!UICONTROL Send & Save]:** 何时发送报表： *[!UICONTROL On Schedule]* 或 *[!UICONTROL Run Now]*. 计划报表将在帐户时区的09:00之前提交。

>[!NOTE]
>
>您可以 [随时运行自定义报表](report-run-now.md) 从 [!UICONTROL Reports] 中。

>[!MORELIKETHIS]
>
>* [关于自定义报表](/help/dsp/reports/report-about.md)
>* [创建自定义报表](/help/dsp/reports/report-create.md)
>* [复制自定义报表](/help/dsp/reports/report-copy.md)
>* [编辑自定义报表](/help/dsp/reports/report-edit.md)
>* [运行自定义报表](/help/dsp/reports/report-run-now.md)
>* [自定义报表设置](/help/dsp/reports/report-settings.md)
>* [关于报表目标](/help/dsp/reports/report-destinations/report-destination-about.md)

* [可用报表列](/help/dsp/reports/report-columns.md)
