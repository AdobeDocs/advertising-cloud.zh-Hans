---
title: 向 [!DNL FreeWheel]提交PG交易的广告
description: 了解如何通过FreeWheel与出版商就程序化保证交易请求广告批准。
feature: Private Inventory, Deal IDs
exl-id: null
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# 向FreeWheel提交程序化保证交易的广告

*仅具有程序 [!DNL FreeWheel] 保证权限的帐户*

在[接受与FreeWheel](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox)上的发布者进行的程序化保证交易（包括选择广告并创建用于交易的程序化保证默认位置）后，您必须将广告提交给FreeWheel以供审批。

>[!PREREQUISITES]
>
>与您的Adobe帐户团队合作，确保您的[!DNL DSP]帐户有权使用[!DNL FreeWheel]程序化保证工作流。

1. 复制与FreeWheel交易一起使用的广告的广告键：

   1. 单击营销活动的名称。

   1. 在子菜单中，单击&#x200B;**[!UICONTROL Ads]**。

   1. 单击广告名称旁边的&#x200B;**[!UICONTROL ...]>[!UICONTROL Edit]**。

   1. 打开广告设置后，复制URL中显示在浏览器地址栏中的字母数字广告键。

      例如，在以下URL中，广告键为`3NtNC5ZbaGZtqbei8jD3`

      `https://advertising.adobe.com/configurator/ad/3NtNC5ZbaGZtqbei8jD3?referrer=/playtime/ads`

1. 将广告提交到FreeWheel:

   1. 在[!UICONTROL Deals]视图中，找到交易。

   1. 在交易行中，单击![选项菜单](/help/dsp/assets/options-menu.png) **>[!UICONTROL submit to [!DNL FreeWheel]]**。

   1. 验证交易ID，输入您在步骤1中复制的&#x200B;**[!UICONTROL Ad Key]**，然后单击&#x200B;**[!UICONTROL Submit]**。

   必须先提交并批准广告，然后才能运行。

1. [检查广告提交状态](freewheel-check-status.md)。

>[!MORELIKETHIS]
>
>* [在FreeWheel中设置程序化保证交易概述](freewheel-overview.md)
>* [在交易ID收件箱中接受交易](deal-id-inbox-accept.md)
>* [检查程序化保证交易 [!DNL FreeWheel] 的广告状态](freewheel-check-status.md)
>* [FreeWheel广告提交的错误代码](freewheel-error-codes.md)

