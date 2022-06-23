---
title: Advertising Cloud DSP的新增功能
description: 本页介绍Advertising Cloud DSP中的新增功能和最近更改的功能。
cloud: Experience Cloud
product: advertising cloud
index: true
exl-id: d4b67393-e8c5-4170-92eb-bcf643ba3ec3
source-git-commit: 602d2dd36a83f5f438c444e8ccaaec92054f0186
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 新增功能

以下是新增功能或最近更改的功能。

| 日期 | 功能 | 描述 | 有关详细信息 |
| ---- | ------- | ----------- | -------------------- |
| 2022年5月31日 | 受众源 | （测试版功能）Advertising Cloud DSP现在可以摄取由在客户数据平台(CDP)中构建的经过验证的信号组成的第一方区段。 | 请参阅“[关于从受众源激活经过身份验证的区段](/help/dsp/audiences/sources/source-about.md).&quot; |
| 2022年5月25日 | 优化目标 | 现在，视频和本机版面可以包含在具有自定义目标“最高ROAS”和“最低CPA”的包中。 | 请参阅“[优化目标及其使用方法](/help/dsp/optimization/optimization-goals.md).&quot; |
| 2022年4月12日 | Campaign Management | 广告规范已更新，以反映当前支持。 | 请参阅“[支持的广告类型的规范](/help/dsp/campaign-management/ads/ad-specs.md).&quot; |
| 2022年2月17日 | 视频教程 | 新增了有关“如何创建标准显示版面”的视频。 | 请参阅 [Advertising CloudTutorials](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/dsp/placement-create.html). |
| 2022年1月31日 | 帮助 | 有关 [!DNL Deal IDs] 和 [!DNL Simple Ad Serving] 现已可用。 | 请参阅“库存”>“专用库存”的子章节。 |
| 2021年12月10日 | 视频教程 | 提供了新的视频教程：“Advertising Cloud DSP简介”、“帐户结构和用户界面”、“如何创建包”、“如何批量上传第三方广告标签”和“如何使用批量编辑工具编辑版面”。 | 请参阅“[Advertising CloudTutorials](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/overview.html).&quot; |
| 2021年11月12日 | [!UICONTROL Deal IDs] | 在 [!UICONTROL Deal ID] 设置， &quot;[!DNL Rubicon]“(“)”已更改为“[!DNL Magnite DV+]，其中 [!DNL DV+] 表示显示、视频和其他格式，如音频。 这反映了 [!DNL Magnite] SSP. **注意：** [!DNL Magnite DV+] 仍列为“[!DNL Rubicon]“ [!UICONTROL Deal ID Inbox]. | 请参阅“[SSP合作伙伴](/help/dsp/inventory/ssp-partners.md).&quot; |
| 2021年10月27日 | 自定义报表 | 您现在可以创建和管理 [!DNL Amazon S3] 和不同类型的FTP交付位置(称为 *[!DNL report destinations]*，用于自定义报表。 配置报表目标后，您可以设置每个新的自定义报表，以将其提交到单个目标类型的一个或多个位置，或电子邮件收件人。 更新了 [!DNL Amazon S3] 和FTP凭据不会中断报表交付。<br><br>您的现有报表仍会发送到指定的电子邮件收件人。 要配置到其他报表目标的投放，请使用新目标创建新报表。 | 请参阅“[关于 [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md), &quot;[创建 [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-create.md), &quot;[[!UICONTROL Report Destination] 设置](/help/dsp/reports/report-destinations/report-destination-settings.md)、和[自定义报表设置](/help/dsp/reports/report-settings.md).&quot; |
|  | [!UICONTROL Packages], [!UICONTROL Placements]和 [!UICONTROL Ads] 视图 | 当您查看某一天的数据时，趋势图现在包含每小时数据。 将光标悬停在任意点上可查看该小时的数据。 | 请参阅“[单个营销活动报告](/help/dsp/campaign-management/reports/campaign-reports-about.md#single-campaign-reporting).&quot; |
|  | [!UICONTROL Placements] | 版面 [!UICONTROL Inspector] 现在包含 [!UICONTROL Inventory] 选项卡，其中显示了该版面的所有交易及其相关量度。 无需生成自定义报告，即可使用信息进行快速调整或解决问题。 | 请参阅“[版面 [!UICONTROL Inspector]](/help/dsp/campaign-management/reports/campaign-reports-about.md#placement-inspector).&quot; |
|  | [!UICONTROL Ads] | (有权包含 [!DNL Clearcast] 时钟编号)如果您使用附加到其他广告的时钟编号，则DSP不再显示错误。 **注意：**  最佳做法是为每个视频广告使用唯一的时钟号。 否则，发布者不会批准所有广告。 | — |
|  | [!UICONTROL Deal IDs] | 的 [!UICONTROL Deal ID] 设置和用户界面中的其他位置反映了 [!DNL Magnite] SSP:<br><ul><li>SSP &quot;[!DNL Tremor]&quot;([!DNL Telaria])现在为“[!DNL Magnite CTV].&quot;</li><li>在接下来的几周里， [!DNL Rubicon]“ ”将更改为“ ”[!DNL Magnite DV+]，其中 [!DNL DV+] 表示显示、视频和其他格式，如音频。</li></ul> | 请参阅“[SSP合作伙伴](/help/dsp/inventory/ssp-partners.md).&quot; |
|  | [!DNL Freewheel] 程序保证的交易 | 您现在可以提交广告并检查广告的状态 [!DNL Freewheel] 通过 [!UICONTROL Ads] 中。 以前，您只能通过 [!UICONTROL Deals] 中。 | 请参阅“[为程序化保证交易提交广告 [!DNL Freewheel]](/help/dsp/inventory/freewheel-submit.md)" and "[Check the Status of Ads for [!DNL Freewheel] 程序化保证交易](/help/dsp/inventory/freewheel-check-status.md).&quot; |
| 2021年10月7日 | 帮助 | 全部 [DSP和其他Advertising Cloud文档](https://experienceleague.adobe.com/docs/advertising-cloud.html) on [!DNL Experience League] 现在机器已翻译成所有可用语言。 要更改显示的语言，请使用任何页面左下角的“更改语言”菜单。<br>![更改语言](/help/dsp/assets/change-language.png) |
| 2021年9月30日 | 品牌安全 | （9月22日发布） [!DNL DoubleVerify] 品牌安全预竞价产品已更新为 [!DNL Brand Suitability Tiers]，允许广告商在特定区段的三个风险级别（低、中、高）之间进行选择，而无需避免特定主题的所有实例。 以前，区段不包含任何容差级别。<br><br>与新 [!DNL DoubleVerify] 区段结构中， DSP将您现有的品牌安全区段迁移到新的、推荐的 *媒体* — 级别区段。 您可以选择将区段层调整为 *低* 或 *高*.<br><br>**注意：** 少量区段列表没有层，但具有新名称，如“骚扰/间谍软件/恶意软件、Warez”>激励/恶意软件/混乱。” | — |
|  | 优化 | 已弃用以下优化目标和竞价前过滤器：<ul><li>优化目标：<ul><li>[!UICONTROL Always Max Bid & Highest Viewability Rate (Moat – GroupM)]</li><li>[!UICONTROL Always Max Bid & Highest Viewability Rate (Moat – MRC)]</li></ul><li>竞价筛选器目标：<ul><li>[!UICONTROL Viewability IAS]</li><li>[!UICONTROL Viewability Moat]</li></ul></ul> | 请参阅“[优化目标及其使用方法](/help/dsp/optimization/optimization-goals.md)&quot;和&quot;[版面级别的预竞价过滤器及其使用方法](/help/dsp/optimization/optimization-pre-bid-filters.md).&quot; |
| 2021年9月28日 | 促销活动管理视图 | A &quot;[!UICONTROL Creation date]“ ”列现在在自定义列集中可用于 [!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements]和 [!UICONTROL Ads] 视图。 您还可以过滤 [!UICONTROL Placements] 和 [!UICONTROL Ads] 查看次数 [!UICONTROL Creation date]. | 请参阅“[创建自定义列视图](/help/dsp/campaign-management/reports/column-view-create.md)&quot;和&quot;[过滤营销活动数据](/help/dsp/campaign-management/reports/campaign-data-filter.md).&quot; |
|  | 程序化保证交易 | （9月8日版）您现在可以编辑 [!UICONTROL Max Bid] 用于程序化保证(PG)交易的默认位置。 但是，由于PG交易始终具有固定的CPM，因此只有国际客户才应编辑 [!UICONTROL Max Bid] 考虑货币兑换费。 | — |
|  |  | （9月8日发布）具有“[!DNL FreeWheel Programmatic Guaranteed]“权限现在可以向 [!DNL FreeWheel Programmatic Creative API] 从 [!UICONTROL Ads] 视图或 [!UICONTROL Placements] 中。 您仍可以从 [!UICONTROL Deals] 中。 | —<!-- Add link to page on submitting ads to Freewheel once it's edited. --> |
| 2021年8月11日 | 竞价前可见性 | 竞价前可见性过滤器 [!DNL Oracle Advertising (Moat)] 现在可用于您的版面。 | 有关 [第三方集成以实现竞价前可见性](/help/dsp/introduction/features/brand-safety-media-quality.md#pre-bid-viewability) 和&quot;[版面级别的预竞价过滤器及其使用方法](/help/dsp/optimization/optimization-pre-bid-filters.md).&quot; |
| 7月15日 | 帮助 | 添加了关于Advertising Cloud DSP基金客户如何将购买媒体和服务的帐户记录在案的详细信息。 | 请参阅“[帐户资金](/help/dsp/introduction/billing/account-funding.md).&quot; |
| 2021年6月12日 | 帮助 | 广告策略已更新。 | 请参阅“[Adobe Advertising Cloud广告要求政策](/help/policies/ad-requirements-policy.md).&quot; |
| 2021年6月7日 | 帮助 | 有关如何通过编程保证的交易与 [!DNL FreeWheel]. | 请参阅“[在中设置程序化保证交易概述 [!DNL FreeWheel]](/help/dsp/inventory/freewheel-overview.md)," "[Submit an Ad for a Programmatic Guaranteed Deal to [!DNL FreeWheel]](/help/dsp/inventory/freewheel-submit.md)," "[Check the Status of Ads for [!DNL Freewheel] 程序化保证交易](/help/dsp/inventory/freewheel-check-status.md)、和[的错误代码 [!DNL FreeWheel] 广告提交](/help/dsp/inventory/freewheel-error-codes.md).&quot; |
| 2021年5月27日 | 帮助 | 可接受的与健康相关的受众区段和策略提供准则，以用作定位与健康相关的受众区段的替代方法。 | 请参阅“[可接受的健康区段指南](/help/policies/health-segment-guidelines.md).&quot; |
| 2021年5月26日 | 帮助 | 章节“与Adobe Experience Cloud集成”现在是单独的指南，可从 [Advertising Cloud文档主页](https://experienceleague.adobe.com/docs/advertising-cloud.html). 新指南包含新的子章节“在 [!DNL Analytics Marketing Channels].&quot;<br>本DSP指南的目录包含指向新指南的链接。 | 请参阅“[与Adobe Experience Cloud集成](/help/integrations/home.md).&quot; |
| 2021年5月24日 | 帮助 | 在“Campaign Management”一章中，提供了有关如何使用Excel QA电子表格查看和编辑营销活动关键版面设置的新主题。 | 请参阅“[关于使用电子表格更正促销活动的版面设置](/help/dsp/campaign-management/qa/qa-about.md), &quot;[下载营销活动的版面设置](/help/dsp/campaign-management/qa/qa-sheet-download.md), &quot;[营销活动的上传版面设置](/help/dsp/campaign-management/qa/qa-sheet-upload.md)和“[已下载/已上载电子表格中的列](/help/dsp/campaign-management/qa/qa-sheet-columns.md). |
| 2021年5月5日 | 包设置 | 提供了新的步调填充策略选项“略微提前”，它是新包的默认选项。 此策略可加快投放速度，使其在飞行时长的一半完成55-65%。 | 请参阅“[包设置](/help/dsp/campaign-management/packages/package-settings.md).&quot; |
| 2021年3月17日 | 帮助 | &quot;Campaign Management&quot;一章已扩大，包括更多程序和参考。 | 在目录中，打开“Campaign Management”章节和子部分。 |
| 2021年3月10日 | 库存 | 您无法再创建 [!UICONTROL Smart Ad Serving] 使用VAST标记的交易。 相反，请咨询您的发布者，他们是否可以通过交易ID运行您的私人交易。 您可以使用 [!UICONTROL Deal ID inbox] 或手动输入交易详细信息。<br><br>您现有的智能广告服务交易仍然可用，但今年晚些时候将停用。 | 请参阅“[关于 [!UICONTROL Deal ID inbox]](/help/dsp/inventory/deal-id-inbox-about.md)&quot;和&quot;[手动创建 [!UICONTROL Deal ID] 详细信息](/help/dsp/inventory/deal-id-create.md)&quot; |
| 2021年2月25日 | 帮助 | 有关 [!DNL Analytics for Advertising Cloud]，它集成了Adobe Analytics和Adobe Advertising Cloud，可用。 | 有关集成的概述，请参阅[概述 [!DNL Analytics for Advertising Cloud]](/help/integrations/analytics/overview.md).&quot; 有关完整文档，请参阅“与Adobe Experience Cloud集成”>“[!DNL Analytics for Advertising Cloud].&quot; |
| 2020年10月28日 | 新帮助 | 旧版帮助已替换为更新的页面，这些页面可从 [!DNL DSP] 主菜单，也可随时从 [https://experienceleague.adobe.com/docs/advertising-cloud/dsp/home.html](https://experienceleague.adobe.com/docs/advertising-cloud/dsp/home.html). | — |
|  | 促销活动 | 上一个 [!UICONTROL Campaigns Beta] 视图现在为默认视图 [!UICONTROL Campaigns] 视图、更快的分析、简化的工作流和自定义视图。<br><br>新 [!UICONTROL Campaigns] 视图包括：<ul><li>新导航。 您可以查看帐户中所有营销活动的列表。 在营销活动中，您可以根据营销活动实体过滤数据： [!UICONTROL Packages], [!UICONTROL Placements]和 [!UICONTROL Ads].<br><br>![促销活动实体选项卡](/help/dsp/assets/campaign-subtabs.png)</li><li>允许您最多比较三个量度的数据可视化图表。<br><br>![三个量度的单独趋势图](/help/dsp/assets/trend-chart-separate.png)</li><li>能够创建和管理预定义的自定义列视图 [!UICONTROL Pacing] 和 [!UICONTROL Performance] 视图。<br><br>![列视图选择器](/help/dsp/assets/column-view-selector.png)</li><li>升级了搜索和筛选。</li></ul><br>旧版 [!UICONTROL Campaigns Classic] 视图仍然可从右上角的“配置文件”菜单访问。 要打开 [!UICONTROL Campaigns Classic] 视图，单击 **[!UICONTROL Switch to Campaigns Classic]**.<br><br>![链接至 [!UICONTROL Campaigns Classic]](/help/dsp/assets/switch-campaigns-classic.png)<br><br>返回 [!UICONTROL Campaigns] 在主页，单击 **[!UICONTROL Exit Classic]**. | 请参阅“[关于平台内报表](/help/dsp/campaign-management/reports/campaign-reports-about.md).&quot;<br><br>另请参阅“[关于Campaign数据视图](/help/dsp/campaign-management/reports/campaign-data-views-about.md).&quot; |
|  | 版面 | 删除了包含手动竞价规则的选项，以便DSP优化可以为您完成工作。 现在，所有现有的基于回访间隔的最大竞价都会自动优化。 | — |
|  |  | 为了提高整体性能，您无法再基于查看器的时区进行分时段。 现在，所有分时段功能都基于营销活动的时区&#x200B;。 | 请参阅“[版面设置](/help/dsp/campaign-management/placements/placement-settings.md).&quot; |
| 2020年10月15日 | 专用清单 | 现在，所有用户都可以使用新的交易ID表单来设置和编辑交易ID详细信息，该表单是旧版的简化版 [!UICONTROL Smart Ad Serving] 表单。 要设置新的交易ID详细信息，请转到 [!UICONTROL Inventory] > [!UICONTROL Deals]，单击 [!UICONTROL Create]，然后单击 [!UICONTROL Deal ID Beta]. | 请参阅“[手动创建交易ID详细信息](/help/dsp/inventory/deal-id-create.md)&quot;和&quot;[手动交易ID设置](/help/dsp/inventory/deal-id-settings.md).&quot; |
|  | 版面预测 | 对于具有投放级别步调的版面， [!UICONTROL Forecast] 版面设置的部分包含一个新 [!UICONTROL Estimated Maximums] 部分，指示当前定位配置中的可用容量。 | — |
| 2020年9月2日 | 报告 | 具有多个DSP帐户的任何组织都可以根据组织的需要，选择在自定义报表中启用跨帐户数据。 | 请参阅“[关于自定义报表](/help/dsp/reports/report-about.md#cross-account-reporting).&quot; |

{style=&quot;table-layout:auto&quot;}
