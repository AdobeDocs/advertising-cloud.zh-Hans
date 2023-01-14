---
title: Campaign Management在Advertising DSP中的概述
description: 了解营销活动管理层次结构和组件。
feature: DSP Packages, DSP Placements, DSP Ads
exl-id: c94e08d0-0dd5-4cf9-8df2-9eb4c591375c
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 0%

---

# Campaign Management在Advertising DSP中的概述

DSP促销活动具有以下层次结构：

* Campaign
   * 包
      * 版面
         * 广告

<!-- Do clients think in terms of insertion orders? If yes, then work in the following info.:
In Advertising DSP, an insertion order is represented as a campaign, and line items are represented as packages. Each package will include placements, which can use different strategies and tactics to deliver the line item requirements.
-->

## [!UICONTROL Campaigns]

[促销活动](/help/dsp/campaign-management/campaigns/campaign-about.md) 是飞行设置的总体框架。 每个营销活动都配置了广告商、开始和结束日期、总体预算、跨设备定位选项和默认频率上限，以及可见性、欺诈、品牌安全和受众验证的报告选项。 所有营销活动级别的设置都会自动应用于营销活动中的每个包和版面。

## [!UICONTROL Packages]

每个营销活动可包含一个或多个 [软件包](/help/dsp/campaign-management/packages/package-about.md)，其中每个版面都包含一组版面。

使用包对投放进行分组，以便交付到设定的预算、性能目标和自定义步调策略。 DSP通过将预算转移到包中性能最佳的版面来优化包。 您可以按版面格式、库存类型、数据提供商、角色或其他可识别特性来组织包。

包是可选的，但建议使用。

## [!UICONTROL Placements]

A [投放](/help/dsp/campaign-management/placements/placement-about.md) 存储同一广告类型的一个或多个广告的定位参数。 您可以为单个促销活动或包创建版面，然后为其分配广告。

## [!UICONTROL Ads]

[广告](/help/dsp/campaign-management/ads/ad-about.md) 包括创意资产和跟踪URL。 您可以使用合作伙伴标签表或批量标签模板单独或批量上传第三方广告服务标签。 您还可以手动创建本机显示广告，以便DSP提供。

设置广告后，您需要将每个广告附加到版面。 您可以将单个广告附加到一个或多个版面。

在活动营销活动中的活动投放中，所有活动的已批准广告都有资格根据投放定位参数运行。

>[!MORELIKETHIS]
>
>* [关于Campaign Management](/help/dsp/campaign-management/campaigns/campaign-about.md)
>* [关于包管理](/help/dsp/campaign-management/packages/package-about.md)
>* [关于版面管理](/help/dsp/campaign-management/placements/placement-about.md)
>* [关于广告管理](/help/dsp/campaign-management/ads/ad-about.md)
>* [营销活动启动核对清单](/help/dsp/campaign-management/campaign-launch-checklist.md)
>* [设置效果促销活动的最佳实践](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [关于平台内报表](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [关于Campaign数据视图](/help/dsp/campaign-management/reports/campaign-data-views-about.md)
>* [视频：DSP帐户结构和用户界面](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/dsp/ui.html)

