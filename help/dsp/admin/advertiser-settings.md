---
title: 广告商帐户设置
description: 请参阅可用广告商设置的描述。
source-git-commit: ca19836d5918c69161c4d850a65eaff311249225
workflow-type: tm+mt
source-wordcount: '972'
ht-degree: 0%

---

# 广告商帐户设置

*对只读用户不可用*

## [!UICONTROL General] 设置

**[!UICONTROL Advertiser Name]:** 广告商名称。

**[!UICONTROL Category]:** 广告商业务运营的类别。 当您按库存竞价时，会向发布者传达类别。 确保选择与您的广告相一致的类别，否则发布者可能会拒绝您的广告。

>[!NOTE]
>
>如果您选择 *[!UICONTROL Other]*，则广告商将无法访问DSP [!DNL On Demand Inventory].

**[!UICONTROL Advertiser URL]:** 广告商的主页或主网站URL(以 `http://` 或 `https://`)。

**[!UICONTROL Share all private exchange feeds into this advertiser]:** （仅限新广告商帐户）使为组织的DSP帐户配置的所有专用Exchange馈送可供广告商使用。

### [!UICONTROL Adobe IMS IDs]

使用其他Adobe Experience Cloud产品的广告商可以使用组织的唯一ID在某些产品之间共享数据以进行Experience Cloud。 您可以在 [!UICONTROL Integrations] 中。

**[!UICONTROL Account IMS org and ID]:** (具有额外Experience Cloud产品的广告商，这些产品是通过多个广告商的Experience Cloud帐户获得许可的；可选)组织的Experience CloudID。

**[!UICONTROL Advertiser IMS org and ID]:** (直接获得其他Experience Cloud产品许可的广告商；可选)组织的Experience CloudID。

### [!UICONTROL Integrations]

（可选）链接到DSP帐户的其他Experience Cloud产品。 产品必须与 [!UICONTROL Adobe IMS IDs] 中。

**[!UICONTROL Adobe Media Optimizer]:** (使用Advertising Cloud Search或使用Advertising Cloud转化像素的广告商)A [!DNL Search] 将与DSP交换归因数据的帐户。

**[!UICONTROL Adobe Device Co-op or 3rd Party Graph]:** (使用Advertising Cloud转换像素的广告商);可选)您可以使用设备图，通过Advertising Cloud Search中广告商的帐户设置进行基于人员的归因测量。

>[!NOTE]
>
> * 设备归因仅适用于使用Advertising Cloud转化跟踪服务跟踪的转化，而不适用于Adobe Analytics跟踪的转化。
> * 您还可以在 [营销活动级别](/help/dsp/campaign-management/campaigns/campaign-settings.md). 然后，您可以在 [投放级别](/help/dsp/campaign-management/placements/placement-settings.md) 再加上频率上限 [包级别](/help/dsp/campaign-management/packages/package-settings.md) 和 [投放级别](/help/dsp/campaign-management/placements/placement-settings.md). 跨设备定位和频率管理不需要广告商级别的归因测量；而是使用营销活动设置中指定的设备图。


**[!UICONTROL Adobe Analytics]:** (拥有Adobe Analytics的广告商；可选；仅适用于使用Advertising Cloud转化跟踪标记收集的数据，这些标记包括 [!DNL EF Redirect] 和令牌)一个或多个 [!DNL Analytics] DSP会将从发布者和供应方合作伙伴收集的数据发送到的报表包。 Analytics还会将其从客户端网站收集的数据发送至DSP。

要使数据显示在报表包中， [!DNL Search] 广告商级别设置为“[!UICONTROL Enable tracking for SAINT feeds]必须启用。 此外，广告商 [!DNL Analytics] 帐户必须配置为从Advertising Cloud接收数据。 <!-- from Advertising Cloud or DSP in particular? Add cross-reference to file in Integrations section. -->

>[!WARNING]
>
>如果您删除之前链接的报表包，DSP将不再与该报表包交换数据。 预计会看到数据波动。 <!-- Fluctuations where? Clarify -->

**[!UICONTROL Adobe Analytics Cloud]:** (拥有Adobe Audience Manager或Adobe Analytics的广告商；可选)Audience Manager或 [!DNL Analytics] DSP将从中提取所有广告商Adobe受众的区段元数据、层次结构数据和独特受众数据的帐户。 这包括以下数据：

* Audience Manager区段
* [!DNL Analytics] 发布到Adobe Experience Cloud的区段
* 在Adobe Experience Cloud中使用 [!DNL People core service]
* 在Adobe Experience Platform中创建并通过Audience Manager发送到Advertising Cloud的区段

初始同步大约需要24小时。 之后，数据会实时同步，延迟时间为1到2秒。
<!-- I don't think this is true anymore:
Segment membership data is sent to Advertising Cloud only after one of the following:

* The segment is targeted in an Advertising Cloud placement or audience library
* The segment is added to the Advertising Cloud batch and real-time destinations within the Audience Manager user interface
-->

## [!UICONTROL Targeting] 设置

您可以选择为广告商的新版面配置默认目标。 用户可以覆盖任何新版面的默认目标。

### [!UICONTROL Geo-targeting]

**[!UICONTROL Countries]:** 每个版面的地理定位的默认国家/地区。 用户可以更改国家/地区，并为每个版面配置更具体的地理定位。

### [!UICONTROL Audience Targeting]

**[!UICONTROL Audiences to exclude]:** 默认情况下要禁止的任何受众或区段。 用户可以更改每个版面的排除项。

### [!UICONTROL Media Quality]

#### [!UICONTROL Contextual Filtering]

类型 [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science]和 [!DNL Peer39] 要应用的上下文过滤器。 您可以在 [投放级别](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-context}

**[!UICONTROL Block sites that are]:** （可选）默认情况下，要阻止的一种或多种类型的库存上下文。 可能需要支付额外费用。

##### [!UICONTROL Peer 39] {#peer39-context}

**[!UICONTROL Target sites that are]:** （可选）默认情况下，要定位的一个或多个库存属性类型。 可能需要支付额外费用。

##### [!UICONTROL ComScore]

**[!UICONTROL Block sites that are]:** （可选）默认情况下，要阻止的一种或多种类型的库存属性。 可能需要支付额外费用。

##### [!UICONTROL Integral Ad Science] {#ias-context}

**[!UICONTROL Adult Content]:** （可选）默认情况下要阻止广告的成人内容的程度： *[!UICONTROL Do Not Block]* （默认）、 *[!UICONTROL Standard]*&#x200B;或 *[!UICONTROL Strict]*. 可能需要支付额外费用。

**[!UICONTROL Alcohol Content]:** （可选）默认情况下要阻止广告的酒精含量程度： *[!UICONTROL Do Not Block]* （默认）、 *[!UICONTROL Standard]*&#x200B;或 *[!UICONTROL Strict]*. 可能需要支付额外费用。

#### [!UICONTROL Pre-Bid Fraud Blocking]

基于通过测量的欺诈性流量和可疑活动而阻止的网站类型 [!DNL DoubleVerify], [!DNL Integral Ad Science]和 [!DNL Peer39]. 您可以在 [投放级别](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-fraud}

**[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** 默认情况下，会阻止所有100%的无效流量（包括被劫持设备上的流量）进行新投放。 可能需要支付额外费用。

**[!UICONTROL Also block sites with]:** （可选）默认情况下，会导致DSP阻止广告的额外级别欺诈和无效流量：  *[!UICONTROL None]* （默认设置，不阻止其他流量）， *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]*&#x200B;或 *[!UICONTROL >25% Average Fraud/IVT levels]*. 可能需要支付额外费用。

##### [!UICONTROL Peer 39] {#peer-39-fraud}

**[!UICONTROL Block sites that are]:** （可选）默认情况下，一种或多种类型的欺诈将导致DSP阻止广告： *[!UICONTROL Fraud]* （它阻止所有网站出现欺诈） *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]*&#x200B;和/或 *[!UICONTROL Fraud: Zero Ads]*. 可能需要支付额外费用。

##### [!UICONTROL Integral Ad Science] {#ias-fraud}

**[!UICONTROL Block sites that are]:** （可选）默认导致DSP阻止广告的可疑网站或应用程序活动类型： *[!UICONTROL None]* （默认，不会基于可疑活动阻止广告）， *[!UICONTROL Suspicious Activity - High Risk]*&#x200B;或 *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. 可能需要支付额外费用。

#### [!UICONTROL Ads.text]

**[!UICONTROL Ads.txt Filtering]:** 默认情况下， [[!DNL Ads.txt] 预竞价过滤](https://iabtechlab.com/ads-txt-about/) 通过利用每个发布者的 [!DNL Authorized Digital Sellers] 列表：
* *[!UICONTROL Opt out of ads.txt (default)]*:从所有卖家处购买库存。
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*:优先从域的授权直销商和转销商购买库存。
* *[!UICONTROL Ads.txt sellers only]*:仅向域的授权直销商和经销商购买库存。
* *[!UICONTROL Ads.txt sellers only]*:仅从域的授权直销商处购买库存。

您可以在 [投放级别](/help/dsp/campaign-management/placements/placement-settings.md).

#### [!UICONTROL Safe Site Block]

**[!UICONTROL Enable Site Safety Block]:** 默认情况下，会启用实时竞价后过滤器，以确保广告在广告商定位的网站上提供。 <!-- Can remove this: Users can enable or disable the feature for each placement. I don't see this option, but I should probably verify. If this can't be edited at placement level, then remove "By default." If it can, say that you can override at placement level. -->

#### [!UICONTROL DoubleVerify Authentic Brand Safety]

**[!UICONTROL DoubleVerify Account]:** ([!DNL DoubleVerify] 仅限客户；可选)与组织的 [!DNL DoubleVerify] 帐户。

**[!UICONTROL Enable Authentic Brand Safety]:** （可选）默认情况下，启用 [!DNL DoubleVerify] 正版品牌安全，它使用为指定区段ID配置的自定义品牌安全规则阻止投标后展示。 DSP会向您的帐户收取区段ID的使用情况帐单。

您可以在版面级别覆盖广告商级别的设置。

>[!MORELIKETHIS]
>
>* [创建广告商帐户](/help/dsp/admin/advertiser-create.md)


<!-- >* [View the Advertiser List for the Account](/help/dsp/admin/advertiser-view.md) -->
