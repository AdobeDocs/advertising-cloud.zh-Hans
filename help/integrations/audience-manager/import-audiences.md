---
title: 导入Adobe Audience Manager区段以进行广告定位
description: 了解如何导入 [!DNL Adobe] 使用Adobe Audience Manager将受众导入DSP和搜索
feature: Integration with Adobe Audience Manager
exl-id: 08a40148-b7d2-442b-81e8-f3aec4fca7df
source-git-commit: 17482b831c5db7ef6c211f87b2e408443180746e
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 0%

---

# 导入Adobe Audience Manager区段以进行广告定位

Advertising DSP和 [!DNL Advertising Search] 可以分别提取所有广告商或代理的元数据、层次结构数据和唯一受众数据 [!DNL Adobe] 受众<!-- segments or audiences? Standardize terms per AAM's docs -->. 这包括以下数据：

* Adobe Audience Manager区段

* Adobe Analytics区段发布到Adobe Experience Cloud

* 在Adobe Experience Cloud中使用 [!DNL People core service]

* 在Adobe Experience Platform中创建并通过Audience Manager发送到Adobe广告的区段

访问 [!DNL Adobe] DSP或 [!DNL Creative]，则必须将受众导入DSP。 访问 [!DNL Adobe] [!DNL中的受众 [!DNL Search]]，则必须将受众导入[!DNL [!DNL Search]]。

## 先决条件

* 广告商必须实施 [the [!DNL Adobe Experience Cloud Identity (ECID) Service]](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) 版本2.0或更高版本。 的 [!DNL Identity Service] 提供了一个通用的永久性ID，用于在Experience Cloud的所有解决方案中标识您的访客。

   实施包括添加 [!DNL Identity service] 代码到广告商网站上的每个网页。

* 组织必须 [为Experience Cloud服务启用](https://experienceleague.adobe.com/docs/core-services/interface/services/core-services.html) 并拥有Experience Cloud [!DNL Organization ID] (以前称为 [!DNL IMS org ID])。

   的 [!UICONTROL Organization ID] 允许具有多个Adobe Experience Cloud产品的组织在某些产品之间共享数据。

* (具有 [!DNL Analytics])广告商必须 [实施 [!DNL Analytics] 使用 `appMeasurement.js`](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html) 版本1.6.4或更高版本。

* 广告商的网站访客不包含大量 [!DNL Apple Safari] 用户。

* (当广告商同时使用Audience Manager和 [!DNL Analytics])要减少对每个网页的调用，请删除现有Audience Manager [!DNL Data Integration Library] 用于数据收集的代码，并为每个 [!DNL Analytics] 报表包。 有关更多信息，请参阅[服务器端转发概述](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

* （推荐）为了获得更高的匹配率，请仅将第一方网站数据发送到Adobe广告。 如果广告商捆绑来自客户关系管理系统的第三方数据或离线数据，则数据泄漏可能会降低匹配率。

## 将Audience Manager受众导入DSP

### 将受众导入DSP的步骤

的 [!DNL Adobe] 帐户和数据运营团队将执行以下步骤。

1. 的 [!DNL Adobe] 帐户团队应配置广告商级别的设置“[!UICONTROL Adobe Analytics Cloud].&quot;

1. 的 [!DNL Adobe] 帐户团队应提交请求<!-- Submit a request as a JIRA task? --> 到数据运营团队<!-- implementation team? --> 使用Advertising DSP本机API集成导入组织的Audience Manager区段。

### 哪些更改会导致Audience Manager?

API会自动：

* 在Audience Manager中创建两个DSP目标：

   * **[!UICONTROL Adobe Ad Cloud Cross-Channel (real-time)]**

   * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)])**

* 将两个目标映射到所有Audience Manager区段，从而允许Audience Manager与与同一Experience Cloud关联的DSP广告商帐户共享区段 [!DNL Organization ID] 用于Audience Manager。 <!-- Verify -->

   组织可以选择从Audience Manager的目标中删除不需要的区段。

* 在组织的Audience Manager容器中添加以下exchange Cookie同步像素，以提高客户促销活动的覆盖范围：

   * AdobeAdCloud:411 [!DNL Identity Service] 版本2.0.具有 [!DNL Identity Service] 低于2.0版本时，应将此像素添加到其Audience Manager容器。

## 将Audience Manager受众导入 [!DNL Search]

### 将受众导入的步骤 [!DNL Search]

[!DNL Adobe] 人员将执行以下大部分或全部步骤。

1. 的 [!DNL Adobe] 客户团队应向数据运营团队提交请求，以设置 [!DNL Search] 和Audience Manager。 包括要导出到的Audience Manager区段的名称 [!DNL Search].

1. 在Audience Manager中，为 [!DNL Search]:

   1. 创建两个新目标： `[!UICONTROL Adobe Media Optimizer (HTTP)]` 和 `[!UICONTROL Adobe Media Optimizer Batch Destination]`.

      [!DNL Media Optimizer] 以前是 [!DNL Search].

   1. 为每个目标指定区段。

      使用 [!UICONTROL Automatically map all current and future segments] 选项，则所有区段都会每天进行映射和同步。

      的 [!UICONTROL Manually map segments] 选项允许您手动映射要与批处理目标同步的区段(`[!UICONTROL Adobe Media Optimizer Batch Destination]`)。 无需手动将区段映射到HTTP目标。

1. 在 [!DNL Search]，或 [!DNL Search] 实施团队或具有直接访问客户端管理员角色的用户应从启动导入 [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup].

   您需要输入组织的Experience Cloud [!DNL Organization ID] ([!DNL IMS org ID])。 ID必须与组织Audience Manager帐户使用的ID相同。

### 哪些更改会导致Audience Manager?

组织将看到两个 [!DNL Search] Audience Manager中的目标：

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination])**

## 数据同步

初始导入大约需要24小时。 初始导入后，数据会实时同步，延迟时间为一到两秒。

<!--
### How DSP Syncs the Data

DSP syncs the data automatically using the [!DNL Adobe Experience Cloud Identity (ECID) Service]. During synchronization, the [!DNL ECID Service] calls Adobe Advertising at [!DNL cm.eversttech.net]. Because Adobe Advertising is a trusted domain, ID syncs take place from parent pages rather than within the destination publishing iframes, as they do with most third-party activation partners. Audience Manager identifies unique users by device IDs, using the [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html#global-device-ids), also called the [!DNL Device ID].
 
![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)

### How Search Syncs the Data
-->

<!-- 
Segment membership data is sent only after one of the following events occurs:

* (Advertisers with DSP):

  * The segment is targeted in an Adobe Advertising display ad.

  * The segment is added to the [!DNL Adobe AdCloud Cross-Channel] batch and real-time destinations within the Audience Manager user interface.

* (Advertisers with [!DNL Search]):

  * The segment is targeted in an Adobe Advertising search ad.

  * The segment is added to the [!DNL Adobe Media Optimizer] batch and HTTP destinations within the Audience Manager user interface.
 -->
<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

## 在何处查找已同步的区段

### 在DSP中

在DSP中，区段名称由Audience Manager分类组织，并可与中相应的区段成员资格计数一起使用：

* [版面设置](/help/dsp/campaign-management/placements/placement-settings.md#audience-targeting):在 [!UICONTROL Adobe Segments] 选项卡 [!UICONTROL Audience Targeting] 中。

* 在 [受众设置](/help/dsp/audiences/audience-settings.md):在 [!UICONTROL Adobe Segments] 选项卡。

### 在广告创意中

在 [!DNL Creative]，则目标节点的体验设置中会提供这些区段。

### 在 [!DNL Advertising Search]

在[!DNL中 [!DNL Search]]，在创建 [!DNL Google] 受众使用 [!UICONTROL Data Source] &quot;[!UICONTROL Adobe Audience]从 [!UICONTROL Campaigns] > [!UICONTROL Audiences] > [!UICONTROL Library].

对于 [!DNL Google] 受众， [!DNL Google] 提供受众大小。

>[!MORELIKETHIS]
>
>* [Adobe与Adobe Audience Manager的广告集成](/help/integrations/audience-manager/overview.md)

