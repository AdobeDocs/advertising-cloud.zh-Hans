---
title: 关于从受众源激活经过身份验证的区段
description: 了解如何从客户数据平台摄取第一方区段。
feature: DSP Audiences
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# 关于从受众源激活经过身份验证的区段

<!-- Doesn't specifically explain what you can do in our UI -->
*测试版功能*

DSP可以摄取由在客户数据平台(CDP)中构建的经过验证的信号组成的第一方区段。 您可以将摄取的区段用作版面的目标。

## [!DNL Adobe Real-Time Customer Data Profile]

DSP与 [the [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html)，是Adobe Experience Platform的一部分。

在 [!DNL Real-time CDP], *目标* 是与外部数据平台的连接，允许无缝数据激活。 例如，您可以使用目标来激活您已知的客户关系（如经过哈希处理的电子邮件地址），以便在DSP支持的数字格式中进行定向广告。

有关目标的更多信息，请参阅Experience Platform [目标指南](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html)，包括产品概述， [创建目标工作区](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) 和 [创建目标连接](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html)和 [将数据激活到目标](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

### 使用DSP集成的工作流 [!DNL Real-time CDP] {#workflow-sources}

<!-- Make sure that titles make the distinctions clear -- everything can't be "Activate XXX." -->

1. [允许DSP将客户数据区段转换为 [!DNL LiveRamp RampIDs]](source-durable-id.md) 在可拍的环境中可辨认的。<!-- I don't think I need this here: This requires DSP account-level and campaign-level settings to enable segment sharing with [!DNL LiveRamp], which will translate customer data to [!DNL RampIDs] to create targetable segments. Your DSP account team will perform this configuration. -->

1. [创建受众源](source-create.md) 将受众导入DSP帐户或广告商帐户。

1. [配置 [!DNL Real-Time CDP] 目标连接Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).

如需其他支持，请联系 [!DNL Adobe] 客户团队或 `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [从持久ID合作伙伴激活经过身份验证的区段](source-durable-id.md)
>* [创建受众源以激活第一方受众](source-create.md)
>* [受众源设置](source-settings.md)
>* [AdobeAdvertising DSP Connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [目标目录概述](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [关于受众管理](/help/dsp/audiences/audience-about.md)

