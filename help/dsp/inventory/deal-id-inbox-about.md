---
title: 关于 [!UICONTROL Deal ID Inbox]
description: 了解 [!UICONTROL Deal ID inbox] 功能，允许您接受已与 [!DNL FreeWheel], [!DNL Google Authorized Buyers] (formerly known as [!DNL AdX]), and [!DNL Magnite DV+] (以前 [!DNL Rubicon])。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 959ad1d4-4671-4967-9f73-ec5b0464d0cd
source-git-commit: 2539d9b8ec7de7202dd6c3400dda85aa133853e3
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---

# 关于 [!UICONTROL Deal ID Inbox]

DSP [!UICONTROL Deal ID inbox] 允许您快速设置Advertising Cloud DSP通过供应方平台(SSP)从发布商导入的交易，这样您就不必手动设置每笔交易。 您可以接受您已与发布者协商的有保证和无保证的专用库存协议 [!DNL FreeWheel], [!DNL Google Authorized Buyers] (以前称为 [!DNL AdX])和 [!DNL Magnite DV+] (以前 [!DNL Rubicon]) [!UICONTROL Deal ID inbox].

>[!NOTE]
>
>Advertising Cloud DSP是第一个与集成的DSP [!DNL FreeWheel] API。

在 [!UICONTROL Deal ID inbox]，您可以在发布者看到交易详细信息时查看交易详细信息，加快交易设置，并避免手动输入错误。

<!-- 
Accepting a deal automatically pre-populates a new Deal ID record with details from the publisher, and you need to enter only the publisher [always? or just in some cases?], the media type, who can access the deal, and any attribute labels to apply to the deal so it's easy to find. [Are labels a dimension you can report on?]

For each available deal, you can review the deal details sent directly from the publisher. Some deals are grouped as proposals (packages), and you can see the individual deal details by reviewing the deal.
   
You can accept any available deal or move an incorrect deal to the Ignored Deals tab. You can also un-ignore deals, which moves them back to the New Deals tab so you can potentially accept them.

For each deal, you can select one publisher and one media type (Desktop Video, Mobile Video, Connected TV, Display, or Audio), and you can share the deal with specific advertisers and with all advertisers for a specific account.
 -->

DSP每天美国东部标准时间凌晨4点30分自动刷新所有交易详细信息。 它还会刷新所有 [!DNL FreeWheel] 通过 [!DNL Google] 和 [!DNL Magnite DV+] 每小时。 您还可以随时手动刷新交易详细信息以填充新交易。

<!-- MC: I'm not sure where I got the following. Is this currently true? -->
>[!NOTE]
>
>通过 [!DNL Google Authorized Buyers]，则您必须交付至少90%的预算，否则您的帐户将无法访问 [!DNL Google] 中的交易 [!UICONTROL Deal ID inbox].

## 实施 [!UICONTROL Deal ID Inbox]

要在 [!UICONTROL Deal ID inbox]，则您的SSP帐户必须将贵组织的DSP帐户映射到您的SSP帐户。 DSP将与相关SSP共享组织的帐户名称。 联系您的 [!DNL Adobe] 客户经理。

在交易谈判期间，请告知发布者将交易发送给您的买方，而不是父DSP帐户。 交易标识符可以是名称或ID，具体取决于SSP。

## 您可以对交易采取的操作

* **审核交易** 验证SSP是否发送了正确的发布者、投放日期、CPM和其他交易详细信息。 如果发布者出错，请在DSP外联系他们，以便他们更正并重新发送交易。

* **接受交易** 审核后，它们将不再显示在 [!UICONTROL Deal ID inbox]. 已接受的交易列在 [!UICONTROL Inventory] > [!UICONTROL Deals] 并准备好在广告商的版面中定位。

* **忽略交易** 不需要或未经请求的。 已忽略的交易将移至 [!UICONTROL Ignored Deals] 选项卡 [!UICONTROL Deal ID inbox]，用作存档。 当您忽略交易时，DSP不会提醒SSP和发布者。

* **修改已接受交易的详细信息** 从 [!UICONTROL Inventory] > [!UICONTROL Deals] (不在 [!UICONTROL Deal ID inbox])。 同样，当出版商向交易发送更改时，广告商负责在 [!UICONTROL Inventory] > [!UICONTROL Deals] 因为 [!UICONTROL Deal ID inbox] 在交易设置完成后，不会同步来自SSP的更改。

## 哪些类型的交易无法接受？

当交易列表不包含 ![接受](/help/dsp/assets/accept.png) 图标或 [!UICONTROL Accept] 按钮，您无法从 [!UICONTROL Deal ID inbox]. 相反，您可以 [手动创建交易ID详细信息](/help/dsp/inventory/deal-id-create.md).

您不能接受以下类型的交易：

* [!DNL Google] 不以美元计价的交易。

* [!DNL Magnite DV+] 不以美元计价的交易

* [!DNL FreeWheel] 不是您帐户货币的交易。

* 在今天之前具有结束日期的交易。

* 旧 [!DNL Magnite DV+] 标记为“多媒体类型”的交易。

交易细节包括交易无法接受的原因。

>[!MORELIKETHIS]
>
>* [在交易ID收件箱中接受交易](deal-id-inbox-accept.md)
>* [库存功能概述](inventory-overview.md)

