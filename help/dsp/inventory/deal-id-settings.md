---
title: 手动交易ID设置
description: 请参阅手动输入的交易ID设置的描述。
feature: DSP Private Inventory, DSP Deal IDs
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# 手动交易ID设置

| 区域 | 参数 | 描述 | 必需 | 可编辑 |
|---------|-----------|-------------|----------|----------|
| [交易详细信息] | [!UICONTROL Deal name] | 用于标识您的 [!UICONTROL Deal ID] 在Advertising DSP中。 输入名称或选择 **[!UICONTROL Auto-name]** 以便DSP根据交易详细信息生成名称。<br><br>自动生成的名称示例： `[!DNL 24159708 - Deal ID - Guaranteed Fixed - USD - 5 - 24Kitchen - Private]` | 是 | 是 |
|  | [!UICONTROL External deal ID] | 发布者和SSP用于标识此交易的ID。 | 是 | 否 |
|  | [!UICONTROL Publisher] | 销售此库存的发布者的名称。 | 是 | 否 |
|  | [!UICONTROL SSP] | 此交易通过的供应方平台(SSP)。 | 是 | 否 |
|  | [!UICONTROL Media type] | 通过此交易购买的媒体类型： *[!UICONTROL Desktop video]*, *[!UICONTROL Mobile video]*, *[!UICONTROL Connected TV]*, *[!UICONTROL Display]*&#x200B;或 *[!UICONTROL Audio]*. 选项因SSP而异。<br><br> 如果交易允许多种媒体类型，请在创建交易时为默认版面选择媒体类型。 稍后，您可以更改值，或者只需 [使用附加的媒体类型附加新版面](deal-id-attach-placements.md).<!-- It would be ideal if this field was multi-select rather than a radio button, so you don't have to "change" the value later. --> | 是 | 否 |
|  | [!UICONTROL Deal type] | 交易承诺和定价结构：<br><ul><li>*[!UICONTROL Non guaranteed (floor)]*:您和发布者未承诺投放固定数量的展示投放。 该交易规定了库存的最低价格，尽管CPM可能会根据市场情况而波动和上升。</li><li>*[!UICONTROL Non guaranteed (fixed)]*:您和发布者未承诺投放固定数量的展示投放。 定价按议定固定利率计算。</li><li>*[!UICONTROL Guaranteed (fixed)]*:您和发布商已就预定义的展示次数、定位、投放日期和固定价格达成了一致。<br><br><b>注意：</b> 有保证的交易需要投放日期和 [!UICONTROL Tracking] 中。 您还必须为交易创建默认的程序化保证(PG)投放，并且您可以选择将该交易用于其他投放。</li></ul> | 是 | 否 |
|  | [!UICONTROL CPM] | 每1000次展示的协商成本(CPM)。 | 是 | 是 |
|  | [货币] | 交易的货币。<br><br>所有南苏丹镑都接受以美元计价的交易。 当SSP接受您的DSP帐户的货币时，该货币也可用。 | 是 | 否 |
|  | [!UICONTROL Billing method] | 所有交易ID均 [!DNL Adobe] — 融资和开票。 DSP会根据使用情况向所有可用的媒体供应商支付费用，管理与供应商的差异，并向帐户发送一张合并发票。 此选项会产生额外费用，如帐户费率卡中所述。 | 是 | 否 |
| [!UICONTROL Advertisers] | [!UICONTROL Account email] | 可访问交易的用户帐户的电子邮件地址。 | 否 | 是 |
|  | [!UICONTROL Advertisers that can access this deal] | 帐户中可访问此交易的特定广告商。<br><br><b>注意：</b> 您可以在 [!UICONTROL Deals] 中。 在交易行中，单击 **[!UICONTROL #]**，单击 **[!UICONTROL share]**，然后将交易与电子邮件地址共享。 | 是 | 是 |
| [!UICONTROL Tracking] | [!UICONTROL Flight Dates] | 使用此交易的流量的开始和结束日期。 这些日期仅用于跟踪，不会影响广告交付。<br><br><b>提示：</b> 在 [!UICONTROL Inventory] > [!UICONTROL Deals] , [!UICONTROL Pacing & Budget] 列显示交易如何步调到指定的投放日期和展示目标。 如果投放进度缓慢或过于紧张，请联系您的发布者以调整通过交易发送的量。 | 有保证的交易：是<br>无担保交易：否 | 是 |
|  | [!UICONTROL Impressions] | （对于无保证交易而言，它是可选项）使用此交易预计要运行的预计展示次数。 此值仅用于跟踪；发布者控制广告投放。 | 有保证的交易：是<br>无担保交易：否 | 是 |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [手动创建交易ID详细信息](deal-id-create.md)
>* [SSP合作伙伴](ssp-partners.md)
>* [关于专用清单](private-inventory-about.md)

