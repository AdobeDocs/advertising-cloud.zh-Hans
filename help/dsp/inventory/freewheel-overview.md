---
title: 在FreeWheel中设置PG交易概述
description: '了解在FreeWheel上与出版商进行程序化保证交易时运行广告所需的先决条件和额外步骤。 '
feature: DSP Private Inventory, DSP Deal IDs
exl-id: null
source-git-commit: dfd5992f059645622b3a75d092d3eb7fe1bfa696
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---

# 在FreeWheel中设置程序化保证交易概述

在FreeWheel上与发布者建立程序化保证交易需要额外的权限和步骤。

>[!PREREQUISITES]
>
>使用 [!DNL Adobe] 帐户团队来确保 [!DNL DSP] 帐户具有以下权限。
>
>1. 使用 [!DNL FreeWheel] 程序化保证工作流，它需要为程序化保证交易提交广告，以 [!DNL FreeWheel].
>
>1. （如果您与英国出版商合作，后者要求每个广告都使用Clearcast时钟号）允许在您的广告中包含时钟号。


## 工作流

1. 使用交易中指定的媒体类型创建广告。

   对于某些英国出版商，您必须在广告中包含Clearcast时钟号。

1. [接受交易ID](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox) 您已使用“交易ID收件箱”与FreeWheel上的发行商进行协商。

   接受交易后，按照提示操作： 1)选择要用于交易的广告； 2)创建程序化保证的默认投放以提供该广告。

1. [将广告提交到FreeWheel](freewheel-submit.md)

   必须先提交并批准广告，然后才能运行。

1. [检查广告提交状态](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [在交易ID收件箱中接受交易](deal-id-inbox-accept.md)
>* [向FreeWheel提交程序化保证交易的广告](freewheel-submit.md)
>* [检查广告的状态 [!DNL FreeWheel] 程序化保证交易](freewheel-check-status.md)
>* [FreeWheel广告提交的错误代码](freewheel-error-codes.md)

