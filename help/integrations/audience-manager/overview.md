---
title: Advertising Cloud与Adobe Audience Manager集成
description: 了解Advertising Cloud与Adobe Audience Manager交换数据的不同方式。
feature: Integration with Adobe Audience Manager
source-git-commit: c761c96b32171bcfba12ed4a39235e6e8b6f6d34
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 0%

---

# Advertising Cloud与Adobe Audience Manager集成

您可以通过以下方式将Advertising Cloud与Audience Manager集成。

## 同步Audience Manager和其他 [!DNL Adobe] 用于广告定位的区段

Advertising Cloud Search和Advertising Cloud DSP可以提取所有广告商或代理Audience Manager以及其他活动的元数据、层次结构数据和独特受众数据 [!DNL Adobe] 受众。 此独特连接仅适用于使用Advertising Cloud的营销人员。 请参阅“[导入Adobe Audience Manager区段以进行广告定位](/help/integrations/audience-manager/import-audiences.md).&quot;

### 使用Audience Manager和其他 [!DNL Adobe] 要创建的区段 [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*已选择加入的广告商，具有 [!DNL Advertising Cloud Search] 仅*

在 [!DNL Search]，您可以创建 [!DNL Google Ads] Google客户使用您现有的具有 [!UICONTROL Adobe Media Optimizer (HTTP)] 和 [!UICONTROL Adobe Media Optimizer Batch Destination] 作为目标。 ([!DNL Media Optimizer] 以前是Advertising Cloud Search的名字。) 这包括发布到Adobe Experience Cloud的Adobe Analytics区段，以及在Adobe Experience Cloud中使用 [!DNL People core service]. 有关更多信息，请参阅 [!DNL Search].

[客户匹配来自用户ID的受众](https://support.google.com/google-ads/answer/9199250) 与基于网站标签的受众类似，但会将非PII ID分配给独特受众成员，以获得比标准客户匹配和基于网站标签的受众更显着的优势。

要创建必要的用户ID，您必须使用Advertising Cloud JavaScript标记 <!-- with a user ID parameter -->在您的网站上。 有关更多信息，请联系您的Advertising Cloud Search客户团队。

![区段创建过程](/help/integrations/assets/ad_search_user_id_pic.png)

创建受众后，即可在 [!DNL Google Ads] 营销活动 [营销活动级别或广告组级别的目标或排除项](#audience-manager-targets).

### 使用Audience Manager和其他 [!DNL Adobe] 要定位或排除广告的区段 {#audience-manager-targets}

* (已选择加入的广告商， [!DNL Search])您可以使用 [!DNL Google Ads] 受众 [使用 [!DNL Adobe] 区段](#audience-manager-google-audiences) 作为营销活动级别或广告组级别的目标或排除项 [!DNL Google Ads] 营销活动。

* (具有Advertising Cloud DSP的广告商)您可以使用现有 [!DNL Adobe] 区段作为广告投放的目标。 您可以选择将区段包含在可重复使用的受众中，以将其用作多个版面的目标或排除项。

* (具有Advertising Cloud Creative的广告商)您可以使用现有 [!DNL Adobe] 区段作为广告体验中特定创意的目标。

>[!NOTE]
>
>有关如何在受众和Experience Cloud中创建受众的更多信息 [!DNL Audience Library] 不同受众类型的界面和常见用例，请参阅[受众创建选项](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html).&quot;

## 将DSP媒体曝光数据发送到Audience Manager

*仅使用DSP的广告商*

使用Adobe Audience Manager的Advertising Cloud DSP客户可以使用像素调用从广告促销活动中捕获Audience Manager。 然后，您可以使用促销活动数据构建基于规则的特征，您可以使用该特征定义新区段以启用各种DSP用例，如更高级的分段、频率管理、营销分析和报表分析。

请参阅“[将DSP媒体曝光数据发送到Adobe Audience Manager概述](/help/integrations/audience-manager/media-data-integration/overview.md)“ ”以了解详细信息。

## 通过Audience Analytics，更深入地分析网站活动

Advertising Cloud客户 [[!DNL Adobe][!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) 可以将Advertising Cloud跟踪的数据和Audience Manager区段发送到 [!DNL Analytics] 以丰富有关网站活动的分析。

有关更多信息，请参阅[[!DNL Adobe][!DNL Audience Analytics] 对于Advertising Cloud客户](/help/integrations/audience-manager/audience-analytics.md).&quot;
