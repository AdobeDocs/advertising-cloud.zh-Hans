---
title: 概述 [!DNL Analytics for Advertising]
description: 概述 [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '1076'
ht-degree: 0%

---

# 概述 [!DNL Analytics for Advertising]

*使用Advertising DSP和[!DNL Advertising Search]*

[!DNL Analytics for Advertising] 集成了Adobe Analytics和Adobe广告，以扩展和增强每个产品的功能。

该集成允许广告商跟踪其网站中的点进和显示到达交互 [!DNL Analytics] 例如，允许品牌了解其广告支出如何促进网站参与和关键业务目标。

此外，Adobe广告还可以访问大量的第一方数据， [!DNL Analytics] 收集 [!DNL Analytics] 网站上已有的标记。 这样可以提供更强大的历程管理、第一方再营销和付费媒体网站报告功能。 Adobe广告可进一步使用 [!DNL Analytics] 用于支出和竞价优化的数据。

如果适当使用， [!DNL Analytics for Advertising] 模糊两种传统角色之间的界限：广告历程管理（通过广告将用户发送到网站的操作），并通过web分析了解该网站的参与度。

主要优势：

* 发送 [!DNL Analytics] 区段直接Adobe广告以进行第一方网站再营销。
* 使用 [!DNL Analytics] 自定义事件和标准事件作为转化信号，用于优化付费媒体广告。
* 利用 [!DNL Analytics] Analysis Workspace以更好地了解网站的入口点和访问行为。
* 实现Web分析人员与付费媒体团队之间更密切的协作。
* 在中使用永久性Adobe广告显示到达和点进ID [!DNL Analytics] 了解网站参与度。
* 使用自定义量度、自定义维度和网站活动增强Analysis Workspace中的传统付费媒体报表，在将数据或像素导出到广告服务器或其他DSP时，这些量度或维度无法实现。
* 利用 [!DNL Analytics] 网站上已有用于在Adobe广告中跟踪和优化的代码。

>[!TIP]
>
> 观看 [视频简介 [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html?lang=en#analytics).

## 使用Analytics进行付费媒体报告

[!DNL Analytics for Advertising] 通过允许您：

* 在中使用永久性Adobe广告显示到达和点进ID [!DNL Analytics] 了解网站参与度。
* 利用Analysis Workspace更好地了解网站的入口点和访问行为。 您可以访问付费媒体维度和事件数据，包括Adobe广告促销活动实体名称（精确到版面和广告）及其关联量度，如点击量、展示次数和成本。

使用 [!DNL Analytics] 作为您的付费媒体报告工具，您的组织需要Experience Cloud登录才能访问Analysis Workspace。 您的Adobe广告团队将帮助您将Adobe广告数据映射到Analysis Workspace中的各个报表包。 您可以将Adobe广告数据发送到任何报表包，但您应该了解已映射到Adobe广告的报表包以及未映射的报表包。根据报表包的不同，这可能会更改报告的数据。

[Adobe广告ID(位于 [!DNL Analytics]](ids.md) 与其他eVar类似，具有自定义的永久过期时间。 默认情况下，归因回顾窗口会在Adobe广告实施期间设置为60天。 要更改此设置，请使用 [!DNL Adobe] 客户团队。

Adobe广告维度会附加后缀“(AMO ID)”(例如“广告类型(AMO ID)”)。 请参阅“[Adobe广告量度在Analysis Workspace中](advertising-metrics-in-analytics.md)“ ”，以查看可用维度的列表。

>[!NOTE]
>
> 在中查看Adobe广告数据（或任何数据集）时 [!DNL Analytics]，请注意，量度和报表基于 [!DNL Analytics]. 数据可能与您在其他报表系统（如广告服务器报表）中看到的数据不同。 [!DNL DSP] 报表或搜索引擎报表。 要了解 [!DNL Analytics]，您需要了解eVar数据何时过期、定义访问的内容、最近联系归因与总保留归因之间的关系，以及其他因素。 有关更多信息，请参阅 [之间的预期数据差异 [!DNL Analytics] 和Adobe广告](data-variances.md).

## 使用Analytics增强Adobe广告促销活动和Portfolio

无需任何额外像素， [!DNL Analytics for Advertising] 通过向Adobe广告发送两个主要信号，可以更好地优化受众并简化受众分段：

* 用作竞价信号的转化量度：
   * 标准量度，例如 [!UICONTROL Revenue] 和 [!UICONTROL Cart Views].
   * 网站参与量度，如页面查看和访问量度。
   * 自定义收入量度。
   * 保留的收入量度。
* 在中创建的区段 [!DNL Analytics] 和发布到Experience Cloud。

   您可以使用 [!DNL Analytics] 区段，用于 [!DNL DSP] 和付费搜索广告。

   ([!DNL Search] （仅限）具有 [!DNL Analytics] 但是，不能Audience Manager也可以从中创建Google网站基于标签的受众（再营销列表）和客户匹配受众（客户列表） [!DNL Analytics] 与Experience Cloud共享的区段。

### 网站转化量度作为竞价信号

您可以从 [!DNL Analytics] 以在Adobe广告中构建加权目标。 目标可为您的竞价决策提供信息 [!DNL DSP] 包和搜索组合。

>[!NOTE]
>
> 无法映射 [!DNL Analytics] Adobe广告。

您的Adobe广告团队将帮助您识别适用于付费媒体表现的事件并将其映射到Adobe广告中，这些事件将显示在 [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Transaction Properties].

请参阅“[Adobe广告中的Analytics量度](analytics-data-in-advertising.md)“ ”，以获取可用量度列表。

### 用于网站重定位的Analytics区段

Adobe广告可以 [!DNL Analytics] 区段，用于再营销DSP和 [!DNL Search] 使用本机Experience Cloud受众集成 [!DNL Analytics] 和Experience Cloud。

访问 [!DNL Analytics] 区段，广告商帐户需要 [Experience CloudID服务](https://experienceleague.adobe.com/docs/id-service/using/home.html) 已启用。 启用ID服务后，所有Experience Cloud区段(包括 [!DNL Analytics] 发布到Experience Cloud、在Adobe Audience Manager中创建的区段、在Experience Cloud中使用 [!DNL People core service]，以及在Adobe Experience Platform中创建并通过Audience Manager发送到Adobe广告的区段)，一旦处理完这些区段，即可在Adobe广告中使用。

[!DNL Analytics] 区段在24小时内可用，并且每天更新。

有关Experience Cloud受众服务的更多信息，请参阅 [Experience Cloud受众](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## 如何使用集成的示例

### 在Analysis Workspace中使用Adobe广告数据

要了解如何使用Adobe广告数据在Analysis Workspace中创建可视化报表，请观看视频“[工作区和报表简介](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html).&quot;

### 创建Adobe广告功能板

要了解如何根据Analysis Workspace中的目标跟踪Adobe广告数据，请观看视频“[使用Adobe Analytics创建Adobe广告功能板](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-dashboards-a4adc.html).&quot;

### 将Adobe广告ID用于网站登入分析

要了解如何创建Adobe广告网站登入报表以监控每周时间、每日时间、浏览器和地理位置的影响，请观看视频“[创建Adobe广告网站登入报表](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-site-entry-a4adc.html).&quot;

>[!MORELIKETHIS]
>
>* [视频：简介 [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html)
>* [实施的先决条件和关键信息 [!DNL Analytics for Advertising]](prerequisites.md)
>* [AdobeAnalytics使用的广告ID](ids.md)
>* [适用于Analytics for Advertising的JavaScript代码](/help/integrations/analytics/javascript.md)
>* [之间的预期数据差异 [!DNL Analytics] 和Adobe广告](data-variances.md)
>* [Adobe广告量度在Analysis Workspace中](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Adobe广告中的数据](/help/integrations/analytics/analytics-data-in-advertising.md)

