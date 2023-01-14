---
title: 使用 [!DNL Roku] 库存
description: 了解DSP与 [!DNL Roku]，包括库存选项、已批准的第三方跟踪供应商以及 [!DNL Roku] — 特定版面。
feature: DSP On Demand Inventory, DSP Private Inventory
exl-id: 0cd42782-f006-4aa8-b879-322f86cfac4b
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 0%

---

# 使用 [!DNL Roku] 库存

Advertising DSP为 [!DNL Roku].

## DSP和 [!DNL Roku] 合作伙伴

Roku和DSP具有与 [!DNL DSP] 受众 [!DNL Roku] 确定性受众定位的ID(在 [!DNL Roku] 库存。

在Roku自己的DSP(OneView)之外，Advertising DSP可以完全访问这些定位功能。 Advertising DSP也是唯一有权测量的DSP [!DNL Roku] 在所有其他连接的电视(CTV)清单旁提供。 因为 [!DNL Roku] 不共享所有标准的RTB和展示像素信号，其他任何DSP都无法在Roku销售的CTV供应中定位或测量。

## [!DNL Roku] 库存选项

您可以a)直接通过 [!DNL Roku] 然后，将交易ID数据输入DSP或b)访问 [!DNL On Demand] 图片库，订购 [!DNL Roku] 用户档案：

>[!NOTE]
>
>[!DNL Roku] 在开放的市场和交易所中不提供库存。

* 为了私下交易， [在DSP中设置有关交易ID的信息](/help/dsp/inventory/deal-id-create.md) 然后定位“[!UICONTROL Roku Network – Audience]&quot;和&quot;[!UICONTROL The Roku Channel – Audience]在 [!DNL Roku] 版面。<!-- Or do you target the deal ID?? I see those strings for Roku On Demand inventory. Clarify if all Roku private deals will show up as one or the other of these in Roku Private inventory in Roku placement settings. -->

* 您可以 [订阅以下内容 [!DNL Roku] 库存 [!DNL On Demand] 图库](/help/dsp/inventory/on-demand-inventory-subscribe.md)，然后定位 [!DNL Roku] 版面：

   * &quot;[!UICONTROL Roku Network – Audience]“ ”，用于 [!DNL Roku] 具有高级内容合作伙伴的生态系统，例如 [!DNL The CW], [!DNL ABC]和 [!DNL ESPN].
   * &quot;[!UICONTROL The Roku Channel – Audience]&quot; [!DNL Roku] 自有和运营(O&amp;O)应用程序内容。

### 使用定制私人市场的优势 [!DNL Roku]

私有交易允许您根据自己的需求自定义交易参数。

* **协商定价：** 使用 [!DNL Roku] 销售团队来协商和构建满足营销活动需求的交易。

* **缩放优先级：** 私有市场(PMP)比始终如一的交易(例如 [!DNL On Demand] 交易)。

* **频率管理：** 的 [!DNL Roku] 默认频度上限为每用户每30分钟一(1)个广告，但您可以按小时、日、周、月或整个飞行时段自定义上限。<!-- Within the DSP placement settings? NO - you negotiate this with Roku, but Christine to confirm with Amanda whether you should be able to edit this in placement. -->

* **[!DNL Roku]数据定位：** [!DNL Roku] 受众的构建依据 [!DNL Roku] 设备和电视信号，跟踪数据 [!DNL The Roku Channel] （如电视流派亲和度、流媒体电视行为和有线订阅状态），以及 [!DNL Roku] 客户关系管理(CRM)系统。

* **[!DNL Roku]内容定位：** 私人交易可以按流派、应用程序、季节和阻止列表极点事件的应用程序来定位应用程序，并在 [!DNL The Roku Channel] 仅。

## [!DNL Roku] 版面

在DSP促销活动中， [创建 [!DNL Roku] — 特定投放](/help/dsp/campaign-management/placements/placement-create.md) 使用放置类型“[!UICONTROL Connected TV (Roku)].&quot; 包括 [!DNL Roku] 版面 [!DNL Roku] — 特定包，其中包含定义的目标。

每个 [!DNL Roku] 投放必须至少定向一个 [!DNL Roku] 交易或来源。 将DSP独特受众与 [!DNL Roku]，包括一个或多个可与匹配的受众区段 [!DNL Roku] （选择启用）确定性数据集。

### [!DNL Roku] — 已批准的第三方跟踪供应商

[!DNL Roku] 版面可以包括来自以下供应商的第三方事件像素和转化像素：  [!DNL Acxiom], [!DNL comScore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk]和 [!DNL Research Now].

### 按位置策略列出的最佳实践

以下是 [!DNL Roku] — 特定版面。

要最大化增量访问，请执行以下操作：

* 在上禁止显示的受众 [!DNL Roku O&O] 通过排除已使用访问的受众 [!DNL The Roku Channel].

* 在上禁止显示的受众 [!DNL All Roku] 通过排除在 [!DNL Roku] 平台。

要获得最快的设置，请执行以下操作：

* 为现有的永久性交易定位 [!DNL The Roku Channel] in [[!DNL On Demand] 库存](/help/dsp/inventory/on-demand-inventory-subscribe.md) 快速访问 [!DNL Roku] 自有和经营的库存。
* 为现有的永久性交易定位 [!DNL Roku Network] in [[!DNL On Demand] 库存](/help/dsp/inventory/on-demand-inventory-subscribe.md) 以快速实现跨 [!DNL Roku] 平台。

要达到最大规模：

* 自定义 [!DNL Roku] 专用市场，以优先访问 [!DNL Roku] 以协议价格供应。

>[!MORELIKETHIS]
>
>* [手动创建交易ID详细信息](/help/dsp/inventory/deal-id-create.md)
> * [订阅并请求访问 [!DNL On Demand] 高级库存交易](/help/dsp/inventory/on-demand-inventory-subscribe.md)
>* [创建版面](/help/dsp/campaign-management/placements/placement-create.md)

