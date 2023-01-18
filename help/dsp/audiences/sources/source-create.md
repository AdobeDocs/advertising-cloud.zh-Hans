---
title: 创建受众源以激活第一方受众
description: 了解如何创建源以将受众导入您的帐户或广告商帐户。
feature: DSP Audiences
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---

# 创建受众源以激活第一方受众

*测试版功能*

<!-- Will this remain for admin users/Adobe account teams only? -->

创建将受众导入DSP帐户或广告商帐户的源。 目前，您可以从 [the [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html).

>[!NOTE]
>
>在为 [!DNL Real-Time CDP]，您需要激活 [!DNL Real-Time CDP] 受众(通过AdobeAdvertising DSP目标在 [!DNL Real-Time CDP] 以开始导入。 请参阅 [激活工作流中的步骤](source-about.md#workflow-sources).

1. 在主菜单中，单击**[!UICONTROL Audiences] > [!UICONTROL Sources (BETA)].

1. 单击 [!UICONTROL Add Source].

1. 在 [!UICONTROL Select a Type] 菜单，选择源类型。

   *[!UICONTROL RT-CDP]*:此源类型，用于 [the [!DNL Adobe Real-Time Customer Data Profile]](source-about.md)，是唯一选项。

1. 指定 [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* 或 *[!UICONTROL Account]*.

1. 输入剩余 [源设置](source-settings.md).

   保留 [!UICONTROL Source Key] 生成。 您稍后需要该值。

1. 单击 **[!UICONTROL Save]**.

1. 在Experience Platform中，使用 [!UICONTROL Source Key] 在DSP源设置中生成的URL。

有关激活DSP目标连接、选择区段和访问控制权限的说明，请参阅[Adobe Advertising Cloud DSP连接](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).&quot;

>[!MORELIKETHIS]
>
>* [受众源设置](source-settings.md)
>* [关于从受众源激活经过身份验证的区段](source-about.md)
>* [从持久ID合作伙伴激活经过身份验证的区段](source-durable-id.md)<!-- title?-->
>* [Adobe Advertising Cloud DSP连接](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [关于受众管理](/help/dsp/audiences/audience-about.md)

