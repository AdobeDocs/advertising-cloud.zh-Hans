---
title: 营销活动设置
description: 请参阅可用营销活动设置的描述。
feature: DSP Campaigns
exl-id: ff2e22ff-8073-4532-884b-36e0c1f22641
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '990'
ht-degree: 0%

---

# 营销活动设置

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]:** 营销活动名称。

**[!UICONTROL Advertiser]:** （现有促销活动的只读）适用的广告商（品牌）。选择现有广告商或创建新广告商。

**[!UICONTROL Advertiser URL]:** 广告商的正式页面。此字段可加快您与库存合作伙伴的广告批准流程。

**[!UICONTROL Timezone]:** （现有促销活动的只读）报告和竞价的时区。

**[!UICONTROL Customer PO]:** （可选）插入订单/采购订单的客户采购订单。

**[促销活动日期]:** 促销活动开始和结束日期。

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]:** 是否管理营销活动的边距： *[!UICONTROL Yes]* 或( *[!UICONTROL No]* 默认)。

选择&#x200B;*[!UICONTROL Yes]时，*&#x200B;指定边距类型和金额：

* **[!UICONTROL Margin Type]:** 边距的类型。启用边距管理并保存营销活动后，便无法更改边距类型。

   * *[!UICONTROL Fixed]:* （默认）允许Advertising Cloud DSP根据的固定利润百分比自动计算和限制支 [!UICONTROL Gross Budget]出。

   * *[!UICONTROL Dynamic]:* 用于通过为营销活动中的每个包和版面指定 [!UICONTROL Budget Reserve %] 单独 [!UICONTROL Gross Budget] 的和来向下管理页边距。Advertising Cloud DSP会根据每次投放的财务效率进行优化，而无需保证特定的利润。 对于由多个行项目组成的插入订单，您同意以固定费率交付固定数量的件数或件数类型。

* **[!UICONTROL Fixed Margin %]:** （仅具有固定边距的促销活动）每个插入顺序的默认标 <!-- impression? -->记（以百分比表示）。此金额将从[!UICONTROL Gross Budget]中扣除，以定义净促销活动预算。

* **[!UICONTROL Budget Reserve %]:** (仅具有固定边距的促销活动；（可选）保留指定百分比 [!UICONTROL Gross Budget] 作为保护。此金额将从[!UICONTROL Gross Budget]中扣除，以定义净促销活动预算。

**[!UICONTROL Gross Budget]:** （仅限具有毛利管理的促销活动）在应用指定的边际调整之前的促销活动预算总额。

您可以选择添加额外的每日、每周或每月总预算：

1. 单击 **[!UICONTROL Add an additional Gross Budget]**.

1. 输入&#x200B;**[!UICONTROL Gross Budget]**&#x200B;并选择预算间隔：*[!UICONTROL Daily]、* *[!UICONTROL Weekly]、*&#x200B;或&#x200B;*[!UICONTROL Monthly]*。

总净预算（即营销活动的支出上限）根据利润设置自动计算，并指示在此值下方。

**[!UICONTROL Budget]:** （无边距管理的促销活动）促销活动整体预算。

**[!UICONTROL Estimated Tax Withholding]:** 在国家/地区或地方税的帐户级别保留所有广告费、广告服务费和/或数据费的总支出的百分比。税率是用于预算和步调的估计，因此开具发票的税率可能会有所不同。

要估计税金以预扣：

1. 单击 **[!UICONTROL Update rates here]**.

1. 以百分比形式指定&#x200B;**[!UICONTROL Estimated tax rate]**。

1. 选中要预缴税金的每个费用类型旁边的复选框。 收费类型包括：

   * *[!UICONTROL Include estimated tax - ads fee]:* 适用于所有Advertising Cloud DSP媒体支出，包括促销活动管理费用税。

   * *[!UICONTROL Include estimated tax - ad serving fee]:* 适用于除媒体和数据之外的所有在Advertising Cloud DSP上的花费。它不包括促销活动管理费的税

   * *[!UICONTROL Include estimated tax - data fee]:* 适用于所有在Advertising Cloud DSP上花费的数据。

1. 单击 **[!UICONTROL Submit]**.

>[!NOTE]
>
>* 在美国，州在将税费纳入广告、广告投放和数据方面可能会有所不同。 对于其他国家/地区的组织，包括所有三类纳税费用，以计算增值税。
>
>* 您还可以在帐户的费用设置中配置这些值。<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->


**[!UICONTROL Cross Device Level]:** (自2020年6月22日起创建的现有营销活动为只读；不适用于2020年6月22日之前创建的促销活动)Advertising Cloud将定位广告并应用频率上限的级别： *用于* 定位设备的同一 ** 个设备，或用于定位所有已知设备上的人员。

**[!UICONTROL Device Graph]:** (现有营销活动为只读；仅使用基于人员的跨设备定位的促销活动)用于跨设备定位和频率管理的设备图：

* *[!UICONTROL LiveRamp - U.S. only]:* 对于使用设备图交付的展示次数（即，在目标受众区段内未找到的设备），所有广告商均可 [!DNL LiveRamp] 以按0.35 CPM的价格进行跨设备定位。您可以在放置级别设置跨设备定位。

   此选项还可供所有广告商使用，无需支付任何费用即可进行频率管理和归因测量。

* *[!UICONTROL Adobe Co-op U.S. and Canada only]:* 仅供Adobe Experience Cloud参与者 [!DNL Device Co-op] 使用，无需额外付费。

>[!TIP]
>
>如果广告商还使用跨设备归因，则最佳实践是使用与广告商跨设备归因设置中指定的设备图设置进行定位和频率管理。 如果为此营销活动选择其他设备图，则可能会出现报表差异。

**[!UICONTROL Frequency Cap]:** （可选）营销活动中向独特设备或人员(取决于指 [!UICONTROL Cross Device Level]定的)提供广告的次数。选项包括&#x200B;*[!UICONTROL Unlimited]*&#x200B;或每天、每周或每月的特定金额。

>[!NOTE]
>
> 您可以在营销活动、资源包和版面级别设置频率上限。 DSP将遵循营销活动层级中最严格的频率上限。

**[!UICONTROL Packages]:** 要包 [](/help/dsp/campaign-management/packages/package-about.md) 含在营销活动中的包。选择现有包和/或创建要包含的包。 如果创建包，请参阅有关[包设置](/help/dsp/campaign-management/packages/package-settings.md)的说明，以了解更多信息。

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>以下设置仅启用测量和报告功能。 性能优化仅在包和放置级别执行。

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]:** （可选）使用指 [!DNL IAS] 定的设置，启用可见性、欺诈、品牌安全和受众验证的测量和报告功能。额外收费。

* **[!UICONTROL Measure On]:** 要测量的库存： *[!UICONTROL Display and VPAID video inventory]* （默认）或 *[!UICONTROL Display, VPAID & VAST video inventory]*。

   >[!NOTE]
   >
   >视频可见性仅可在VPAID清单中测量。

* **[!UICONTROL IAS Account ID (AnID)]:** (拥有自己帐户的广 [!DNL IAS] 告商；（可选）组织的帐 [!DNL IAS] 户ID，将直 [!DNL IAS] 接收费以供使用。

* **[!UICONTROL IAS Team ID]:** (拥有自己帐户的广 [!DNL IAS] 告商；（可选）组织帐户的团队ID，该 [!DNL IAS] 帐户将直 [!DNL IAS] 接收费供使用。  <!-- verify -->

**[!UICONTROL MOAT]:** （可选）启用 [!DNL MOAT] 可视性、欺诈、品牌安全和受众验证的测量和报告功能。额外收费。

#### 受众验证

**[!UICONTROL Nielsen]:** （可选）启用 [!DNL Nielsen] 使用指定的设置来测量和报告受众验证。额外收费。

* **[!UICONTROL Target Gender]:** 要定位的性别： *[!UICONTROL Both]* （默认）、  *[!UICONTROL Male]*&#x200B;或  *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** 要定位的年龄范围。根据需要使用左和右滑块来缩小范围。

* **[!UICONTROL Target Country]:** （可选）要定位的国家/地区。[!DNL Nielsen] 将仅测量在受支持国家/地区提供的展示次数。

**[!UICONTROL comScore vCE]:** （可选）启用 [!DNL Comscore validated Campaign Essentials (vCE)] 使用指定的设置来测量和报告受众验证。额外收费。

* **[!UICONTROL Target Gender]:** 要定位的性别： *[!UICONTROL Both]* （默认）、  *[!UICONTROL Male]*&#x200B;或  *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** 要定位的年龄范围。根据需要使用左和右滑块来缩小范围。

* **[!UICONTROL Target Country]:** （可选）要定位的国家/地区。[!DNL Comscore] 将仅测量在受支持国家/地区提供的展示次数。

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]:** 根据指定的敏感度级别，使用技术启用第 [!DNL IAB Open Video Viewability (OpenVV)] 一方测量和报告可见性：

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [关于营销活动管理](campaign-about.md)
>* [创建营销活动](campaign-create.md)
>* [编辑营销活动](campaign-edit.md)

