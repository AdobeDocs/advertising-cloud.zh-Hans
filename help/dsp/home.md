---
title: Advertising Cloud DSP的新增功能
description: 本页介绍Advertising Cloud DSP中的新增功能和最近更改的功能。
cloud: Experience Cloud
product: advertising cloud
index: true
exl-id: d4b67393-e8c5-4170-92eb-bcf643ba3ec3
source-git-commit: ebb8c99da206fe17d5a15f4343b5ddd8485a59af
workflow-type: tm+mt
source-wordcount: '971'
ht-degree: 0%

---

# 新增功能

以下是新增功能或最近更改的功能。

| 日期 | 功能 | 描述 | 有关详细信息 |
| ---- | ------- | ----------- | -------------------- |
| 2021年9月30日 | 品牌安全 | （9月22日发布）[!DNL DoubleVerify]品牌安全投标前产品已更新为[!DNL Brand Suitability Tiers]，这允许广告商在特定区段的三个风险级别（低、中、高）之间进行选择，而无需避免特定主题的所有实例。 以前，区段不包含任何容差级别。 | — |
|  | 优化 | 已弃用以下优化目标和竞价前过滤器：<ul><li>优化目标：<ul><li>[!UICONTROL Always Max Bid & Highest Viewability Rate (Moat – GroupM)]</li><li>[!UICONTROL Always Max Bid & Highest Viewability Rate (Moat – MRC)]</li></ul><li>竞价筛选器目标：<ul><li>[!UICONTROL Viewability IAS]</li><li>[!UICONTROL Viewability Moat]</li></ul></ul> | 请参阅“[优化目标和如何使用它们](/help/dsp/optimization/optimization-goals.md)”和“[版面级别的预竞价过滤器以及如何使用它们](/help/dsp/optimization/optimization-pre-bid-filters.md)”。 |
| 2021年9月28日 | 促销活动管理视图 | “[!UICONTROL Creation date]”列现在在[!UICONTROL Campaigns]、[!UICONTROL Packages]、[!UICONTROL Placements]和[!UICONTROL Ads]视图的自定义列集中可用。 您还可以按[!UICONTROL Creation date]过滤[!UICONTROL Placements]和[!UICONTROL Ads]视图。 | 请参阅“[创建自定义列视图](/help/dsp/campaign-management/reports/column-view-create.md)”和“[过滤营销活动数据](/help/dsp/campaign-management/reports/campaign-data-filter.md)”。 |
|  | 程序化保证交易 | （9月8日版）现在，您可以编辑[!UICONTROL Max Bid]以获取程序化保证(PG)交易的默认位置。 但是，由于PG交易始终具有固定的CPM，因此只有国际客户才应编辑[!UICONTROL Max Bid]以考虑货币兑换费用。 | — |
|  |  | （9月8日发布）现在，具有“[!DNL FreeWheel Programmatic Guaranteed]”权限的用户可以从[!UICONTROL Ads]视图或[!UICONTROL Placements]视图向[!DNL FreeWheel Programmatic Creative API]提交广告。 您仍可以从[!UICONTROL Deals]视图提交广告。 | —<!-- Add link to page on submitting ads to Freewheel once it's edited. --> |
| 2021年8月11日 | 竞价前可见性 | [!DNL Oracle Advertising (Moat)]中的竞价前可见性过滤器现在可用于您的版面。 | 有关[第三方集成的更多信息，以了解竞价前可见性](/help/dsp/introduction/features/brand-safety-media-quality.md#pre-bid-viewability)和“[版面级别的竞价前过滤器以及如何使用它们](/help/dsp/optimization/optimization-pre-bid-filters.md)”。 |
| 7月15日 | 帮助 | 添加了关于Advertising Cloud DSP基金客户如何将购买媒体和服务的帐户记录在案的详细信息。 | 请参阅“[帐户资金](/help/dsp/introduction/billing/account-funding.md)”。 |
| 2021年6月12日 | 帮助 | 广告策略已更新。 | 请参阅“[Adobe Advertising Cloud广告要求策略](/help/policies/ad-requirements-policy.md)”。 |
| 2021年6月7日 | 帮助 | 有关使用程序化保证交易与[!DNL FreeWheel]上的发布者运行广告的说明。 | 请参阅“[在 [!DNL FreeWheel]](/help/dsp/inventory/freewheel-overview.md)中设置程序化保证交易概述”、“[向 [!DNL FreeWheel]](/help/dsp/inventory/freewheel-submit.md)提交程序化保证交易的广告”、“[检查 [!DNL Freewheel] 程序化保证交易](/help/dsp/inventory/freewheel-check-status.md)的广告状态”和“[ [!DNL FreeWheel] 广告提交](/help/dsp/inventory/freewheel-error-codes.md)的错误代码”。 |
| 2021年5月27日 | 帮助 | 可接受的与健康相关的受众区段和策略提供准则，以用作定位与健康相关的受众区段的替代方法。 | 请参阅“[可接受的健康区段准则](/help/policies/health-segment-guidelines.md)”。 |
| 2021年5月26日 | 帮助 | 章节“与Adobe Experience Cloud集成”现在是一个单独的指南，可从[Advertising Cloud文档主页](https://experienceleague.adobe.com/docs/advertising-cloud.html)获取。 新指南包含关于“在[!DNL Analytics Marketing Channels]中工作”的新子章节。<br>本DSP指南的目录包含指向新指南的链接。 | 请参阅“[与Adobe Experience Cloud的集成](/help/integrations/home.md)”。 |
| 2021年5月24日 | 帮助 | 在“营销活动管理”一章中，提供了有关如何使用Excel QA电子表格查看和编辑营销活动关键版面设置的新主题。 | 请参阅“[关于使用电子表格更正营销活动的版面设置](/help/dsp/campaign-management/qa/qa-about.md)、“[营销活动的下载版面设置](/help/dsp/campaign-management/qa/qa-sheet-download.md)、“[营销活动的上传版面设置](/help/dsp/campaign-management/qa/qa-sheet-upload.md)和“[已下载/已上载电子表格中的列](/help/dsp/campaign-management/qa/qa-sheet-columns.md)。 |
| 2021年5月5日 | 包设置 | 提供了新的步调填充策略选项“略微提前”，它是新包的默认选项。 此策略可加快投放速度，使其在飞行时长的一半完成55-65%。 | 请参阅“[包设置](/help/dsp/campaign-management/packages/package-settings.md)”。 |
| 2021年3月17日 | 帮助 | “促销活动管理”章节已扩展，包含更多程序和参考。 | 在目录中，打开“促销活动管理”章节和子部分。 |
| 2021年3月10日 | 库存 | 您无法再使用VAST标记创建[!UICONTROL Smart Ad Serving]交易。 相反，请咨询您的发布者，他们是否可以通过交易ID运行您的私人交易。 您可以使用[!UICONTROL Deal ID inbox]直接从发布者导入交易ID，或手动输入交易详细信息。<br><br>您现有的智能广告服务交易仍然可用，但今年晚些时候将停用。 | 请参阅“[关于[!UICONTROL Deal ID inbox]](/help/dsp/inventory/deal-id-inbox-about.md)”和“[手动创建[!UICONTROL Deal ID]详细信息](/help/dsp/inventory/deal-id-create.md)” |
| 2021年2月25日 | 帮助 | 提供了有关集成了Adobe Analytics和Adobe Advertising Cloud的[!DNL Analytics for Advertising Cloud]的文档。 | 有关集成的概述，请参阅“[ [!DNL Analytics for Advertising Cloud]](/help/integrations/analytics/overview.md)概述”。 有关完整文档，请参阅“与Adobe Experience Cloud集成”>“[!DNL Analytics for Advertising Cloud]”一章。 |
| 2020年10月28日 | 新帮助 | 旧版帮助页面已替换为更新页面，这些页面可从[!DNL DSP]主菜单的“帮助”链接获取，也可随时从[https://experienceleague.adobe.com/docs/advertising-cloud/dsp/home.html](https://experienceleague.adobe.com/docs/advertising-cloud/dsp/home.html)获取。 | — |
|  | 促销活动 | 以前的[!UICONTROL Campaigns Beta]视图现在是默认的[!UICONTROL Campaigns]视图，用于加快分析、简化工作流和自定义视图。<br><br>新视图 [!UICONTROL Campaigns] 包括：<ul><li>新导航。 您可以查看帐户中所有营销活动的列表。 在营销活动中，您可以根据营销活动实体过滤数据：[!UICONTROL Packages]、[!UICONTROL Placements]和[!UICONTROL Ads]。<br><br>![促销活动实体选项卡](/help/dsp/assets/campaign-subtabs.png)</li><li>允许您最多比较三个量度的数据可视化图表。<br><br>![三个量度的单独趋势图](/help/dsp/assets/trend-chart-separate.png)</li><li>能够创建和管理自定义列视图，其中包含预定义的[!UICONTROL Pacing]和[!UICONTROL Performance]视图。<br><br>![列视图选择器](/help/dsp/assets/column-view-selector.png)</li><li>升级了搜索和筛选。</li></ul><br>旧版视 [!UICONTROL Campaigns Classic] 图仍可从右上角的配置文件菜单访问。要打开[!UICONTROL Campaigns Classic]视图，请单击&#x200B;**[!UICONTROL Switch to Campaigns Classic]**。<br><br>![链接至 [!UICONTROL Campaigns Classic]](/help/dsp/assets/switch-campaigns-classic.png)<br><br>要返回 [!UICONTROL Campaigns] 主页，请单 **[!UICONTROL Exit Classic]**&#x200B;击。 | 请参阅“[关于平台内报表](/help/dsp/campaign-management/reports/campaign-reports-about.md)”。<br><br>另请参阅“[关于Campaign数据视图](/help/dsp/campaign-management/reports/campaign-data-views-about.md)”。 |
|  | 版面 | 删除了包含手动竞价规则的选项，以便DSP优化可以为您完成工作。 现在，所有现有的基于回访间隔的最大竞价都会自动优化。 | — |
|  |  | 为了提高整体性能，您无法再基于查看器的时区进行分时段。 现在，所有分时段功能都基于营销活动的时区&#x200B;。 | 请参阅“[版面设置](/help/dsp/campaign-management/placements/placement-settings.md)”。 |
| 2020年10月15日 | 专用清单 | 现在，所有用户都可以使用新的交易ID表单来设置和编辑交易ID详细信息，该表单是旧版[!UICONTROL Smart Ad Serving]表单的简化版本。 要设置新的交易ID详细信息，请转到[!UICONTROL Inventory] > [!UICONTROL Deals]，单击[!UICONTROL Create]，然后单击[!UICONTROL Deal ID Beta]。 | 请参阅“[手动创建交易ID详细信息](/help/dsp/inventory/deal-id-create.md)”和“[手动交易ID设置](/help/dsp/inventory/deal-id-settings.md)”。 |
|  | 版面预测 | 对于具有投放级别步调的投放，投放设置的[!UICONTROL Forecast]部分新增了[!UICONTROL Estimated Maximums]部分，其中指示了当前目标配置中的可用容量。 | — |
| 2020年9月2日 | 报告 | 具有多个DSP帐户的任何组织都可以根据组织的需要，选择在自定义报表中启用跨帐户数据。 | 请参阅“[关于自定义报表](/help/dsp/reports/report-about.md#cross-account-reporting)”中的“跨帐户报表”部分。 |
