---
title: 关于Advertising Cloud DSP中的受众管理
description: 了解受众管理功能。
feature: DSP Audiences, DSP Segments
exl-id: 624d2211-59a2-4791-b8f1-a9a5cecd0b8e
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '1026'
ht-degree: 0%

---

# 关于Advertising Cloud DSP中的受众管理

在Advertising Cloud DSP中，您可以创建和管理受众区段和受众集，并将其用作版面的目标：

* 您可以通过创建和实施区段来收集您自己的第一方受众数据。 您可以稍后使用广告重新定位区段中的用户，或阻止区段中的用户接收广告。 您可以创建以下类型的区段：

   * [自定](/help/dsp/audiences/custom-segment-create.md) 义区段，用于跟踪a)从桌面、移动设备和CTV设备显示广告的用户，以及b)访问特定网页的用户。

   * [CCPA选择退出销售区段，](/help/dsp/audiences/ccpa-opt-out-segment-create.md) 用于根据《加州消费者隐私法案》(CCPA)，跟踪网站上消费者选择退出销售请求的用户ID。您可以从选择退出销售请求中检索用户ID的月度报表。

      有关Advertising Cloud对CCPA选择退出销售请求的支持的更多信息，请参阅[Adobe Advertising Cloud对《加州消费者隐私法案》的支持：消费者选择退出支持](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html)。

* 您可以创建包含[可重用受众](/help/dsp/audiences/reusable-audience-create.md)的受众库。 保存的受众由任何可用的受众区段以及任何其他保存的受众组成。 您对已保存受众所做的任何更改都会自动应用于定位或排除该受众的所有版面，以及包含已保存受众的所有其他受众。

   保存的受众允许媒体规划者根据需要对受众进行分组，方法是使用复杂的布尔逻辑包含和排除多个区段。 构建受众时，会指示每个区段的大小和总受众大小。 然后，营销活动执行者只需选择一个或多个已保存的受众作为版面目标，而无需为每个版面手动配置受众目标。

还提供了其他受众类型以用于版面定位。

## 导入第一方和第三方数据区段

Advertising Cloud DSP可以从数据管理平台(DMP)导入您自己的第一方数据区段，并根据需要提供给任意一组广告商。

Advertising Cloud DSP还可以导入自定义第三方区段，包括复杂的第三方区段组合。 您可以根据需要向任意一组广告商提供区段。

有关更多信息，请联系您的客户经理。

## 可用作版面目标的受众

您可以将版面定位到以下所有类型的受众。

* 保存在Advertising Cloud DSP中的所有用户创建的受众集。

* 之前在Advertising Cloud DSP中创建的所有用户创建的受众区段：

   * 访问特定网页的用户和展示特定广告展示次数的用户的自定义区段。

   * 根据《加州消费者隐私法案》(CCPA)，对于在您的网站上提交了选择退出销售请求的用户，CCPA选择退出销售受众区段。

* 导入的所有第一方数据区段。

* 所有导入的自定义第三方数据区段。

* （仅限美国的版面）[来自超过30个提供商的Advertising Cloud DSP客户可用的所有第三方数据区段，包括[!DNL Acxiom]、[!DNL Datalogix]、[!DNL eXelate]([!DNL Nielsen])、[!DNL Lotame]、[!DNL Oracle]、[!DNL Quantcast]等。](/help/dsp/audiences/third-party-data-providers.md)

   您可以定位特定区段，这些区段会根据受众数据（例如，具有特定人口统计、兴趣或意图的用户，以及/或行为配置文件）来定位用户。 您可以按数据提供程序和类别浏览，按名称或区段ID搜索区段，或按数据提供程序、总区段大小、Web浏览器计数或设备计数过滤结果。

   第三方区段会产生额外费用，每个区段名称旁边会显示这些费用。

* (使用Adobe Experience Cloud、Adobe Audience Manager或Adobe Analytics(仅限使用Advertising Cloud JavaScript转化标签的广告商)在Adobe Experience Cloud中创建、在Audience Manager中创建或从Audience Manager或[!DNL Analytics]发布到Adobe Experience Cloud的所有可用第一方、第二方或第三方受众区段。

   区段使用的定价是预先协商的，在Advertising Cloud中不可见。 <!-- Verify -->

   在Adobe Experience Cloud中创建或发布区段大约一小时后，即可使用这些区段。 直接来自Audience Manager的区段在您创建后大约24小时内可用。<!-- Verify all -->

   >[!NOTE]
   >
   >有关在这些解决方案中为区段设置和收集数据的信息，请参阅[Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html)、[Analytics](https://experienceleague.adobe.com/docs/analytics/landing/home.html)和[Adobe Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html)的文档。

## 受众大小数据

在保存的受众设置和版面设置中，您可以查看详细的受众规模数据：

* 将显示所有选定区段和已保存受众中已消除重复的受众总数和活动受众数量，您可以按设备类型（浏览器、移动设备或连接的电视）查看详细信息。

   ![总受众规模](/help/dsp/assets/audience-size.png)

* 对于单个区段和保存的受众，总受众大小和CPM（如果适用）会显示在区段名称旁边。 您可以查看有关区段的更多详细信息，包括按设备类型（浏览器、移动设备或连接的电视）的大小。 对于已保存的受众，总大小为删除重复项的总计。

   ![单个区段大小](/help/dsp/assets/audience-size-segment.png)

## 受众视图

### “所有受众”视图

在[!UICONTROL All Audiences]视图或受众库中，您可以保存和管理可重复使用的受众，包括受众区段组，甚至包括其他已保存的受众。 您可以使用受众作为多个版面的目标。 版面名称旁会显示使用每个受众的版面数量。

您可以编辑、克隆、删除、导出或共享任何受众。

### 区段视图

在[!UICONTROL Segments]视图中，所有用户都可以创建其他自定义区段。

[!UICONTROL Segments]视图还列出了以下区段类型：

* 用户可以使用所有用户创建的自定义区段。

   您可以查看您创建的任何自定义区段的跟踪标记，并与其他用户共享这些区段。 您还可以编辑或删除您创建的自定义区段。

   您无法编辑或共享其他用户与您共享的自定义区段。

* 用户可以使用所有导入的第一方区段。

   您无法编辑或共享与您共享的第一方区段。 如果您需要与其他用户共享第一方区段，请联系您的客户经理。

* 用户可以使用所有自定义第三方区段。

   您无法编辑或共享与您共享的第三方区段。 如果您需要与其他用户共享第三方区段，请联系您的客户经理。

>[!MORELIKETHIS]
>
>* [创建可重用受众](reusable-audience-create.md)
>* [受众设置](audience-settings.md)
>* [受众区段逻辑的语法](audience-segment-logic-syntax.md)
>* [创建和实施自定义区段](custom-segment-create.md)
>* [创建和实施区 [!UICONTROL CCPA Opt-Out-of-Sale] 段](ccpa-opt-out-segment-create.md)
>* [可用的第三方数据提供商](third-party-data-providers.md)
>* [版面设置](/help/dsp/campaign-management/placements/placement-settings.md)

