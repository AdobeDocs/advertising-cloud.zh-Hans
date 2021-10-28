---
title: 将PG交易的广告提交到 [!DNL FreeWheel]
description: 了解如何通过FreeWheel与出版商就程序化保证交易请求广告批准。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: null
source-git-commit: c2caed80f0afc0cbe3572d01dc2c89f13ed13712
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---

# 向FreeWheel提交程序化保证交易的广告

*使用 [!DNL FreeWheel] 仅程序化保证权限*

一旦 [接受与FreeWheel上的出版商的程序化保证交易](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox)，包括选择广告并创建用于交易的程序化保证默认版面，您必须将广告提交到FreeWheel进行批准。

>[!PREREQUISITES]
>
>使用 [!DNL Adobe] 帐户团队来确保 [!DNL DSP] 帐户有权使用 [!DNL FreeWheel] 程序化保证的工作流。

## 复制广告键以用于 [!DNL FreeWheel] 交易 {#copy-ad-key}

1. 单击营销活动的名称。

1. 在子菜单中，单击 **[!UICONTROL Ads]**.

1. 单击  **[!UICONTROL ...]>[!UICONTROL Edit]** 广告名称旁边。

1. 打开广告设置后，复制URL中显示在浏览器地址栏中的字母数字广告键。

例如，在以下URL中，广告键为 `3NtNC5ZbaGZtqbei8jD3`

`https://advertising.adobe.com/configurator/ad/3NtNC5ZbaGZtqbei8jD3?referrer=/playtime/ads`

## 从 [!UICONTROL Ads] 查看

1. [复制广告的广告键](#copy-ad-key).

1. 在广告名称旁边，单击  **[!UICONTROL ...]>[!UICONTROL submit to FreeWheel]**.

1. 验证交易ID，输入 [the **[!UICONTROL Ad Key]**](#copy-ad-key)，然后单击&#x200B;**[!UICONTROL Submit]**.

   必须先提交并批准广告，然后才能运行。

1. [检查广告提交状态](freewheel-check-status.md).

## 从 [!UICONTROL Deals] 查看

1. [复制广告的广告键](#copy-ad-key).

1. 在主菜单中，单击 **[!UICONTROL Inventory]> [!UICONTROL Deals].**

1. 在交易行中，单击 ![“选项”菜单](/help/dsp/assets/options-menu.png) **>[!UICONTROL submit to FreeWheel]**.

1. 验证交易ID，输入 [the **[!UICONTROL Ad Key]**](#copy-ad-key)，然后单击&#x200B;**[!UICONTROL Submit]**.

   必须先提交并批准广告，然后才能运行。

1. [检查广告提交状态](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [在FreeWheel中设置程序化保证交易概述](freewheel-overview.md)
>* [在交易ID收件箱中接受交易](deal-id-inbox-accept.md)
>* [检查广告的状态 [!DNL FreeWheel] 程序化保证交易](freewheel-check-status.md)
>* [FreeWheel广告提交的错误代码](freewheel-error-codes.md)

