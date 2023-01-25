---
title: 关于 [!UICONTROL CCPA Opt-out-of-Sale] 区段和报表
description: 了解如何创建区段以跟踪CCPA选择退出销售请求中的ID，以及如何检索ID报表。
feature: CCPA, DSP Segments
exl-id: 28b5e00b-a695-46f1-abbf-7bbd78f05411
source-git-commit: e9d9d51302d32b06af805917db2f46e5f6daee62
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# 关于 [!UICONTROL CCPA Opt-out-of-Sale] 区段和报表

您可以根据《加州消费者隐私法案》(CCPA)，通过以下方式在您的网站上跟踪来自消费者选择退出销售请求的用户ID: [创建和实施CCPA选择退出销售区段](ccpa-opt-out-segment-create.md). 用户将无限期地保留在CCPA选择退出销售区段中。

实施区段像素标记后，Adobe广告将开始代表广告商收集一个ID池。

## 消费者选择退出销售报表

Adobe广告会生成客户为帐户的选择退出销售请求提交的ID的月度报表。 该数据整合了使用在DSP中创建的CCPA选择退出销售区段捕获的请求以及通过Privacy ServiceAPI提交的任何请求。  报表是在每月的第一个月生成，具体时间为上个月。 例如，6月份的每月用户列表在7月1日可用。

每个报表都可作为以制表符分隔的文本文件进行压缩，格式为GZIP。 在CCPA选择退出销售区段中捕获的用户ID由区段和广告商进行标识。

您可以 [检索指向每月报表的链接](ccpa-opt-out-segment-report-retrieve.md) 之前三个月创建的受众(从DSP中或通过使用DSP [!DNL Trafficking API]. 每个链接的有效期为7天，但客户每次尝试检索一个链接时都会刷新。

>[!MORELIKETHIS]
>
>* [Adobe对《加州消费者隐私法案》的广告支持：消费者选择退出支持](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [创建和实施 [!UICONTROL CCPA Opt-Out-of-Sale] 区段](ccpa-opt-out-segment-create.md)
>* [检索消费者选择退出销售报表](ccpa-opt-out-segment-report-retrieve.md)
>* [关于受众管理](audience-about.md)

