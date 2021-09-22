---
title: Advertising Cloud DSP中的促销活动管理概述
description: 了解营销活动管理层次结构和组件。
feature: DSP Packages, DSP Placements, DSP Ads
exl-id: c94e08d0-0dd5-4cf9-8df2-9eb4c591375c
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 0%

---

# Advertising Cloud DSP中的促销活动管理概述

Advertising Cloud DSP营销活动具有以下层次结构：

* Campaign
   * 包
      * 版面
         * 广告
            * 创意

<!-- Add "Feature: DSP Creatives" once we have other topics on creatives; get Bob to update the feature list. -->
<!-- Do clients think in terms of insertion orders? If yes, then work in the following info.:
In Advertising Cloud DSP, an insertion order is represented as a campaign, and line items are represented as packages. Each package will include placements, which can use different strategies and tactics to deliver the line item requirements.
-->

## [!UICONTROL Campaigns]

[](/help/dsp/campaign-management/campaigns/campaign-about.md) Campaign是飞行设置的总体框架。每个营销活动都配置了广告商、开始和结束日期、总体预算、跨设备定位选项和默认频率上限，以及可见性、欺诈、品牌安全和受众验证的报告选项。 所有营销活动级别的设置都会自动应用于营销活动中的每个包和版面。

## [!UICONTROL Packages]

每个营销活动可以包含一个或多个[包](/help/dsp/campaign-management/packages/package-about.md)，每个包都包含一组投放。

使用包对投放进行分组，以便交付到设定的预算、性能目标和自定义步调策略。 DSP通过将预算转移到包中性能最佳的版面来优化包。 您可以按版面格式、库存类型、数据提供商、角色或其他可识别特性来组织包。

包是可选的，但建议使用。

## [!UICONTROL Placements]

[placement](/help/dsp/campaign-management/placements/placement-about.md)存储同一广告类型的一个或多个广告的定位参数。 您可以为单个促销活动或包创建版面，然后为其分配广告。

## [!UICONTROL Ads]

[](/help/dsp/campaign-management/ads/ad-about.md) 包括创意资产和跟踪URL。您可以上传创意资产，并且DSP将免费提供使用这些资产的广告，也可以上传第三方广告投放标记。

设置广告后，您需要将每个广告附加到版面。 您可以将单个广告附加到一个或多个版面。

在活动营销活动中的活动投放中，所有活动的已批准广告都有资格根据投放定位参数运行。

## [!UICONTROL Creatives]

您可以上传音频和视频文件，以在指定促销活动的广告中使用。
<!-- add link to [About Creative Management](/help/dsp/campaign-management/creatives/creative-about.md) when it's available-->

您可以立即使用上传的创意创建广告，也可以稍后从创意视图或广告视图创建广告。

>[!MORELIKETHIS]
>
>* [关于营销活动管理](/help/dsp/campaign-management/campaigns/campaign-about.md)
>* [关于包管理](/help/dsp/campaign-management/packages/package-about.md)
>* [关于版面管理](/help/dsp/campaign-management/placements/placement-about.md)
>* [关于广告管理](/help/dsp/campaign-management/ads/ad-about.md)
>* [营销活动启动核对清单](/help/dsp/campaign-management/campaign-launch-checklist.md)
>* [设置效果促销活动的最佳实践](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [关于平台内报表](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [关于Campaign数据视图](/help/dsp/campaign-management/reports/campaign-data-views-about.md)

