---
title: 将PG交易的广告提交到 [!DNL FreeWheel]
description: 了解如何请求批准广告，以便与发布者在 [!DNL Freewheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: null
source-git-commit: 02dc96c5aeceb61762cf52c684ec8a607d6afb2a
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# 为程序化保证交易提交广告 [!DNL Freewheel]

*使用 [!DNL FreeWheel] 仅程序化保证权限*

一旦 [接受与FreeWheel上的出版商的程序化保证交易](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox)，包括选择广告并创建要用于交易的程序化保证默认版面，您必须将广告提交到 [!DNL Freewheel] 进行审批。

>[!PREREQUISITES]
>
>与您的Adobe帐户团队合作，确保 [!DNL DSP] 帐户有权使用 [!DNL FreeWheel] 程序化保证的工作流。

1. 复制与 [!DNL Freewheel] 交易：

   1. 单击营销活动的名称。
   1. 在子菜单中，单击 **[!UICONTROL Ads]**.
   1. 单击  **[!UICONTROL ...]>[!UICONTROL Edit]** 广告名称旁边。
   1. 打开广告设置后，复制URL中显示在浏览器地址栏中的字母数字广告键。

      例如，在以下URL中，广告键为 `3NtNC5ZbaGZtqbei8jD3`

      `https://advertising.adobe.com/configurator/ad/3NtNC5ZbaGZtqbei8jD3?referrer=/playtime/ads`

1. 将广告提交到 [!DNL Freewheel]:

   1. 执行以下任一操作：

      * 在广告名称旁边，单击  **[!UICONTROL ...]** > **[!UICONTROL submit to FreeWheel]**.
      * 在主菜单中，单击 **[!UICONTROL Inventory]** > **[!UICONTROL Deals]**. 在交易行中，单击 ![“选项”菜单](/help/dsp/assets/options-menu.png) > **[!UICONTROL submit to FreeWheel]**.
   1. 验证交易ID，输入 **[!UICONTROL Ad Key]** 在步骤1中复制，然后单击 **[!UICONTROL Submit]**.

   必须先提交并批准广告，然后才能运行。

1. [检查广告提交状态](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [在中设置程序化保证交易概述 [!DNL Freewheel]](freewheel-overview.md)
>* [在交易ID收件箱中接受交易](deal-id-inbox-accept.md)
>* [检查广告的状态 [!DNL FreeWheel] 程序化保证交易](freewheel-check-status.md)
>* [的错误代码 [!DNL Freewheel] 广告提交](freewheel-error-codes.md)

