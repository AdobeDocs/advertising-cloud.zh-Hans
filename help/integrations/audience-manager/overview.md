---
title: Adobe与Adobe Audience Manager的广告集成
description: 了解Adobe广告可以通过不同方式与Adobe Audience Manager交换数据。
feature: Integration with Adobe Audience Manager
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---

# Adobe与Adobe Audience Manager的广告集成

您可以通过以下方式将Adobe广告与Audience Manager集成。

## 同步Audience Manager和其他 [!DNL Adobe] 用于广告定位的区段

[!DNL Search] 和DSP可以提取广告商或代理的所有Audience Manager和其他 [!DNL Adobe] 受众。 此独特连接仅适用于使用Adobe广告的营销人员。 请参阅“[导入Adobe Audience Manager区段以进行广告定位](/help/integrations/audience-manager/import-audiences.md).&quot;

### 使用Audience Manager和其他 [!DNL Adobe] 要创建的区段 [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*已选择加入的广告商，具有 [!DNL Advertising Search] 仅*

在[!DNL内 [!DNL Search]]您可以创建 [!DNL Google Ads] Google客户使用您现有的具有 [!UICONTROL Adobe Media Optimizer (HTTP)] 和 [!UICONTROL Adobe Media Optimizer Batch Destination] 作为目标。 ([!DNL Media Optimizer] 是[!DNL的以前名称 [!DNL Search]]) 这包括发布到Adobe Experience Cloud的Adobe Analytics区段，以及在Adobe Experience Cloud中使用 [!DNL People core service]. 有关更多信息，请参阅[!DNL中的产品内帮助 [!DNL Search]]。

[客户匹配来自用户ID的受众](https://support.google.com/google-ads/answer/9199250) 与基于网站标签的受众类似，但会将非PII ID分配给独特受众成员，以获得比标准客户匹配和基于网站标签的受众更显着的优势。

要创建必要的用户ID，您必须使用Adobe广告JavaScript标记 <!-- with a user ID parameter -->在您的网站上。 联系您的[!DNL [!DNL Search]]客户团队以了解更多信息。

![区段创建过程](/help/integrations/assets/ad_search_user_id_pic.png)

创建受众后，即可在 [!DNL Google Ads] 营销活动 [营销活动级别或广告组级别的目标或排除项](#audience-manager-targets).

### 使用Audience Manager和其他 [!DNL Adobe] 要定位或排除广告的区段 {#audience-manager-targets}

* （使用[!DNL的选择加入广告商） [!DNL Search]])您可以使用任何 [!DNL Google Ads] 受众 [使用 [!DNL Adobe] 区段](#audience-manager-google-audiences) 作为营销活动级别或广告组级别的目标或排除项 [!DNL Google Ads] 营销活动。

* (使用DSP的广告商)您可以使用现有 [!DNL Adobe] 区段作为广告投放的目标。 您可以选择将区段包含在可重复使用的受众中，以将其用作多个版面的目标或排除项。

* （具有广告创意的广告商）您可以使用现有 [!DNL Adobe] 区段作为广告体验中特定创意的目标。

>[!NOTE]
>
>有关如何在受众和Experience Cloud中创建受众的更多信息 [!DNL Audience Library] 不同受众类型的界面和常见用例，请参阅[受众创建选项](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html).&quot;

## 将DSP媒体曝光数据发送到Audience Manager

*仅使用DSP的广告商*

具有Adobe Audience Manager的DSP客户可以使用对Audience Manager的像素调用从广告促销活动中捕获数据。 然后，您可以使用促销活动数据构建基于规则的特征，您可以使用该特征定义新区段以启用各种DSP用例，如更高级的分段、频率管理、营销分析和报表分析。

请参阅“[将DSP媒体曝光数据发送到Adobe Audience Manager概述](/help/integrations/audience-manager/media-data-integration/overview.md)“ ”以了解详细信息。

## 通过Audience Analytics，更深入地分析网站活动

Adobe广告客户 [[!DNL Adobe][!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) 可将Adobe广告跟踪数据和Audience Manager区段发送到 [!DNL Analytics] 以丰富有关网站活动的分析。

有关更多信息，请参阅[[!DNL Adobe][!DNL Audience Analytics] Adobe广告客户](/help/integrations/audience-manager/audience-analytics.md).&quot;
