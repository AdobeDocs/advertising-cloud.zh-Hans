---
title: 品牌安全与媒体质量
description: 进一步了解品牌安全和媒体质量功能。
feature: DSP Introduction
exl-id: df5be5d4-490e-479f-b76d-4fda4acd4201
source-git-commit: b436936e3a0edcb78497fadb6f3c4086412baaa5
workflow-type: tm+mt
source-wordcount: '1365'
ht-degree: 0%

---

# 品牌安全与媒体质量

<!-- Check on logo sizes in staging environment -- I made them all 100 pixels high except for DoubleVerify, which is 150 (harder to see at 100), but some instances look larger in VS Code. -->

Advertising Cloud DSP提供一套品牌保护功能，以确保您的每个营销活动在品牌安全的环境中面向实际用户。

我们的欺诈监控团队与行业领先的合作伙伴(例如 [!DNL Interactive Advertising Bureau], [!DNL Trust and Accountability Group] [!DNL (TAG)]和 [!DNL WhiteOps]，以仔细策划我们平台上的清单。 通过主动预防性地管理我们的供应， DSP可确保平台中的所有广告商都免受非人类流量（机器人、爬网程序、数据中心流量和欺诈）的影响，并仅在品牌安全的环境中提供。

除提供中央质量管理外，我们相信增强广告商的能力，使其能够设计与其品牌相符的控制。 Adobe Advertising Cloud提供与 [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], [!DNL Oracle Data Cloud]和 [!DNL Peer39]，确保每个广告商都可以选择所需的欺诈保护级别、情境过滤和关键词定位。

## Advertising Cloud DSP质量计划

### 库存验证 [!DNL Ads.txt] 支持

[[!DNL Ads.txt]，表示 [!DNL Authorized Digital Sellers]](https://iabtechlab.com/ads-txt) 是由 [!DNL Interactive Advertising Bureau] ([!DNL IAB])，以促进在公开市场上正确呈现库存，从而打击非法的流量来源和域欺骗。 参与的出版商和分销商通过维护 `ads.txt` 页面(例如 `example.com/ads.txt`)。

DSP支持 [!DNL ads.txt] 阅读每位出版商的 `ads.txt` 文件，并允许您选择仅从已验证的 [!DNL ads.txt] 卖家。 例如，通过匹配我们看到访问的卖家 `nytimes.com` 到《纽约时报》 `ads.txt` 文件中，我们可以识别哪些是合法的，哪些是不合法的，并且如果该职位配置为仅向经验证的卖家购买，我们将阻止违规者。 <!-- can we actually mention NY Times? -->

您可以设置默认 [!DNL ads.txt] 每个广告商的控件<!-- [default ads.txt controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->，然后（可选） [自定义每个版面的设置](/help/dsp/campaign-management/placements/placement-settings.md) 至：

* 仅从域的授权直销商处购买库存

* 仅向域的授权直销商和经销商购买库存

* 优先从域的授权直销商和经销商购买库存

* 从所有卖家处购买库存

### 平台欺诈监控

DSP已构建了强大的内部工具和系统来管理我们整个平台中的欺诈行为，并与诸如 [!DNL Whiteops] 和 [!DNL Integral Ad Science].

此外，Adobe与 [!DNL IAB] 和 [!DNL TAG] 以确保利用诸如 [!DNL ads.txt] （请参阅上一节）、 [!DNL IAB] 机器人和蜘蛛程序列表，以及 [!DNL TAG] 数据中心IP列表。

通过我们的多维质量方法，我们的团队可以监控异常和无效流量模式，从而确保受保护库存上的无效流量少于3%。 任何可疑的清单（包括特定域的清单或来自特定发布者或销售者的清单）会立即在整个平台上被阻止。

### 库存映射、分层和分类

库存映射是所有新库存在添加到我们平台之前，需要进行的详细审核和载入过程。 此流程旨在确保DSP上所有库存的安全和质量。

* **映射：** 我们的库存团队仔细审查了每个域，并评估了以下方面：

   * 品牌安全

   * 广告类型验证

   * 通用内容、重复域和虚假广告服务

* **分层：** 我们全面地检查整个生态系统中的品牌存在情况，以跨不同层对库存进行分类。 您可以 [定位您的投放](/help/dsp/campaign-management/placements/placement-settings.md) 到这些层，以获得所需的访问级别：

   * **[!UICONTROL T1]**  — 品牌名称，国际知名网站

   * **[!UICONTROL T2]**  — 外观精美的网站，具有最新、最新的功能，不含用户生成的内容，通常缺乏全球认可度

   * **[!UICONTROL T3]**  — 用户生成的内容和小众内容

* **网站分类：** 为确保轻松定位和阻止内容，我们会根据属性的内容，使用Advertising Cloud定义的网站类别来标记每个属性。 您可以 [定位或排除每个版面的这些网站类别](/help/dsp/campaign-management/placements/placement-settings.md) 基于投放目标。

### 全面支持站点阻止

Advertising Cloud DSP提供了全局阻止的网站列表以及为广告商和帐户创建自定义阻止的网站列表的选项。

#### Advertising Cloud DSP全局阻止的站点列表 {#global-blocked-sites}

Advertising Cloud DSP维护一个在全球被阻止的网站列表，其中列出了在上运行广告时被认为不安全的网站。 此列表包含具有令人反感的内容（如仇恨或恐怖）的网站，以及受机器人、假前置、不匹配的域和其他欺诈活动感染的网站。

作为“品牌安全”计划的一部分，我们会使用阻止的网站列表中的措施来筛选所有网站，以根除欺骗广告商的活动。 未通过品牌安全检查的所有网站都会添加到全局阻止的网站列表中。 由于Advertising Cloud DSP会动态管理此列表，因此网站可能会根据最新的品牌安全分析随时在列表上移动或移出。

当您在全局阻止的网站列表中将某个网站添加为版面目标时，该网站会带有红色的感叹号(!)。 这表示广告不会在标记网站上运行。

>[!NOTE]
>
>您可以选择绕过全局阻止的站点列表，为附加到受信任的私有交易的标准显示广告提供支持，方法是启用“[!UICONTROL Allow unscreened sites]“ ”选项 [版面设置](/help/dsp/campaign-management/placements/placement-settings.md). 如有必要， [!DNL Adobe] 客户团队还可以选择在交易的发布者设置中，禁用公开（拍卖级别）交易的网站阻止。

#### 帐户级别和广告商级别的阻止网站列表

用户还可以维护帐户级别和广告商级别的阻止网站列表<!-- [account-level and advertiser-level blocked sites lists](/help/dsp/admin/blocked-sites-list-edit.md) -->，可自动用于所有版面。 除了全局阻止的站点列表之外，还会应用级别较低的阻止站点列表。

## 第三方集成

### 上下文过滤

上下文筛选允许您根据广告所在页面的上下文来定位或阻止广告机会。 Adobe通过与业内领先供应商的集成提供上下文筛选： [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science]和 [!DNL Peer39]. 当前过滤器的示例包括 [!UICONTROL Adult Content], [!UICONTROL Natural Disasters], [!UICONTROL Legal Drinking Age], [!UICONTROL MANGA], [!UICONTROL Epidemics]和 [!UICONTROL G-rated Sites].

您可以为每个广告商设置默认的上下文过滤器控件<!-- [default contextual filter controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->，然后（可选） [自定义每个版面的设置](/help/dsp/campaign-management/placements/placement-settings.md). 使用此功能时，可能需要支付额外费用。

![Comscore徽标](/help/dsp/assets/comscore-logo.png) ![DoubleVerify徽标](/help/dsp/assets/doubleverify-logo.png) ![Integral Ad Science徽标](/help/dsp/assets/ias-logo.png) ![Peer39徽标](/help/dsp/assets/peer39-logo.png)

### 投标前欺诈阻止

利用我们的第三方集成 [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science]和 [!DNL Peer39] 来阻止营销活动中的非人类流量。 这些集成提供了行业领先的投标前阻止功能，可最大程度地减少营销活动中一般和复杂的无效流量（GIVT和SIVT）。

您可以为每个广告商设置默认的投标前欺诈阻止控制<!-- [default pre-bid fraud blocking controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->，然后（可选） [自定义每个版面的设置](/help/dsp/campaign-management/placements/placement-settings.md). 使用此功能时，可能需要支付额外费用。

有关功能的更多信息，请直接联系首选供应商，或联系您的 [!DNL Adobe] 客户团队。

![Comscore徽标](/help/dsp/assets/comscore-logo.png) ![DoubleVerify徽标](/help/dsp/assets/doubleverify-logo.png) ![Integral Ad Science徽标](/help/dsp/assets/ias-logo.png) ![Peer39徽标](/help/dsp/assets/peer39-logo.png)

### 竞价前可视性 {#pre-bid-viewability}

由我们业界领先的合作伙伴提供支持的竞价前可见性过滤器 [!DNL DoubleVerify], [!DNL Oracle Advertising] ([!DNL Moat])和 [!DNL Integral Ad Science] 允许广告商确保其促销活动在视频和显示内容中达到其期望的可视性性能目标。

您可以为每个广告商设置默认的可查看性过滤器<!-- [default pre-viewability filters for each advertiser](/help/dsp/admin/advertiser-settings.md) -->，然后（可选） [自定义每个版面的设置](/help/dsp/campaign-management/placements/placement-settings.md). 使用此功能时，可能需要支付额外费用。

![DoubleVerify徽标](/help/dsp/assets/doubleverify-logo.png) ![Oracle广告徽标](/help/dsp/assets/oracle-advertising-logo.png) ![Integral Ad Science徽标](/help/dsp/assets/ias-logo.png)

### 主题定位

DSP主题定位允许您通过利用我们行业领先的情境合作伙伴来定位或阻止关键词列表 [!DNL Comscore] 和 [!DNL Oracle Data Cloud] ([!DNL Grapeshot])。 主题定位可帮助您确保广告始终在与您的品牌保持一致的环境中提供，无论这包括阻止有害内容，还是确保在可确保更好结果的上下文中花费。

主题定位要求您直接使用 [!DNL Comscore] 或 [!DNL Grapeshot] (使用 [!DNL Oracle Data Cloud])。 在合作伙伴平台中创建这些组件后，您可以 [在 [!UICONTROL Audience Targeting] 每个版面的部分](/help/dsp/campaign-management/placements/placement-settings.md). 此功能可能需要额外付费。

要创建自定义主题区段，请执行以下操作：

* 创建 [!DNL Comscore] 帐户并创建自定义区段，则可以请求登录 [!DNL Activation Segment Manager] at [https://agents.comscore.com](https://agents.comscore.com). 请参阅 [[!DNL Comscore] 帮助中心](https://comscoreactivation.zendesk.com/hc/) ，以了解有关设置自定义区段的完整说明。 自定义区段的费用可在 [!DNL Segment Manager] 创建时。

* 开始使用 [!DNL Oracle Data Cloud]，联系 [!DNL Oracle Data Cloud] 或 [!DNL Adobe] 客户团队。

![Comscore徽标](/help/dsp/assets/comscore-logo.png) ![Grapeshot徽标](/help/dsp/assets/oracle-grapeshot-logo.png)

### [!DNL DoubleVerify Authentic Brand Safety]

DSP与 [!DNL DoubleVerify] 提供 [!DNL Authentic Brand Safety] 定位解决方案，它允许您创建一组集中的品牌安全要求，以在所有购买平台中进行定位以保持一致性。

在您构建 [!DNL DoubleVerify] 品牌安全区段，您可以在DSP中使用该区段跨Web环境复制竞价后块规则和竞价前。

您可以指定 [!DNL DoubleVerify] 每个广告商的区段ID<!-- [specify a DoubleVerify segment ID for each advertiser](/help/dsp/admin/advertiser-settings.md) -->，然后（可选） [启用或禁用 [!UICONTROL Authentic Brand Safety] 对于每个版面](/help/dsp/campaign-management/placements/placement-settings.md). DSP会向您的帐户收取区段ID的使用情况帐单。

有关功能的更多信息，请联系 [!DNL DoubleVerify] 直接联系，或 [!DNL Adobe] 客户团队。

![DoubleVerify徽标](/help/dsp/assets/doubleverify-logo.png)

>[!MORELIKETHIS]
>
>* [版面设置](/help/dsp/campaign-management/placements/placement-settings.md)

<!-- >* [Advertiser Account Settings](/help/dsp/admin/advertiser-settings.md) -->
