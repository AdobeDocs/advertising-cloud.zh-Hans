---
title: 复制版面
description: 了解如何复制一个或多个版面。
feature: DSP Placements
exl-id: d22a61a8-4f1b-41ee-b4fb-3124bec81a2f
source-git-commit: 5ed402a7c83072a7af6a06757050486c6d7d7080
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# 复制版面

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

复制一个或多个版面以创建具有类似设置的版面。 您可以：

* 创建多个重复的版面
* 在原始广告商和营销策划中或在不同的广告商和营销策划中复制版面
* （对于原始营销活动中的重复投放）（可选）复制原始广告
* 修改新版面的状态和投放日期

请参阅“[未复制的内容](#placement-not-duplicated)“ ”，查看未复制的版面设置列表。

1. 在主菜单中，单击 **[!UICONTROL Campaigns]**.
1. 单击营销活动的名称。
1. 在子菜单中，单击 **[!UICONTROL Placements]**.
1. 执行以下任一操作：
   * 要复制一个版面，请单击  **[!UICONTROL ...]>[!UICONTROL Duplicate]** 包名称旁边的。
   * 要复制多个版面，请执行以下操作：
      1. 选中要复制的每个版面旁边的复选框。
      1. 在批量操作工具栏中，单击 **[!UICONTROL Duplicate]**.
1. 指定新的版面设置：
   1. （单个版面）输入新版面名称。
   1. 在 **[!UICONTROL Choose Package (Required)]** 菜单，选择父包或**[!UICONTROL No package]*.
   1. （可选）更改默认设置。

   设置适用于所有选定的版面。

   默认情况下，新投放是针对原始广告类型的，会分配给原始广告商和促销活动，并且具有从当天开始的飞行时间表，会暂停，并且不包含原始广告。

   创建多个版面时，新版面名称会依次使用约定&lt;*original_placement_name #N*>，如“我的版面#2”。

1. 单击 **[!UICONTROL Submit]**.

## 未复制的内容 {#placement-not-duplicated}

原始版面中的所有设置都会复制，但以下各项除外：

* 实验设置
* （如果更改投放日期）自定义广告计划
* （如果不附加广告）自定义广告权重和计划
* 程序化保证(PG)交易的默认版面和 [!UICONTROL Simple Ad Serving] 交易
* （如果您将版面复制到其他营销活动）：
   * 地域目标
   * 事件像素
   * 广告
   * 版面级别 [!DNL DoubleVerify Authentic Brand Safety] 区段（覆盖广告商级别的区段）

>[!MORELIKETHIS]
>
>* [关于版面管理](placement-about.md)
>* [创建版面](placement-create.md)
>* [编辑版面](placement-edit.md)
>* [查看版面的更改日志](placement-change-log.md)
>* [版面设置](placement-settings.md)

