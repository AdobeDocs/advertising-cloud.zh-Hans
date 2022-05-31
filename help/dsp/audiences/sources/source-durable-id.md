---
title: '从持久ID合作伙伴激活经过身份验证的区段 '
description: 了解如何通过持久ID解决方案激活经过验证的受众。
feature: DSP Audiences
source-git-commit: 155ab740084bebfba5fd992a23706129668fcc90
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# 从持久ID合作伙伴激活经过身份验证的区段

*测试版功能*

要通过Advertising Cloud DSP内的持久ID解决方案激活经过验证的受众，您的区段必须转换为 [!DNL RampIDs]，可在可买的环境中识别。 您可以通过以下任一方式实现此目的：

* 利用DSP与 [!DNL Adobe Real-Time Customer Data Profile (CDP)] 和 [!DNL Adobe-LiveRamp Retrieval API].

* 从将经过身份验证的区段手动发送到DSP [!DNL LiveRamp] [!DNL Connect] 功能板。

## 任务

1. 对于任一选项，请联系 `adcloud-support@adobe.com` 可在DSP中启用以下设置，以便在DSP促销活动中定位经过身份验证的区段一次 [激活工作流中的所有步骤均已完成](source-about.md#workflow-sources):

   1. [!DNL LiveRamp] [!DNL RampID] 从共享区段之前的营销活动配置 [!DNL Real-Time CDP].

   1. 帐户级别“[!UICONTROL LiveRamp segments]“ ”选项。

1. (用户从 [!DNL LiveRamp])在 [!DNL LiveRamp] [!DNL Connect] 功能板：

   1. 激活目标磁贴 **[!DNL AAC API 1P Onboarding]**.

   1. 已设置 [!DNL Identifier Settings] to **[!DNL Ramp ID]** 仅。

      ![标识符设置](/help/dsp/assets/liveramp-tile-settings.png)

   1. （可选）如果您仍要接收基于Cookie的标识符，请再创建一个 [!DNL AAC API 1P Onboarding] 目标磁贴带有“[!DNL Cookies], &quot;[!DNL IDFA]、和[!DNL AAID]“ ”。

## 测试和数据验证的最佳实践

* **Target [!DNL RampID]不同营销活动中基于Cookie的区段和基于Cookie的区段。**

   * 促销活动设置仅允许一个标识符按优先级排列。

   * 目前， [!DNL RampIDs] 无法在现场事件中检索。 这意味着某些自定义目标（如最低CPA和ROAS）在使用经过身份验证的区段时不可用。 仅当您具有限制性的性能KPI时，才使用基于Cookie的区段。

* **在 [!DNL RampID] 和基于Cookie的营销活动。**

   * 定位从中共享的区段 [!DNL LiveRamp] 使用标准区段激活流程。

   * 与您的Advertising Cloud支持团队合作，以验证正确的数据分发。

详细了解DSP与 [!DNL LiveRamp]，联系 `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [关于从受众源激活经过身份验证的区段](source-about.md)
>* [创建受众源以激活第一方受众](source-create.md)
>* [受众源设置](source-settings.md)
>* [Adobe Advertising Cloud DSP连接](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [关于受众管理](/help/dsp/audiences/audience-about.md)

