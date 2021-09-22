---
title: 使用 [!DNL Roku] 清单
description: '了解DSP与 [!DNL Roku], including inventory options, approved third-party tracking vendors, and best practices for [!DNL Roku]特定版面的合作关系。 '
feature: DSP On Demand Inventory, DSP Private Inventory
exl-id: 0cd42782-f006-4aa8-b879-322f86cfac4b
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---

# 使用[!DNL Roku]清单

Advertising Cloud DSP为[!DNL Roku]上的广告提供了独特功能。

## Advertising Cloud DSP与[!DNL Roku]伙伴关系

Roku和Advertising Cloud DSP具有独特的合作伙伴关系，可将您的[!DNL DSP]受众与[!DNL Roku] ID匹配，以便在[!DNL Roku]库存中确定性受众定位为1:1。

在Roku自己的DSP(OneView)之外，Advertising Cloud DSP拥有这些定位功能的唯一访问权限。 Advertising Cloud DSP也是唯一有权测量[!DNL Roku]供应量的DSP，位于所有其他连接的电视(CTV)清单旁边。 由于[!DNL Roku]不共享所有标准RTB和展示像素信号，因此其他任何DSP都无法定位或测量Roku销售的CTV供应中的RTB。

## [!DNL Roku] 库存选项

您可以a)直接使用[!DNL Roku]设置私有交易ID，然后将交易ID数据输入DSP，或b)访问[!DNL On Demand]库以订阅[!DNL Roku]用户档案：

>[!NOTE]
>
>[!DNL Roku] 在开放的市场和交易所中不提供库存。

* 对于您的私人交易，您将在[中设置有关交易ID的信息，然后在[!DNL Roku]版面中定位“[!UICONTROL Roku Network – Audience]”和“[!UICONTROL The Roku Channel – Audience]”。<!-- Or do you target the deal ID?? I see those strings for Roku On Demand inventory. Clarify if all Roku private deals will show up as one or the other of these in Roku Private inventory in Roku placement settings. -->](/help/dsp/inventory/deal-id-create.md)

* 您可以[订阅以下 [!DNL Roku] inventory within the [!DNL On Demand] Gallery](/help/dsp/inventory/on-demand-inventory-subscribe.md)，然后在[!DNL Roku]版面中定位任何已批准的交易：

   * “[!UICONTROL Roku Network – Audience]”，用于使用高级内容合作伙伴（如[!DNL The CW]、[!DNL ABC]和[!DNL ESPN]）在[!DNL Roku]生态系统中进行清点。
   * “[!UICONTROL The Roku Channel – Audience]”，用于[!DNL Roku]自有和操作(O&amp;O)应用程序内容。

### 使用[!DNL Roku]自定义私有市场的优势

私有交易允许您根据自己的需求自定义交易参数。

* **协商定价：** 与销售团队 [!DNL Roku] 合作，协商并构建满足营销活动需求的交易。

* **比例优先级：** 私营市场(PMP)获得的优先级高于始终进行的交易(例如 [!DNL On Demand] 交易)。

* **频度管理：** 默 [!DNL Roku] 认的频度上限为每用户30分钟一(1)个广告，但您可以按小时、日、周、月或整个飞行时段自定义频度上限。<!-- Within the DSP placement settings? NO - you negotiate this with Roku, but Christine to confirm with Amanda whether you should be able to edit this in placement. -->

* **[!DNL Roku]数据定位：** [!DNL Roku] 受众从设备和电 [!DNL Roku] 视信号构建，由跟踪的 [!DNL The Roku Channel] 数据（如电视流派亲和度、流电视行为和有线订阅状态），以及客户关系管理(CRM)系统 [!DNL Roku] 中的其他数据。

* **[!DNL Roku]内容定位：** 私人交易可以按流派、应用程序、季节和阻止列表极点事件的应用程序来定位应用程序，并且只能在 [!DNL The Roku Channel] 内显示。

## [!DNL Roku] 版面

在DSP促销活动中，您将使用版面类型“[!UICONTROL Connected TV (Roku)]”创建 [!DNL Roku]特定的版面](/help/dsp/campaign-management/placements/placement-create.md)。 [您将在具有定义目标的特定于[!DNL Roku]的包中包含[!DNL Roku]版面。

每个[!DNL Roku]位置必须至少定位一个[!DNL Roku]交易或来源。 要利用与[!DNL Roku]匹配的DSP独特受众，请包含一个或多个可与[!DNL Roku]（选择加入）确定性数据集匹配的受众区段。

### [!DNL Roku] — 已批准的第三方跟踪供应商

[!DNL Roku] 版面可以包括来自以下供应商的第三方事件像素和转化像素：  [!DNL Acxiom]、  [!DNL comScore]、  [!DNL Data Plus Math]、  [!DNL Experian]、  [!DNL Factual]、  [!DNL Kantar]、  [!DNL Marketing Evolution]、  [!DNL Neustar]、  [!DNL Nielsen]、  [!DNL Nielsen Catalina Solutions]、  [!DNL NinthDecimal]、  [!DNL Oracle]和 [!DNL Placed] [!DNL Polk] [!DNL Research Now]。

### 按位置策略列出的最佳实践

以下是特定于[!DNL Roku]的版面的推荐实践。

要最大化增量访问，请执行以下操作：

* 通过排除已使用[!DNL The Roku Channel]访问的受众来禁止[!DNL Roku O&O]上显示的受众。

* 通过排除已在[!DNL Roku]平台中访问的受众，禁止[!DNL All Roku]上显示的受众。

要获得最快的设置，请执行以下操作：

* 在[[!DNL On Demand] Inventory](/help/dsp/inventory/on-demand-inventory-subscribe.md)中为[!DNL The Roku Channel]定位现有的始终运行交易，以快速访问拥有和运营的[!DNL Roku]库存。
* 在[[!DNL On Demand] Inventory](/help/dsp/inventory/on-demand-inventory-subscribe.md)中为[!DNL Roku Network]定位现有的、始终运行的交易，以便在[!DNL Roku]平台上快速实现规模。

要达到最大规模：

* 自定义[!DNL Roku]私有市场，以按协议价格优先访问[!DNL Roku]供应。

>[!MORELIKETHIS]
>
>* [手动创建交易ID详细信息](/help/dsp/inventory/deal-id-create.md)
> * [订阅并请求访问 [!DNL On Demand] Premium库存交易](/help/dsp/inventory/on-demand-inventory-subscribe.md)
>* [创建版面](/help/dsp/campaign-management/placements/placement-create.md)

