---
title: Advertising Cloud量度在Analysis Workspace中
description: Advertising Cloud量度在Analysis Workspace中
feature: Integration with Adobe Analytics
exl-id: d740bd19-c643-4917-9cfd-f9cf0affd07e
source-git-commit: 56ac178bf10d8c934297521ca3075783e1bc2c36
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---

# Advertising Cloud量度在Analysis Workspace中

*仅具有Advertising Cloud-Adobe Analytics集成的广告商*

>[!NOTE]
>
>* Advertising Cloud每天将流量量度和维度传递到[!DNL Analytics]。
>* [!DNL Analytics] 实时捕获Advertising Cloud点进次数和显示到达次数。


## 来自Advertising Cloud的流量量度

>[!NOTE]
>
>[!DNL Analytics]中的所有Advertising Cloud流量量度均以“AMO”开头。

| 流量量度 | 描述 |
| -------------- | ----------- |
| [!UICONTROL AMO Impressions] | Advertising Cloud展示次数。 |
| [!UICONTROL AMO Clicks] | 总Advertising Cloud点击次数。 |
| [!UICONTROL AMO Cost] | Advertising Cloud使用报表包的货币支出。 |
| [!UICONTROL AMO ID Instance] | 设置Advertising Cloud ID的次数。 |
| [!UICONTROL AMO Minutes Viewed] | 查看Advertising Cloud视频的分钟数。 |
| [!UICONTROL AMO Views] | 广告的查看次数。 查看者启动Advertising Cloud视频时，将计为一次查看。 |
| [!UICONTROL AMO Views 25% Complete] | 观看了Advertising Cloud视频至少25%的查看次数。 |
| [!UICONTROL AMO Views 50% Complete] | 至少50%的Advertising Cloud视频已观看的观看次数。 |
| [!UICONTROL AMO Views 75% Complete] | 观看了Advertising Cloud视频至少75%的查看次数。 |
| [!UICONTROL AMO Views 100% Complete] | 观看了Advertising Cloud视频100%的查看次数。 |
| [!UICONTROL AMO Viewable Impressions] | 根据版面配置测量的可查看展示次数。 |
| [!UICONTROL AMO Not Viewable Impressions] | 确定不可查看的展示次数。 此值计算为([!UICONTROL AMO Measurable Impressions] - [!UICONTROL AMO Viewable ])。 |
| [!UICONTROL AMO Measurable Impressions] | 成功初始化可视性工具的展示次数。 此值计算为（分析展示次数 — 不可测展示次数）。 |

## 有用的自定义计算量度(用于Advertising Cloud)

考虑为您的Advertising Cloud数据创建以下量度。

* 单击登陆页面实例([!UICONTROL AMO ID Instances] / [!UICONTROL AMO Clicks]):这是点击了广告并将其发布到登陆页面的用户百分比。
* 可测量率([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Impressions] * 100)
* 可查看展示率([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Measureable Impressions] * 100)
* 每次查看成本([!UICONTROL AMO Cost] / [!UICONTROL AMO Views])
* 每次点击成本([!UICONTROL AMO Cost] / [!UICONTROL AMO Clicks])

## Advertising CloudDimension

>[!NOTE]
>
>[!DNL Analytics]中的所有Advertising Cloud维度后跟“(AMO ID)”。

| Dimension | 适用的Advertising Cloud数据 | 描述 |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP] 和数 [!DNL Search] 据 | Advertising Cloud DSP或搜索引擎名称 |
| [!UICONTROL Account (AMO ID] | [!DNL DSP] 和数 [!DNL Search] 据 | 帐户名称。 |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP] 和数 [!DNL Search] 据 | RTB([!DNL DSP])或广告网络名称([!DNL Search]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP] 和数 [!DNL Search] 据 | 营销活动名称。 |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP] 和数 [!DNL Search] 据 | 包([!DNL DSP])或组合([!DNL Search])名称。 |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] 数据 | 版面名称。 |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search] 数据 | 广告组名称。 |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search] 数据 | 关键词。 |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search] 数据 | 搜索匹配类型。 |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search] 数据 | 关键词和匹配类型。 |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] 和数 [!DNL Search] 据 | 广告类型，如`text`、`video`、`display`或`native`。 |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] 和数 [!DNL Search] 据 | 广告类型([!DNL DSP])或广告标题([!DNL Search])。 |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] 和数 [!DNL Search] 据 | 广告描述([!DNL DSP])或广告正文([!DNL Search])。 |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search] 数据 | 广告中显示的URL。 |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search] 数据 | 广告的目标URL。 |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] 和数 [!DNL Search] 据 | 登陆页面条目是显示到达还是点进。 |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search] 数据 | 产品列表广告的产品目标。 |

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [[!DNL Analytics] Advertising Cloud中的数据](/help/integrations/analytics/analytics-data-in-advertising-cloud.md)

