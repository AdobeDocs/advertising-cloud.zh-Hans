---
title: DSP如何优化您的营销活动
description: 了解DSP如何优化营销活动中的包。
feature: DSP Optimization
exl-id: 054582ef-b677-4725-b25c-b82bf3e5b43e
source-git-commit: d2ad7d47d9cf13411fc831526a6fa4ff698b0a15
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# DSP如何优化您的营销活动

本页概述了Advertising Cloud DSP优化引擎(由 [!DNL Adobe Sensei]，可优化营销策划中的包。 有关如何手动优化促销活动的提示和技巧，请与 [!DNL Adobe] 客户经理。 <!-- add link to trading playbook if we add it to help -->

包优化目标在两个级别运行：

* 对于每个包：DSP会根据投放的绩效，根据所选KPI，为包中的每个投放分配预算。

* 对于包中的每次置入/拍卖：DSP会计算每次投放竞价的实时经济KPI值，然后使用此值确定竞价。

   >[!NOTE]
   >
   >经济价值可以根据投资安排支出的好坏进行重大加权。 如果配售超出其支出目标，它将被允许购买质量较低的拍卖。 如果配售能够轻松实现其支出目标，那么它将专注于质量更高的拍卖。

## 包优化

DSP可以通过两种基本方式优化您的交付，其中20种变体可用于与您的特定性能目标保持一致。 您可以选择：

* 优先考虑性能比率

* 将成本效率与性能比作优先顺序

请参阅 [优化目标及其使用方法](optimization-goals.md) 以确定将帮助您实现KPI的优化目标。

### 优先考虑性能比率的包

对于优化目标，要优先确定绩效率，DSP会预测每次拍卖的绩效，并始终按最高竞价进行竞价。 适用的优化目标示例包括 [!UICONTROL Highest Viewability Rate], [!UICONTROL Highest Clickthrough Rate]，等等。

在以下情况下，此优化模式非常有效：

* 您已经知道有效/可接受的CPM级别（例如，历史基准）。

* 您愿意手动调整 [!UICONTROL Max Bid] ，如果您在扩展方面遇到困难。

* 你把规模优先于效率。

#### 步调逻辑 {#pacing-logic-performance}

* 如果支出速度加快，竞价将变得更有选择性，这样你只会在预计有较高表现率的拍卖会上竞价。

* 如果支出落后，竞价将变得不那么有选择性，这样你就会在拍卖上竞拍，预计拍卖的成绩会更低，以赶上步调一致的目标。

#### 清除价格/竞价底纹 {#clearing-price-performance}

DSP在执行步调逻辑后，通过清算价格预测模型运行建议的竞价。 如果预测指示竞价可以以对获胜率的最小降低来降低，则根据预测降低竞价。

### 将成本效率与性能比作优先级的软件包

对于某些优化目标， DSP会预测每次拍卖的效果并自动调整竞价，从不超过配售 [!UICONTROL Max Bid]. 适用的优化目标示例包括 [!UICONTROL Lowest CPM], [!UICONTROL Lowest CPA], [!UICONTROL Lowest Cost per View], [!UICONTROL Lowest Cost per Click]，等等。

#### 步调逻辑 {#pacing-logic-balanced}

* 如果支出速度加快，DSP就会更加注重价格，竞标的金额会降低，以此与步调一致的计划来换取获胜率。

* 如果还平衡了绩效量度(除 [!UICONTROL Lowest CPM])，则会将预测的KPI混合到竞价金额中。 因此，您会以更高价格竞拍预计“每成本”会更好的拍卖。

* 如果支出落后于速度，则DSP会降低对价格的敏感程度，并报价更高，直至 [!UICONTROL Max Bid]，用步调计划来交换赢率。

#### 清除价格/竞价底纹 {#clearing-price-balanced}

DSP在执行步调逻辑后，通过清算价格预测模型运行建议的竞价。 如果预测指示竞价可以以对获胜率的最小降低来降低，则根据预测降低竞价。

## 位置优化

投放预竞价过滤器是确保高性能的最严格方法。 DSP会在不同广告类型中战略性地使用预竞价过滤器，以便在每个广告包内的多个版面中实现性能目标。 您可以同时使用竞价前过滤器和包级别优化，也可以单独使用。

>[!NOTE]
>
>可用的预竞价过滤器因广告类型而异。 例如，对于标准显示版面，您可以按点进率和可视性进行筛选，但不能按完成率进行筛选。

请参阅 [版面级别的预竞价过滤器及其使用方法](optimization-pre-bid-filters.md) 以确定哪种竞价前过滤器可帮助您实现KPI。

>[!MORELIKETHIS]
>
>* [包设置](/help/dsp/campaign-management/packages/package-settings.md)
>* [版面设置](/help/dsp/campaign-management/placements/placement-settings.md)
>* [优化目标及其使用方法](optimization-goals.md)
>* [版面级别的预竞价过滤器及其使用方法](optimization-pre-bid-filters.md)
>* [性能疑难解答](/help/dsp/optimization/troubleshooting-performance.md)

