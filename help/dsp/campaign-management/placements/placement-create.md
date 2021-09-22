---
title: 创建版面
description: 了解如何创建版面。
feature: DSP Placements
exl-id: 4e37b571-9af4-4897-bff2-035a5f2600a5
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 1%

---

# 创建版面

>[!TIP]
>
>根据特定促销活动目标或报告需求创建投放。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Campaigns]**。

1. 单击将包含版面的营销活动名称。

1. 在数据表上方，单击&#x200B;**[!UICONTROL Create]**。 在菜单的[!UICONTROL Placement Types]部分中，单击放置类型。

   版面类型确定版面可包含的广告类型。

1. 输入[版面设置](placement-settings.md):

   1. 指定[!UICONTROL Basics]设置。

   1. 在[!UICONTROL Goals]部分中，指定[!UICONTROL Gross Budget]，或者，指定其他版面目标。
某些字段具有可覆盖的默认值。

      如果向其分配投放的资源包具有资源包级别的步调，则您的目标和步调设置将反映资源包设置。

   1. （可选）在[!UICONTROL Geo-Targeting]部分中，缩小包含或排除的位置。

      如果您未识别特定位置，则会定位所有位置。

      >[!NOTE]
      >
      >城市和DMA位置不适用于Roku位置。

   1. 在[!UICONTROL Inventory Targeting]部分中，缩小要包含或排除的库存源。

      对于大多数版面类型，默认包含所有库存类型和每种类型的所有来源。 对于[!DNL Roku]版面，必须指定库存类型和来源。

   1. （可选）在[!UICONTROL Site Targeting]部分中，缩小要定位的站点，并指定要排除的任何站点。

   1. （可选）在[!UICONTROL Audience Targeting]部分中：

      1. 缩小受众范围。 这包括选择要在版面中定位的受众区段。

         对于[!DNL] Roku版面，您可以通过包含一个或多个可与[!DNL Roku]（选择加入）确定性数据集匹配的受众区段，来利用与 [!DNL Roku]](/help/dsp/inventory/roku-inventory.md)匹配的[DSP独特受众。
   1. (适用于具有人员级别跨设备定位的营销活动；（可选）当版面定向一个或多个特定受众时，为版面启用基于人员的跨设备定位。

      [!DNL LiveRamp]仅使用美国数据提供基于人员的跨设备定位。 对于使用[!DNL LiveRamp]设备图（即，在目标受众区段中未找到的设备）交付的展示次数，所有广告商均可以按0.35 CPM的价格获得该服务。

   1. （可选）在[!DNL Brand Safety and Media Targeting]部分中，对您的版面应用品牌安全限制。

   1. （可选）在[!DNL Tracking]部分，为投放的广告输入第三方事件像素或转化像素。

      >[!NOTE]
      >
      >（[!DNL Roku]位置）由[!DNL Roku]批准的第三方像素供应商包括[!DNL Acxiom]、[!DNL comScore]、[!DNL Data Plus Math]、[!DNL Experian]、[!DNL Factual]、[!DNL Kantar]、[!DNL Marketing Evolution]、[!DNL Neustar]、[!DNL Nielsen]、[!DNL Nielsen Catalina Solutions]、[!DNL NinthDecimal]、[!DNL Oracle]、[!DNL Placed]、[!DNL Polk]和[!DNL Research Now]。


1. 单击 **[!UICONTROL Create Placement]**.

1. （可选）将广告附加到投放：

   1. 单击 **[!UICONTROL Attach an ad]**.

   1. 执行以下任一操作：
   * 要创建新广告，请执行以下操作：

      1. 单击 **[!UICONTROL Create a New Ad].**

      1. 指定[音频广告](/help/dsp/campaign-management/ads/ad-settings-audio.md)、[连接的TV](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)、[显示广告](/help/dsp/campaign-management/ads/ad-settings-display.md)、[移动广告](/help/dsp/campaign-management/ads/ad-settings-mobile.md)、[本机广告](/help/dsp/campaign-management/ads/ad-settings-native.md)或[前置广告](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)的广告设置。

      1. 单击 **[!UICONTROL Save & Submit for Review]**.

      1. （可选）对于要为版面创建的每个其他广告，单击&#x200B;**[!UICONTROL Attach Another Ad]**，然后重复步骤1-3。

      1. 如果不附加任何现有广告，请单击&#x200B;**[!UICONTROL I'm done for now]**。
   * 要在营销活动中附加现有广告，请执行以下操作：

      1. 单击 **[!UICONTROL Select an Ad]**.
      1. 执行以下任一操作：
         * 要一次添加一个广告，请执行以下操作：
            1. 在广告名称旁边，单击&#x200B;**[!UICONTROL Select]。**
            1. （可选）对于要附加的每个附加广告，单击&#x200B;**[!UICONTROL Attach Another Ad]**，然后重复该过程。
         * 要一次最多添加20个广告，请执行以下操作：
            1. 选中广告列表上方的复选框。
            1. 选中要添加的每个广告旁边的复选框。
            1. 单击 **[!UICONTROL Attach]**.
            1. 在广告名称旁边，单击&#x200B;**[!UICONTROL Select]**。
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




>[!MORELIKETHIS]
>
>* [关于版面管理](placement-about.md)
>* [编辑版面](placement-edit.md)
>* [编辑版面的广告计划](placement-edit-ad-schedule.md)
>* [暂停或激活版面](placement-pause-activate.md)
>* [版面设置](placement-settings.md)
>* [键盘快捷键](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)

   >*[性能疑难解答](/help/dsp/optimization/troubleshooting-performance.md)

