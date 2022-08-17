---
title: 将DSP媒体曝光数据发送到Adobe Audience Manager概述
description: 了解如何使用Audience Manager事件像素从Advertising Cloud DSP促销活动中捕获展示级和点击级数据
feature: Integration with Adobe Audience Manager
source-git-commit: e861fc53ba14d783c763b291cdc618e5f1d4124f
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 0%

---

# 将DSP媒体曝光数据发送到Adobe Audience Manager概述

*仅使用Advertising Cloud DSP的广告商*

*仅具有Advertising Cloud-Adobe Audience Manager集成的广告商*

具有Adobe Audience Manager的Advertising Cloud DSP客户可以使用Audience Manager事件像素从DSP促销活动中捕获展示级数据和点击级数据。 事件像素将数据作为可操作信号发送到Audience Manager。 这些信号可支持各种DSP用例，例如更高级的分段、频率管理、营销分析和报表分析。

DSP不会向您收取发送这些信号的费用，而是Audience Manager。 但是，您需要根据您的Audience Manager合同，根据服务器调用支付标准Audience Manager摄取成本。 Audience Manager会删除以两种不同方式跟踪的重复事件，以便每个事件只计费一次。

>[!NOTE]
>
> Audience Manager还支持从广告服务器日志文件中捕获数据，这样提供的灵活性较低。 本文档未介绍该过程。

## 主要优势

* DSP促销活动数据会实时流入Audience Manager，您可以使用这些数据构建用于定义区段的基于规则的特征。

* 在用户特征和区段鉴别后，可以立即对区段进行定位，从而支持实时定位工作。

* 您可以利用促销活动数据来处理相关用例，例如创意元素的频度上限、重定向以前展示过促销活动的用户，以及分析下游网站行为和入口点。

* 汇总数据提供营销活动效果的统一视图，帮助识别自定义转化路径，并可用于改进通过Audience Manager导致转化的事件顺序 [!DNL Audience Optimization Reports] 或通过 [[!DNL Audience Analytics] 与Adobe Analytics集成](/help/integrations/audience-manager/audience-analytics.md).

## 数据的跟踪方式

Audience Manager展示和点击事件像素基于Cookie。 像素不会捕获在无Cookie环境(如移动设备应用程序和连接的电视(CTV))中发生的事件。

### 展示跟踪像素

Audience Manager在将1xl像素透明事件跟踪像素附加到广告时跟踪广告的展示数据。 每次向用户提供广告并由Web浏览器加载时，都会加载事件像素。 该像素是从特定于客户端的子域 [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html)，旧版Audience Manager域，包含键值对参数。 事件调用会收集展示次数和转化数据，并将其发送到Audience Manager数据收集服务器。

### 点击跟踪像素

Audience Manager跟踪的点击次数与展示次数类似，不同之处在于它不会在每次投放广告时加载透明的事件像素。 而是会在广告的点进URL中跟踪点击数据。 该广告指向 [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html)，这是旧版的Audience Manager域，用于由Audience Manager数据收集服务器进行处理。 然后，服务器将用户重定向到预期的登陆页面。 URL包含键值对参数。

>[!NOTE]
>
>如果贵组织使用 [!DNL Analytics] 跟踪，则您可能不需要Audience Manager点击跟踪。 Adobe Analytics会捕获点击信号，并可以将其发送到Audience Manager [服务器端转发](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

>[!MORELIKETHIS]
>
>* [从Advertising Cloud DSP促销活动中收集点击和展示数据](collect.md)
>* [用例](use-cases.md)

