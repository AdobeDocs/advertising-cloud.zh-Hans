---
title: 将广告附加到版面
description: 了解如何将广告附加到版面。
feature: Ads
exl-id: 4d85b89b-217f-46eb-a8b2-27da4c220be7
source-git-commit: fcd55f882f56c9eacd82d554d30364400b99555c
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 1%

---

# 将广告附加到版面

## 从[!UICONTROL Ads]视图附加新广告

1. 在主菜单中，单击&#x200B;**[!UICONTROL Campaigns]**。
1. 单击营销活动的名称。
1. 在子菜单中，单击&#x200B;**[!UICONTROL Ads]**。
1. 在广告名称旁边，单击&#x200B;**... >[!UICONTROL Add to Placements]**。
1. 在“置入广告”屏幕中，执行以下任一操作：
   * 要为广告创建新版面，请执行以下操作：
      1. 单击 **[!UICONTROL Create New Placement]**.
      1. 输入[放置设置](/help/dsp/campaign-management/placements/placement-settings.md)，然后单击&#x200B;**[!UICONTROL Create Placement]**。
   * 要将广告添加到一个或多个现有版面，请执行以下操作：
      1. 单击 **[!UICONTROL Select a Placement].**
      1. 执行以下任一操作：
         * 要一次添加一个广告，请执行以下操作：
            1. 在广告名称旁边，单击&#x200B;**[!UICONTROL Select]。**
            1. （可选）对于要附加的每个广告，单击&#x200B;**[!UICONTROL Attach to Other Placement]**。 在广告名称旁边，单击&#x200B;**[!UICONTROL Select]。**
         * 要一次将广告附加到最多20个版面，请执行以下操作：
            1. 选中**批量选择旁边的复选框。”
            1. 选中要将广告附加到的每个版面旁边的复选框。
            1. 单击 **[!UICONTROL Attach]**.
      1. 在“完成并审阅”选项卡中，选择以下选项之一：
         * 要返回到“广告”视图，请单击&#x200B;**[!UICONTROL I'm done for now]**。
         * 要将广告附加到其他版面，请单击&#x200B;**[!UICONTROL Attach To Other Placement]**。

## 从[!UICONTROL Placements]视图附加新广告或现有广告

1. 在主菜单中，单击&#x200B;**[!UICONTROL Campaigns]**。
1. 单击营销活动的名称。
1. 在子菜单中，单击&#x200B;**[!UICONTROL Placements]**。
1. 在版面名称旁边，单击&#x200B;**... > [!UICONTROL Attach Ads].**
1. 在[!UICONTROL Add Ad to Placement]屏幕中，执行以下任一操作：
   * 要创建新广告，请执行以下操作：
      1. 单击 **[!UICONTROL Create a New Ad]**.
      1. 输入[音频广告](ad-settings-audio.md)、[连接的TV](ad-settings-connected-tv.md)、[显示广告](ad-settings-display.md)、[移动广告](ad-settings-mobile.md)、[本机广告](ad-settings-native.md)或[前置广告](ad-settings-pre-roll.md)的广告设置。
      1. 单击 **[!UICONTROL Save & Submit for Review]**.

         新广告的[广告审阅](ad-about.md)需要24-48小时，其中包括检查敏感类别、单击URL功能和预览渲染。 [!UICONTROL Status]列指示DSP是否批准了该广告。 断开的广告可能具有超过24-48小时的待处理状态，因此您有时间修复错误，然后才能拒绝它们。

         >[!NOTE]
         >
         >仅当DSP和SSP都批准了创作元素时，才会提供您的广告。 每个SSP都有自己的批准要求和流程。
   * 要选择现有广告，请执行以下操作：
      1. 单击 **[!UICONTROL Select an Ad].**
      1. 指定广告：
         * 要一次添加一个广告，请执行以下操作：
            1. 在广告名称旁边，单击&#x200B;**[!UICONTROL Select]。**
            1. （可选）对于要附加的每个广告，单击&#x200B;**[!UICONTROL Add Another Ad]**。 在广告名称旁边，单击&#x200B;**[!UICONTROL Select]。**
         * 要一次最多添加20个广告，请执行以下操作：
            1. 选中&#x200B;**[!UICONTROL Bulk Select]**&#x200B;旁边的复选框。&quot;
            1. 选中要添加的每个广告旁边的复选框。
            1. 单击 **[!UICONTROL Attach]**.
      1. （可选）要覆盖版面中特定广告的默认投放期和广告轮换：
         1. 单击 **[!UICONTROL Custom Schedule Ads]**.
         1. 执行以下任一操作：
            * 要添加投放，请单击&#x200B;**[!UICONTROL Add Flight]**，然后指定开始日期和结束日期。
            * 要向广告添加现有投放，请单击投放列广告行中的&#x200B;**[!UICONTROL +]**。
            * 要从广告中删除现有投放，请单击投放列广告行中的&#x200B;**[!UICONTROL x]**。
            * （当多个广告具有相同的投放时）要使广告不均匀地旋转，请单击投放信息中的&#x200B;**[!UICONTROL Even Rotation]**，然后输入每个广告旋转的相对权重（以百分比表示）。
总重量必须等于100。
         1. 单击右上方的&#x200B;**[!UICONTROL Continue]**。
         1. 查看飞行详细信息，然后单击&#x200B;**[!UICONTROL Save & Finish]**。
      1. 单击 **[!UICONTROL I'm done for now]**.


>[!MORELIKETHIS]
>
>* [关于广告管理](ad-about.md)
>* [创建广告](ad-create.md)
>* [编辑广告](ad-edit.md)
>* [列出与广告关联的版面](ad-list-placements.md)
>* [编辑版面的广告计划](/help/dsp/campaign-management/placements/placement-edit-ad-schedule.md)

