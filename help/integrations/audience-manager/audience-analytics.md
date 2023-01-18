---
title: '''[!DNL Adobe] [!DNL Audience Analytics] (针对Adobe广告客户)'
description: 了解如何使用 [!DNL Adobe] [!DNL Audience Analytics] 用于广告用例
feature: Integration with Adobe Audience Manager
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# [!DNL Adobe] [!DNL Audience Analytics] Adobe广告客户

[[!DNL Adobe] [!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) 是Adobe Audience Manager与Adobe Analytics的集成，允许Audience Manager客户将区段发送到 [!DNL Analytics] 以丰富有关网站活动的分析。

Adobe广告客户可以使用 [!DNL Audience Analytics]. 该集成允许您：

* 将Adobe广告曝光数据直接发送到 [!DNL Analytics] 以确定上漏斗活动对下游站点活动的影响。

* 从漏斗上曝光广告中确定营销渠道和网站入口点。

* 对集成进行分层 [!DNL Analytics for Advertising] 以整合 [Audience Manager [!DNL Audience Marketplace]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/audience-marketplace/audience-marketplace.html) with [!DNL Analytics for Advertising] 数据，以进一步分析用户配置文件。

   [!DNL Audience Marketplace] 通过“激活”订阅模型提供对第三方数据馈送的访问，该订阅模型允许购买者将数据发送到目标。 如果数据在 [!DNL Analytics] 目标，则不会收取激活费用。

* (使用Advertising DSP的广告商)添加其他曝光区段，以便获得全面的历程管理分析。

   Advertising DSP可以通过实施Adobe Experience Platform或Audience Manager展示跟踪像素，将曝光数据作为可操作信号发送给Audience Manager。 将相同的数据转发到 [!DNL Analytics] 启用高级数据分析。 请参阅“[Adobe广告媒体数据与Adobe Audience Manager集成概述](/help/integrations/audience-manager/media-data-integration/overview.md)“ ”以了解详细信息。

有关 [!DNL Audience Analytics]，包括其先决条件和工作流，请参阅[Audience Analytics概述](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html).&quot;

## 使用方法示例 [!DNL Audience Analytics] 包含Adobe广告数据的数据

以下是如何在 [!DNL Analytics] [!DNL Analysis Workspace].

### 请参阅上漏斗活动对下游活动的影响

使用Audience Manager曝光区段可查看上漏斗网站活动对下游网站活动的影响。 将Adobe广告或第三方宏ID包含在您的跟踪像素中，以跟踪对详细级别的影响，从促销活动级别到用户所在网站的级别。

主要优势：

* 按漏斗/广告类型跟踪曝光情况并使用 [!DNL Audience Analytics] 以确定登入率并与客户历程的下一个阶段重叠。

* 确定上漏斗活动对下游站点活动的影响。

* 连接 [!DNL Analytics for Advertising]<!-- which doesn't include the last exposure event --> 和 [!DNL Audience Analytics] 数据 <!-- (which includes the user's last exposure event) --> 确定网站的整体历程。

以下是您可以在中创建的报表示例 [!DNL Analysis Workspace].

![查看上漏斗活动对下游网站活动的影响](/help/integrations/assets/audience-analytics-upper-funnel-exposure.png)

### 使用 [!DNL Audience Analytics] 用于用户配置文件分析的第三方区段数据

使用第三方Audience Manager区段，更深入地分析用户如何与您的网站进行交互。 您可以根据第三方区段的用户档案如何与媒体营销活动网站的关键绩效指标进行交互，使用信息确定要为其激活媒体的新第三方受众。

>[!TIP]
> 使用Audience Manager `Audiences ID` 和 `Audiences Name` 维度贯穿整个 [!DNL Analytics]，与任何其他维度一样 [!DNL Analytics] 收集。

以下是您可以在中创建的报表示例 [!DNL Analysis Workspace].

![使用第三方区段扩充用户配置文件分析](/help/integrations/assets/audience-analytics-third-party-report.png)

>[!MORELIKETHIS]
>
>* [Adobe与Adobe Audience Manager的广告集成](/help/integrations/audience-manager/overview.md)

