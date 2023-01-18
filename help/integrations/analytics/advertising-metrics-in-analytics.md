---
title: Adobe广告量度在Analysis Workspace中
description: Adobe广告量度在Analysis Workspace中
feature: Integration with Adobe Analytics
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---

# Adobe广告量度在Analysis Workspace中

*仅具有Adobe广告与Adobe Analytics集成的广告商*

>[!NOTE]
>
>* Adobe广告将流量量度和维度传递到 [!DNL Analytics] 每日。
>* [!DNL Analytics] 实时捕获Adobe广告点进次数和显示点进次数。


## 来自Adobe广告的流量量度

>[!NOTE]
>
>中的所有Adobe广告流量量度 [!DNL Analytics] 从“AMO”开始。

| 流量量度 | 描述 |
| -------------- | ----------- |
| [!UICONTROL AMO Impressions] | Adobe广告展示次数。 |
| [!UICONTROL AMO Clicks] | Adobe广告总点击次数。 |
| [!UICONTROL AMO Cost] | Adobe广告支出以报表包的货币表示。 |
| [!UICONTROL AMO ID Instance] | 设置Adobe广告ID的次数。 |
| [!UICONTROL AMO Minutes Viewed] | 查看Adobe广告视频的分钟数。 |
| [!UICONTROL AMO Views] | 广告的查看次数。 当查看者启动Adobe广告视频时，即计为一次查看。 |
| [!UICONTROL AMO Views 25% Complete] | 观看Adobe广告视频至少25%的查看次数。 |
| [!UICONTROL AMO Views 50% Complete] | 观看Adobe广告视频至少50%的查看次数。 |
| [!UICONTROL AMO Views 75% Complete] | 观看Adobe广告视频至少75%的查看次数。 |
| [!UICONTROL AMO Views 100% Complete] | 观看了100%的Adobe广告视频的查看次数。 |
| [!UICONTROL AMO Viewable Impressions] | 根据版面配置测量的可查看展示次数。 |
| [!UICONTROL AMO Not Viewable Impressions] | 确定不可查看的展示次数。 此值计算为([!UICONTROL AMO Measurable Impressions] - [!UICONTROL AMO Viewable ])。 |
| [!UICONTROL AMO Measurable Impressions] | 成功初始化可视性工具的展示次数。 此值计算为（分析展示次数 — 不可测展示次数）。 |

## 用于Adobe广告的有用自定义计算量度

考虑为您的Adobe广告数据创建以下量度。

* 登陆页面实例的点击次数([!UICONTROL AMO ID Instances] / [!UICONTROL AMO Clicks]):这是点击了广告并将其发布到登陆页面的用户百分比。
* 可测量率([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Impressions] * 100)
* 可查看展示率([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Measureable Impressions] * 100)
* 每次查看成本([!UICONTROL AMO Cost] / [!UICONTROL AMO Views])
* 每次点击成本([!UICONTROL AMO Cost] / [!UICONTROL AMO Clicks])

## Adobe广告Dimension

>[!NOTE]
>
>中的所有Adobe广告维度 [!DNL Analytics] 后跟“(AMO ID)”。

| Dimension | 适用的Adobe广告数据 | 描述 |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP] 和 [!DNL Search] 数据 | Advertising DSP或搜索引擎名称 |
| [!UICONTROL Account (AMO ID] | [!DNL DSP] 和 [!DNL Search] 数据 | 帐户名称。 |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP] 和 [!DNL Search] 数据 | RTB([!DNL DSP])或广告网络名称([!DNL Search]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP] 和 [!DNL Search] 数据 | 营销活动名称。 |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP] 和 [!DNL Search] 数据 | 包([!DNL DSP])或组合([!DNL Search])名称。 |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] 数据 | 版面名称。 |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search] 数据 | 广告组名称。 |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search] 数据 | 关键词。 |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search] 数据 | 搜索匹配类型。 |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search] 数据 | 关键词和匹配类型。 |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] 和 [!DNL Search] 数据 | 广告类型，如 `text`, `video`, `display`或 `native`. |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] 和 [!DNL Search] 数据 | 广告类型([!DNL DSP])或广告标题([!DNL Search])。 |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] 和 [!DNL Search] 数据 | 广告描述([!DNL DSP])或广告正文([!DNL Search])。 |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search] 数据 | 广告中显示的URL。 |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search] 数据 | 广告的目标URL。 |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] 和 [!DNL Search] 数据 | 登陆页面条目是显示到达还是点进。 |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search] 数据 | 产品列表广告的产品目标。 |

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* [[!DNL Analytics] Adobe广告中的数据](/help/integrations/analytics/analytics-data-in-advertising.md)

