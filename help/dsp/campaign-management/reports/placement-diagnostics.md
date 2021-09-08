---
title: 查看版面诊断报告
description: 了解如何诊断置入设置和步调问题。
feature: Placements
exl-id: d64406b6-83b5-4ae7-984c-98610fc1ee40
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# 查看版面诊断报告

<!-- Does this really belong in the Campaign Management > Reports section or in the Placements section? -->

在营销活动上线后，以下工具可帮助您诊断投放设置和步调问题：

* **[!UICONTROL Change Log]:** 显示对关键位置设置（如名称、状态和最高竞价）的更改。每个条目都包括做出更改的人员的日期和用户名。
* **[!UICONTROL Ad Approvals]:** 显示广告是否被库存提供商批准或拒绝。您可以选择更改任何广告的状态（例如，暂停已拒绝的广告）或打开广告设置。
* **[!UICONTROL Non Bids]:** 显示DSP未对版面进行竞价的原因。

1. 打开诊断报告：
   1. 打开版面设置：
      1. 在主菜单中，单击&#x200B;**[!UICONTROL Campaigns]**。
      1. 单击营销活动的名称，然后单击&#x200B;**[!UICONTROL Placements]**。
      1. 在版面名称旁边，单击&#x200B;**[!UICONTROL ...]>[!UICONTROL Edit]**。
   1. 单击右上角的![放置诊断](/help/dsp/assets/placement-diagnostics.png)或&#x200B;**[!UICONTROL Diagnostic]**。
1. 执行以下任一操作：
   * 要查看更改日志，请执行以下操作：
      1. 单击 **[!UICONTROL Change Log]**.
      1. （可选）过滤报表结果：
         * 在日期菜单中，将报表时段从默认的最近14天更改为其他时段（*[!UICONTROL Last 30 days]、* *[!UICONTROL Last 60 days]、* *[!UICONTROL Last 90 days]、*&#x200B;或&#x200B;*[!UICONTROL Last 1 year]*）。
         * 在左侧菜单中，按特定用户名过滤报表。
         * 在右侧菜单中，按特定的放置设置过滤报表。
   * 要查看广告批准的状态，请执行以下操作：
      1. 单击右上方的&#x200B;**[!UICONTROL Ad Approvals]**。
      1. （可选）要暂停或激活广告，请单击“广告”列中的状态开关（![状态开关](/help/dsp/assets/status-switch.png)）。
      1. （可选）要打开广告的设置，请单击广告旁边的&#x200B;**[!UICONTROL View Ad]**。
   * 要了解DSP为何未对版面进行竞价，请执行以下操作：
      1. 单击右上方的&#x200B;**[!UICONTROL Non Bids]**。
      1. （可选）要更改日期范围，请单击日期字段，然后选择其他日期或日期范围。

<!-- Later, add link to >* Definitions for NBRs (Reading No Bid Reports (NBRs)) -->

>[!MORELIKETHIS]
>
>* [关于平台内报表](campaign-reports-about.md)
>* [版面设置](/help/dsp/campaign-management/placements/placement-settings.md)

