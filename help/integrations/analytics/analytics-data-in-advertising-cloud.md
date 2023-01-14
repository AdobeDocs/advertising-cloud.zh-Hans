---
title: '"[!DNL Analytics] Adobe广告中的数据”'
description: '"[!DNL Analytics] Adobe广告中的数据”'
feature: Integration with Adobe Analytics
exl-id: 79fbc809-9965-41c1-971f-3652cc78fee3
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---

# [!DNL Analytics] Adobe广告中的数据

*仅具有Adobe广告与Adobe Analytics集成的广告商*

## Analytics区段

在中创建的所有区段 [!DNL Analytics] 和发布到Experience Cloud。

新区段需要24-48小时才能在Adobe广告中显示。 现有区段的更新将在大约八小时内同步。

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## 网站参与量度

>[!NOTE]
>
>* [!DNL Analytics] 将EF IDeVar的事件传递到Adobe广告。  默认集成不支持将计算量度或其他维度(eVar)发送到Adobe广告。 但是，如果计算量度可以在自定义事件中完全捕获，则Adobe广告可以摄取自定义事件。
>* [!DNL Analytics] 每小时向Adobe广告传递数据。


* [!UICONTROL Timespent_secs_1stvisit]:访客首次访问期间在网站上花费的秒数。
* [!UICONTROL Timespent_secs_total]:在点击回顾窗口内的所有访问中在网站上花费的总秒数。
* [!UICONTROL Pageviews_1stvisit]:访客首次访问网站期间的页面查看次数。
* [!UICONTROL Pageviews_total]:点击回顾窗口内所有访问中网站上的页面查看总数。
* [[!UICONTROL Bounces] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html)
* [[!UICONTROL Visits] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html)
* [!UICONTROL ef_id_instances]:该 [!DNL Analytics] 收集 [!UICONTROL EF ID].

## 转化量度

[!DNL Analytics] 每天将转化量度传递到Adobe广告。

### 标准转化量度

* [[!UICONTROL Revenue] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/revenue.html)
* [[!UICONTROL Orders] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/orders.html)
* [[!UICONTROL Units] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/units.html)
* [[!UICONTROL Carts] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/carts.html)
* [[!UICONTROL Cart Views] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-views.html)
* [[!UICONTROL Checkouts] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/checkouts.html)
* [[!UICONTROL Cart Additions] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-additions.html)
* [[!UICONTROL Cart Removals] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-removals.html)

### 自定义转化量度

这些量度是特定于报表包的，因此每个客户和报表包的可用量度会有所不同。

### 保留的转化量度

这些量度是特定于报表包的，因此每个客户和报表包的可用量度会有所不同。

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* [Adobe广告量度在Analysis Workspace中](/help/integrations/analytics/advertising-cloud-metrics-in-analytics.md)

