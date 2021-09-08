---
title: 将 [!DNL Marketing Channels] 与Advertising Cloud数据一起使用
description: 了解如何在 [!DNL Analytics Marketing Channels]中使用Advertising Cloud数据。
feature: Integration with Adobe Analytics
exl-id: null
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '706'
ht-degree: 0%

---

# 将[!DNL Analytics Marketing Channels]用于Advertising Cloud数据

*仅具有Advertising Cloud-Adobe Analytics集成的广告商*

通过同时使用Advertising Cloud和[!DNL Marketing Channels]报表，您可以对数字媒体对网站活动的影响进行有价值的分析。

<!-- from video: By using Marketing Channels with your Advertising Cloud data, you can get a more holistic view of how your advertising efforts are affecting site behavior. In particular, you can see the value of your view-through and click-through data, and how your advertising assists or is assisted by other channels. -->

下图显示了Advertising Cloud和[!DNL Marketing Channels]如何跟踪构成一个访客历程的各个访问。 [!DNL Analytics]中的Advertising Cloud报表仅限于使用AMO ID通过Advertising Cloud贩运的付费展示和搜索广告。 但是，[!DNL Marketing Channels]会跟踪在[!DNL Marketing Channels]处理规则中配置的所有通道。

![Advertising Cloud和跟 [!DNL Marketing Channels] 踪访客历程中个人访问的方式](/help/integrations/assets/a4adc-mc-sample-journey2.png)

在第一次访问中，用户通过电子邮件营销活动进入网站，执行十次页面查看，然后离开。 在第二次访问中，用户通过展示广告进入网站，执行十次页面查看，然后离开。 在第三次访问中，用户通过免费搜索进入网站，执行五次页面查看，执行了250美元的转化，最后左转。 请注意[!DNL Marketing Channels]和Advertising Cloud之间在跟踪方面的差异。 Advertising Cloud在此历程中跟踪的唯一渠道是[!UICONTROL Display]。 Advertising Cloud会跟踪[!UICONTROL Display]渠道访问，并将后续参与数据（如页面查看次数）和转化归因到该广告的影响。 [!DNL Marketing Channels]，则会显示所有渠道的完整视图。

由于AMO ID在访客历程中持续存在，因此您可以使用AMO ID数据来查看Advertising Cloud对其他营销渠道有何影响。 AMO ID [默认保留60天](/help/integrations/analytics/overview.md)，但您可以根据需要配置持久性。

## 如何将Advertising Cloud和营销渠道数据结合起来分析媒体效果

在[!DNL Analytics]中，您可以将Advertising Cloud持久保留的付费广告数据与[!DNL Marketing Channels]全面的访问数据相结合，以更好地分析媒体性能，从而更好地影响客户旅程。

以下分析使用Advertising Cloud数据来显示不同版本的展示广告对网站转化的影响。 所有三列都使用相同的转化量度，但每一列的情况不同：

* 列1查看在访客历程中持久保留的AMO ID数据。 列1表示有641个应用程序启动事件曾经通过显示到达事件或点进事件与Advertising Cloud广告链接。 此视图未考虑任何其他[!DNL Marketing Channels]归因。

* 但是，在[!DNL Marketing Channels]数据集中，641应用程序启动归因于其他营销渠道。 最后两列采用641个应用程序启动，并将数据限制在[!UICONTROL Display Click-Through]和[!UICONTROL Display View-Through]渠道中，以显示在最近联系归因模型中发生的转化。

![展示广告如何影响网站转化的示例](/help/integrations/assets/a4adc-mc-display-impact.png)

您可以进一步分析此问题。 您可以按营销渠道进一步划分Advertising Cloud行，以查看Advertising Cloud转化归因于641应用程序开始的位置。 您已经知道，其中5个转化归因于最近联系显示点进，19个归因于最近联系显示显示显示点进。 这仍然会导致617个应用程序开始归因于其他营销渠道。 您可以将“最近联系渠道”维度拖放到Advertising Cloud DSP行项目的顶部，以显示其余“应用程序启动”的渠道归因，并显示“显示”渠道的跨渠道影响。

![如何添加“最近联系渠道”维度](/help/integrations/assets/a4adc-mc-display-impact-ltc.png)

现在，您可以查看剩余应用程序开始的归因方式。 对于保留AMO ID的357个最近联系应用程序启动，会为电子邮件分配点数。 通过此类分析，您可以了解Advertising Cloud显示广告在所有渠道中产生的影响。 只有一个数据集和归因模型，此类分析将不可用。

![显示渠道的跨渠道影响示例](/help/integrations/assets/a4adc-mc-display-impact-x-channel.png)

您可以使用设置为“100%堆叠”的堆栈图来显示一段时间内的趋势数据，从而进一步改进分析。 通过此可视化图表，可以更轻松地监控哪些最近联系营销渠道受到展示型营销活动的影响更大。

![显示渠道的趋势跨渠道影响示例](/help/integrations/assets/a4adc-mc-display-impact-x-channel-trend.png)

>[!MORELIKETHIS]
>
>* [的基本原理 [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [使用Advertising Cloud ID创建 [!DNL Marketing Channels] 处理规则](mc-ids.md)
>* [为何渠道数据在Advertising Cloud和 [!DNL Marketing Channels]](mc-data-variances.md)
>* [视频：使用Advertising Cloud报告 [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [概述 [!DNL Analytics for Advertising Cloud]](/help/integrations/analytics/overview.md)

