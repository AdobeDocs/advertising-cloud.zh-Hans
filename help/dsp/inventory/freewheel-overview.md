---
title: 在中设置PG交易概述 [!DNL Freewheel]
description: 了解在以下方面运行广告所需的先决条件和额外步骤：与发布者进行编程保证交易 [!DNL Freewheel].
feature: DSP Private Inventory, DSP Deal IDs
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# 在中设置程序化保证交易概述 [!DNL Freewheel]

在 [!DNL Freewheel] 需要额外的权限和步骤。

>[!PREREQUISITES]
>
>使用 [!DNL Adobe] 帐户团队来确保 [!DNL DSP] 帐户具有以下权限：
>
>* 使用 [!DNL FreeWheel] 程序化保证工作流，它需要为程序化保证交易提交广告，以 [!DNL FreeWheel].
>
>* (如果您与需要 [!DNL Clearcast] 每个广告的时钟编号)在广告中包含时钟编号的权限。


## 工作流

1. 使用交易中指定的媒体类型创建广告。

   对于某些英国出版商，您必须包含 [!DNL Clearcast] 时钟号。

1. [接受交易ID](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox) 你已经和出版商谈过 [!DNL Freewheel] 使用交易ID收件箱。

   接受交易后，按照提示操作： 1)选择要用于交易的广告； 2)创建程序化保证的默认投放以提供该广告。

1. [将广告提交到 [!DNL Freewheel]](freewheel-submit.md)

   必须先提交并批准广告，然后才能运行。

1. [检查广告提交状态](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [在交易ID收件箱中接受交易](deal-id-inbox-accept.md)
>* [为程序化保证交易提交广告 [!DNL Freewheel]](freewheel-submit.md)
>* [检查广告的状态 [!DNL FreeWheel] 程序化保证交易](freewheel-check-status.md)
>* [的错误代码 [!DNL Freewheel] 广告提交](freewheel-error-codes.md)

