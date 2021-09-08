---
title: 关于[!UICONTROL CCPA Opt-out-of-Sale]区段和报表
description: 了解如何创建区段以跟踪CCPA选择退出销售请求中的ID，以及如何检索ID报表。
feature: CCPA, Segments
exl-id: 9256d34e-d0dd-4abf-bc96-2b599caf2a8e
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

---

# 关于[!UICONTROL CCPA Opt-out-of-Sale]区段和报表

您可以根据《加州消费者隐私法案》(CCPA)，通过[创建和实施CCPA选择退出销售区段](ccpa-opt-out-segment-create.md)，在您的网站上跟踪消费者选择退出销售请求的用户ID。 用户将无限期地保留在CCPA选择退出销售区段中。

实施区段像素标记后，Advertising Cloud将开始代表广告商收集一个ID池。

## 消费者选择退出销售报表

Advertising Cloud会生成客户为帐户的选择退出销售请求提交的ID的月度报表。 该数据整合了使用在Advertising Cloud DSP中创建的CCPA选择退出销售区段捕获的请求以及通过Privacy ServiceAPI提交的任何请求。  报表是在每月的第一个月生成，具体时间为上个月。 例如，6月份的每月用户列表在7月1日可用。

每个报表都可作为以制表符分隔的文本文件进行压缩，格式为GZIP。 在CCPA选择退出销售区段中捕获的用户ID由区段和广告商进行标识。

您可以[检索到在前三个月中创建的月度报表](ccpa-opt-out-segment-report-retrieve.md)的链接，这些报表可以是从Advertising Cloud DSP中创建的，也可以是使用Advertising Cloud [!DNL Trafficking API]创建的。 每个链接的有效期为7天，但客户每次尝试检索一个链接时都会刷新。

>[!MORELIKETHIS]
>
>* [Adobe Advertising Cloud对《加州消费者隐私法案》的支持：消费者选择退出支持](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html)
>* [创建和实施区 [!UICONTROL CCPA Opt-Out-of-Sale] 段](ccpa-opt-out-segment-create.md)
>* [检索消费者选择退出销售报表](ccpa-opt-out-segment-report-retrieve.md)
>* [关于受众管理](audience-about.md)

