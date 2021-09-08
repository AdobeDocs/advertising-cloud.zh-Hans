---
title: ' [!DNL Marketing Channels]的基础知识'
description: 了解有关 [!DNL Analytics Marketing Channels] that [!DNL Analytics for Advertising Cloud] 用户应该了解的关键信息。
feature: Integration with Adobe Analytics
exl-id: null
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 0%

---

# [!DNL Analytics Marketing Channels]的基础知识

*仅具有Advertising Cloud-Adobe Analytics集成的广告商*

本页介绍了[!DNL Analytics for Advertising Cloud]用户需要了解的关于[!DNL Analytics Marketing Channels]的关键信息。

有关[!DNL Marketing Channels]的完整文档，请参阅“[ [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/c-getting-started-mchannel.html)快速入门”。

## [!DNL Marketing Channels]概述

[!DNL Marketing Channels] 是Adobe Analytics的关键功能。[!DNL Marketing Channels] 报表显示客户如何通过报表窗口访问您的网站，以及每个渠道如何影响收入或网站行为。

请考虑以下跨访问历程示例。 访客每次访问您的网站时都会通过访客进入的营销渠道来表示。 首次访问（也称为首次联系渠道）是电子邮件。 第二次访问时显示是一个参与渠道，“免费搜索”被视为“最近联系渠道”。 如果您在[!UICONTROL Attribution IQ]中使用[!UICONTROL Last Touch Attribution]，则免费搜索将收到250美元转化事件的全部点数。 使用Experience CloudID服务，您可以将这些单独的访问绑定在一起，以便显示单个访客的一个历程。

![营销渠道中的跨访问转化历程示例](/help/integrations/assets/a4adc-mc-sample-journey.png)

通过使用[!UICONTROL Marketing Channels]处理规则，您可以创建一组逻辑来确定驱动流量的渠道，并在用户访问您的网站时跟踪每个渠道。 例如， [!UICONTROL Email]渠道将由单击时生成的唯一跟踪代码来指示，当Adobe Analytics记录该代码时，会将访问分类为来自电子邮件营销活动的访问。

## 处理规则和如何设置营销渠道

每次用户访问网站时，都会通过他们单击或直接在地址栏中键入的URL来执行此操作。 当用户进入网站时，[!DNL Analytics]会跟踪可用于确定访问渠道的信息。

营销人员通常会在渠道URL中附加查询字符串参数跟踪代码，以帮助跟踪渠道对其网站的影响。 您可以配置[!DNL Marketing Channels]处理规则来监听特定跟踪参数和值，以确定渠道，而无需进行任何其他跟踪。 例如，如果所有电子邮件促销活动URL的格式均遵循`www.adobe.com?cid=email…`（其中URL包含查询字符串参数和值`cid=email`），则可以创建一个规则来监听此跟踪代码，并将访问存储到[!UICONTROL Email]渠道中。

其他渠道没有可跟踪的URL路径，需要进一步的逻辑才能进行识别。 例如，[!UICONTROL Earned Social]是一个重要的跟踪渠道，用户在其中点击另一个用户在社交网络上自然共享的链接。 但是，营销人员无法将查询字符串参数跟踪代码附加到共享的URL。 在这种情况下，您可以创建一个处理规则来监听社交网络的引荐域，并且没有付费跟踪代码来确定渠道。 随后，将在营销渠道报表中将满足这些要求的访问作为免费社交进行跟踪。

Adobe建议与您的分析团队合作，构建一组全面的[!DNL Marketing Channels]处理规则，以跟踪与您的业务相关的所有渠道。 这样，您就可以创建功能强大的归因报表。

要了解Advertising Cloud如何对创建自定义营销渠道所需的信号做出贡献，请参阅“[使用广告ID创建 [!DNL Marketing Channels] 规则](mc-ids.md)”。

>[!MORELIKETHIS]
>
>* [使用Advertising Cloud ID创建 [!DNL Marketing Channels] 处理规则](mc-ids.md)
>* [为何渠道数据在Advertising Cloud和 [!DNL Marketing Channels]](mc-data-variances.md)
>* [ [!DNL Analytics Marketing Channels] 使用Advertising Cloud数据](mc-ac-data.md)
>* [视频：使用Advertising Cloud报告 [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [概述 [!DNL Analytics for Advertising Cloud]](/help/integrations/analytics/overview.md)

