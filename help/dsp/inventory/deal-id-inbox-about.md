---
title: 关于[!UICONTROL Deal ID Inbox]
description: 了解[!UICONTROL Deal ID inbox]功能，该功能允许您接受您已与 [!DNL Google Authorized Buyers], [!DNL FreeWheel], and [!DNL Rubicon]上的发布者协商的私有交易。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 959ad1d4-4671-4967-9f73-ec5b0464d0cd
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# 关于[!UICONTROL Deal ID Inbox]

DSP [!UICONTROL Deal ID inbox]允许您快速设置Advertising Cloud DSP通过供应方平台(SSP)从发布者导入的交易，这样您就不必手动设置每笔交易。 您可以接受您已与[!UICONTROL Deal ID inbox]（以前称为[!DNL AdX]）、[!DNL FreeWheel]和[!DNL Rubicon]的发布者协商的有保证和无保证的专用库存交易。[!DNL Google Authorized Buyers]

>[!NOTE]
>
>Advertising Cloud DSP是第一个与[!DNL FreeWheel] API集成的DSP。

在[!UICONTROL Deal ID inbox]中，您可以在发布者看到交易详细信息时看到交易详细信息，加快交易设置，并避免手动输入错误。

DSP每天美国东部标准时间凌晨4点30分自动刷新所有交易详细信息。 它还会每小时刷新所有[!DNL FreeWheel]交易，并更新[!DNL Google]和[!DNL Rubicon]中的现有交易。 您还可以随时手动刷新交易详细信息以填充新交易。

<!-- MC: I'm not sure where I got the following. Is this currently true? -->
>[!NOTE]
>
>对于通过[!DNL Google Authorized Buyers]提供程序化保证的交易，您必须提供至少90%的预算，否则您的帐户将无法访问[!UICONTROL Deal ID inbox]中的[!DNL Google]交易。

## 实施[!UICONTROL Deal ID Inbox]

要在[!UICONTROL Deal ID inbox]中接收交易，您的SSP帐户必须将贵组织的DSP帐户映射到您的SSP帐户。 DSP将与相关SSP共享组织的帐户名称。 有关说明，请联系您的Adobe客户经理。

在交易谈判期间，请告知发布者将交易发送给您的买方，而不是父DSP帐户。 交易标识符可以是名称或ID，具体取决于SSP。

## 您可以对交易采取的操作

* **查看** 交易，以验证SSP是否发送了正确的发布者、投放日期、CPM和其他交易详细信息。如果发布者出错，请在DSP外联系他们，以便他们更正并重新发送交易。

* **审核** 后接受交易，它们将不再显示在 [!UICONTROL Deal ID inbox]中。已接受的交易列在[!UICONTROL Inventory] > [!UICONTROL Deals]中，并可以在广告商的版面中定位。

* **忽** 略不需要或未经请求的交易。已忽略的交易将移至[!UICONTROL Deal ID inbox]的[!UICONTROL Ignored Deals]选项卡中，该选项卡将用作存档。 当您忽略交易时，DSP不会提醒SSP和发布者。

* **修改已接受交易的详** 细信 [!UICONTROL Inventory] 息， [!UICONTROL Deals] 其方式为>(不在 [!UICONTROL Deal ID inbox]中)。同样，当发布者向交易发送更改时，广告商负责在[!UICONTROL Inventory] > [!UICONTROL Deals]中实施这些更改，因为[!UICONTROL Deal ID inbox]在交易设置后不会从SSP同步更改。

## 哪些类型的交易无法接受？

当交易列表不包含![接受](/help/dsp/assets/accept.png)图标或[!UICONTROL Accept]按钮时，您无法从[!UICONTROL Deal ID inbox]接受它。 相反，您可以手动[创建交易ID详细信息](/help/dsp/inventory/deal-id-create.md)。

您不能接受以下类型的交易：

* [!DNL Google] 不以美元计价的交易。

* [!DNL Rubicon] 不以美元计价的交易

* [!DNL FreeWheel] 不是您帐户货币的交易。

* 在今天之前具有结束日期的交易。

* 标记为“多媒体类型”的[!DNL Rubicon]旧交易。

交易细节包括交易无法接受的原因。

>[!MORELIKETHIS]
>
>* [在交易ID收件箱中接受交易](deal-id-inbox-accept.md)
>* [库存功能概述](inventory-overview.md)

