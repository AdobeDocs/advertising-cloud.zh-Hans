---
title: 关于Advertising DSP中的受众管理
description: 了解受众管理功能。
feature: DSP Audiences, DSP Segments
exl-id: 624d2211-59a2-4791-b8f1-a9a5cecd0b8e
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '1036'
ht-degree: 0%

---

# 关于Advertising DSP中的受众管理

在DSP中，您可以创建和管理受众区段和受众集，并将它们用作版面的目标：

* 您可以通过创建和实施区段来收集您自己的第一方受众数据。 您可以稍后使用广告重新定位区段中的用户，或阻止区段中的用户接收广告。 您可以创建以下类型的区段：

   * [自定义区段](/help/dsp/audiences/custom-segment-create.md) 用于跟踪a)从桌面、移动设备和CTV设备显示广告的用户，以及b)访问特定网页的用户。

   * [CCPA选择退出销售区段](/help/dsp/audiences/ccpa-opt-out-segment-create.md) 要根据《加州消费者隐私法案》(CCPA)，跟踪网站上消费者选择退出销售请求的用户ID。 您可以从选择退出销售请求中检索用户ID的月度报表。

      有关Adobe广告对CCPA选择退出销售请求的支持的更多信息，请参阅 [Adobe对《加州消费者隐私法案》的广告支持：消费者选择退出支持](/help/privacy/ad-cloud-ccpa-opt-out-of-sale.md).

* 您可以创建的受众库 [可重用受众](/help/dsp/audiences/reusable-audience-create.md). 保存的受众由任何可用的受众区段以及任何其他保存的受众组成。 您对已保存受众所做的任何更改都会自动应用于定位或排除该受众的所有版面，以及包含已保存受众的所有其他受众。

   保存的受众允许媒体规划者根据需要对受众进行分组，方法是使用复杂的布尔逻辑包含和排除多个区段。 构建受众时，会指示每个区段的大小和总受众大小。 然后，营销活动执行者只需选择一个或多个已保存的受众作为版面目标，而无需为每个版面手动配置受众目标。

还提供了其他受众类型以用于版面定位。

## 导入第一方和第三方数据区段

DSP可以从数据管理平台(DMP)导入您自己的第一方数据区段，并根据需要将其提供给任意一组广告商。

DSP是 [the [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html)，允许您与批准的广告商和用户共享经过身份验证的第一方区段，以激活促销活动。 要了解有关Real-Time CDP集成的更多信息，请参阅 [“源”部分](/help/dsp/audiences/sources/source-about.md).

DSP还可以导入自定义第三方区段，包括复杂的第三方区段组合。 您可以根据需要向任意一组广告商提供区段。

联系您的 [!DNL Adobe] 帐户团队以了解更多信息。

## 可用作版面目标的受众

您可以将版面定位到以下所有类型的受众。

* 保存在DSP中的所有用户创建的受众集。

* 之前在DSP中创建的所有用户创建的受众区段：

   * 访问特定网页的用户和展示特定广告展示次数的用户的自定义区段。

   * 根据《加州消费者隐私法案》(CCPA)，对于在您的网站上提交了选择退出销售请求的用户，CCPA选择退出销售受众区段。

* 导入的所有第一方数据区段。

* 所有导入的自定义第三方数据区段。

* （仅针对美国的版面） [来自30多家提供商的DSP客户可以使用的所有第三方数据区段](/help/dsp/audiences/third-party-data-providers.md)，包括 [!DNL Acxiom], [!DNL Datalogix], [!DNL eXelate] ([!DNL Nielsen])、 [!DNL Lotame], [!DNL Oracle], [!DNL Quantcast]，等等。

   您可以定位特定区段，这些区段会根据受众数据（例如，具有特定人口统计、兴趣或意图的用户，以及/或行为配置文件）来定位用户。 您可以按数据提供程序和类别浏览，按名称或区段ID搜索区段，或按数据提供程序、总区段大小、Web浏览器计数或设备计数过滤结果。

   第三方区段会产生额外费用，每个区段名称旁边会显示这些费用。

* (具有Adobe Experience Platform和 [!DNL Real-Time CDP]、Adobe Audience Manager或Adobe Analytics(仅使用Adobe广告JavaScript转化标记)在 [!DNL Real-Time CDP]、在Audience Manager中创建，或从Audience Manager或发布到Adobe Experience Cloud [!DNL Analytics].

   区段使用的定价是预先协商的，在DSP中不可见。

   区段来源 [!DNL Analytics] 在创建或发布作为Experience Cloud受众大约一小时后可用。 区段直接来自Audience Manager或 [!DNL Real-Time CDP] 将在您共享它们后的24小时内提供。

   >[!NOTE]
   >
   >请参阅相关文档 [Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html), [Analytics](https://experienceleague.adobe.com/docs/analytics.html)和 [the [!DNL Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/segmentation/segment-builder-guide.html) 以了解有关为这些解决方案中的区段设置和收集数据的信息。

## 受众大小数据

在保存的受众设置和版面设置中，您可以查看详细的受众大小数据：

* 将显示所有选定区段和已保存受众中已消除重复的受众总数和活动受众数量，您可以按设备类型（浏览器、移动设备或连接的电视）查看详细信息。

   ![总受众规模](/help/dsp/assets/audience-size.png)

* 对于单个区段和保存的受众，总受众大小和CPM（如果适用）会显示在区段名称旁边。 您可以查看有关区段的更多详细信息，包括按设备类型（浏览器、移动设备或连接的电视）的大小。 对于已保存的受众，总大小为删除重复项的总计。

   ![单个区段大小](/help/dsp/assets/audience-size-segment.png)

## 受众视图

### “所有受众”视图

在 [!UICONTROL All Audiences] 查看或受众库，您可以保存和管理可重复使用的受众，包括受众区段组，甚至包括其他已保存的受众。 您可以使用受众作为多个版面的目标。 版面名称旁会显示使用每个受众的版面数量。

您可以编辑、克隆、删除、导出或共享任何受众。

### 区段视图

在 [!UICONTROL Segments] 视图，所有用户都可以创建其他自定义区段。

的 [!UICONTROL Segments] 查看还会列出以下区段类型：

* 用户可以使用所有用户创建的自定义区段。

   您可以查看您创建的任何自定义区段的跟踪标记，并与其他用户共享这些区段。 您还可以编辑或删除您创建的自定义区段。

   您无法编辑或共享其他用户与您共享的自定义区段。

* 用户可以使用所有导入的第一方区段。

   您无法编辑或共享与您共享的第一方区段。 联系您的 [!DNL Adobe] 帐户团队。

* 用户可以使用所有自定义第三方区段。

   您无法编辑或共享与您共享的第三方区段。 联系您的 [!DNL Adobe] 帐户团队。

>[!MORELIKETHIS]
>
>* [创建可重用受众](reusable-audience-create.md)
>* [受众设置](audience-settings.md)
>* [受众区段逻辑的语法](audience-segment-logic-syntax.md)
>* [创建和实施自定义区段](custom-segment-create.md)
>* [创建和实施 [!UICONTROL CCPA Opt-Out-of-Sale] 区段](ccpa-opt-out-segment-create.md)
>* [可用的第三方数据提供商](third-party-data-providers.md)
>* [版面设置](/help/dsp/campaign-management/placements/placement-settings.md)

