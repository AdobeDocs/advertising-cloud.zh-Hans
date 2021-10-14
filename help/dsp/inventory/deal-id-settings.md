---
title: 手动交易ID设置
description: 请参阅手动输入的交易ID设置的描述。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 0cd5e9e8-2b13-4b1e-a2e0-b8b492f75acf
source-git-commit: 5f39608155f9237fb6d69a7b31c007d1b8d0306f
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 0%

---

# 手动交易ID设置

| 区域 | 参数 | 描述 | 必需 | 可编辑 |
|---------|-----------|-------------|----------|----------|
| [交易详细信息] | [!UICONTROL Deal name] | 在Advertising Cloud DSP中标识[!UICONTROL Deal ID]的名称。 输入名称或选择[!UICONTROL Auto-name]以让Advertising Cloud根据交易详细信息生成名称。<br><br>自动生成的名称示例： [!DNL *DEAL_ID*  — 交易ID — 保证固定 — USD - 5 - 24厨房 — 私人] | 是 | 是 |
|  | [!UICONTROL External deal ID] | 发布者和SSP用于标识此交易的ID。 | 是 | 否 |
|  | [!UICONTROL Publisher] | 销售此库存的发布者的名称。 | 是 | 否 |
|  | [!UICONTROL SSP] | 此交易将通过的供应方平台(SSP)。 | 是 | 否 |
|  | [!UICONTROL Media type] | 将通过此交易购买的媒体类型：[!UICONTROL Desktop video]、[!UICONTROL Mobile video]、[!UICONTROL Connected TV]、[!UICONTROL Display]或[!UICONTROL Audio]。 选项因SSP而异。<br><br> 如果交易允许多种媒体类型，请在创建交易时为默认版面选择媒体类型。之后，您可以选择其他媒体类型，以使用附加的媒体类型创建新版面。<!-- It would be ideal if this field was multi-select rather than a radio button, so you don't have to "change" the value later. --> | 是 | 否 |
|  | [!UICONTROL Deal type] | 交易承诺和定价结构：<br><ul><li>*[!UICONTROL Non guaranteed (floor)]*:您和发布者未承诺投放固定数量的展示投放。该交易规定了库存的最低价格，尽管CPM可能会根据市场情况而波动和上升。</li><li>*[!UICONTROL Non guaranteed (fixed)]*:您和发布者未承诺投放固定数量的展示投放。定价按议定固定利率计算。</li><li>*[!UICONTROL Guaranteed (fixed)]*:您和发布商已就预定义的展示次数、定位、投放日期和固定价格达成了一致。<br><br><b>注意：</b> 保证交易要求投放日期和部分中的指定展示 [!UICONTROL Tracking] 次数。您还需要为交易创建一个默认的程序化保证(PG)投放，并且您可以选择将该交易用于其他投放。</li></ul> | 是 | 否 |
|  | [!UICONTROL CPM] | 每千次展示次数的协商成本(CPM)。 | 是 | 是 |
|  | [货币] | 交易的货币。<br><br>所有南苏丹镑都接受以美元计价的交易。当SSP接受您的DSP帐户的货币时，该货币也可用。 | 是 | 否 |
|  | [!UICONTROL Billing method] | 所有交易ID都由[!DNL Adobe]提供融资并开具发票。 Advertising Cloud将根据使用情况向所有可用的媒体供应商支付费用，管理与供应商的差异，并向帐户发送一张合并发票。 此选项会产生额外费用，如帐户费率卡中所述。 | 是 | 否 |
| [!UICONTROL Advertisers] | [!UICONTROL Account email] | 可访问交易的用户帐户的电子邮件地址。 | 否 | 是 |
|  | [!UICONTROL Advertisers that can access this deal] | 帐户中可访问此交易的特定广告商。<br><br><b>注意：</b> 您可以从视图与其他帐户中的广告商共享该 [!UICONTROL Deals] 交易。在交易行中，单击&#x200B;**[!UICONTROL #]**，单击&#x200B;**[!UICONTROL share]**，然后与电子邮件地址共享交易。 | 是 | 是 |
| [!UICONTROL Tracking] | [!UICONTROL Flight Dates] | 使用此交易的流量的开始和结束日期。 这些日期仅供跟踪之用，不会影响广告投放。<br><br><b>提示：</b> 在>视 [!UICONTROL Inventory] 图 [!UICONTROL Deals] 中，列将 [!UICONTROL Pacing & Budget] 显示交易在指定的投放日期和展示目标中的步调。如果投放进度缓慢或过于紧张，请联系您的发布者以调整通过交易发送的量。 | 有保证的交易：是<br>无担保交易：否 | 是 |
|  | [!UICONTROL Impressions] | （对于无保证交易而言，它是可选项）使用此交易预计要运行的预计展示次数。 此值仅用于跟踪；发布者控制广告投放。 | 有保证的交易：是<br>无担保交易：否 | 是 |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [手动创建交易ID详细信息](deal-id-create.md)
>* [SSP合作伙伴](ssp-partners.md)

<!-- >* [About Private Inventory](private-inventory-about.md) -->
