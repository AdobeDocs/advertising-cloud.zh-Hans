---
title: 版面级别的预竞价过滤器及其使用方法
description: 引用可用的版面级别的预竞价过滤器，并了解如何使用它们。
feature: Optimization
exl-id: c699e970-84ca-429b-8062-81804e6c9f21
source-git-commit: 185fc7d79798a0a3a9ad5829b701aeb53a4a47c1
workflow-type: tm+mt
source-wordcount: '585'
ht-degree: 0%

---

# 版面级别的预竞价过滤器及其使用方法

| 竞价前过滤器 | 描述 | 何时使用此过滤器 |
| ---------------| ----------- | ---------------------- |
| [!UICONTROL Click Through Rate] | 为拍卖将导致点进的概率设置最小预测阈值。 例如，如果将阈值设置为0.1%，则除非预测的点击概率大于或等于0.1%，否则您不会在拍卖中竞价。<br><br><b>注意：</b> 在优化目标之前应用过滤器。因此，非常严格的过滤器可能会阻止支出。 | 当您的点进率(CTR)的KPI目标达到最低值，并且不想在CTR低于阈值时花费您的预算时，可使用。 此过滤器可能具有相当的限制，因此设置实际目标很重要。 根据对版面的其他限制，.03-.07%的目标通常是一个很好的起点。 您可以根据需要在网站级别对其进行优化，以帮助改进量度。<br><br>如果您的目标是实现最低CTR和最佳CPM，则建议的设置是将过滤器 [!UICONTROL Click Through Rate] 与优化目标“[!UICONTROL Lowest CPM]”结合使用。如果您的目标是最大CPM，但没有实现过高的实际好处，而且CTR最小，则将[!UICONTROL Click Through Rate]过滤器与优化目标“[!UICONTROL Always Max Bid + Highest CTR]”配对可能更合适。 |
| [!UICONTROL 100% Completion Rate] | 设置在展示竞价之前必须满足的最低完成率。 | 当营销活动的主要目标是完成率时，请使用此过滤器。 其他定位参数中的系数，但建议的起始百分比为65%。 |
| [!UICONTROL Player Size - Adobe] | 使用来自Advertising Cloud DSP的数据设置所需的最小播放器大小。 当满足[!UICONTROL Player Size]阈值时，您会根据展示进行竞价。 | 使用可确保使用DSP中的数据来交付整集播放器库存。 |
| [!UICONTROL Player Size 3rdParty (Moat/IAS)] | 使用[!DNL Moat]或[!DNL Integral Ad Science]([!DNL IAS])的数据设置所需的最小播放器大小。 当满足[!UICONTROL Player Size]阈值时，您会根据展示进行竞价。 | 使用可确保使用平台范围的[!DNL Moat]或[!DNL IAS]数据来交付整集播放器清单。<br><br><b>注意：</b> 仅当营销活动配置为使用或数据时，才使用 [!DNL Moat] 此过 [!DNL IAS] 滤器。 |
| [!UICONTROL Viewability IAS] | 使用[!DNL IAS]中的历史数据设置所需的最小可见性百分比。 当满足指定的阈值时，您将根据展示进行竞价。 | 当通过促销活动级别[!DNL IAS]集成提取更多数据时，此过滤器最有效。<br><br>当营销活动配置为使用数 [!DNL IAS] 据时，最佳实践是将此过滤器与包优化目标“[!UICONTROL Lowest vCPM (IAS)]”结合使用。如果未启用集成，则将此过滤器与优化目标“[!UICONTROL Lowest CPM]”一起使用。 |
| [!UICONTROL Viewability Moat] | 使用[!DNL Moat]中的历史数据设置所需的最小可见性百分比。 当满足指定的阈值时，您将根据展示进行竞价。 | 当通过促销活动级别[!DNL Moat]集成提取更多数据时，此过滤器最有效。<br><br>将营销活动配置为使 [!DNL Moat] 用数据时，最佳实践是使用包优化目标“[!UICONTROL Lowest vCPM (Moat)]”。如果未启用集成，则将此过滤器与优化目标“[!UICONTROL Lowest CPM]”一起使用。 |
| [!UICONTROL Viewability Adobe (MRC or [!DNL GroupM])] | 使用Advertising Cloud DSP可视性数字和测量值，设置所需的最小可视性百分比。 当满足指定的阈值时，您将根据展示进行竞价。<br><br><b>注意：</b><ul><li>如果营销活动的[!UICONTROL Viewability Sensitivity]设置为“[!UICONTROL Standard (50% of ad in view for 2 consecutive seconds)]”，则[!DNL Media Rating Council](MRC)可视性测量标准将用于营销活动。 如果[!UICONTROL Viewability Sensitivity]设置为“[!UICONTROL Strict (100% of ad in view & audio on for 50% duration)]”，则[!DNL GroupM]可视性测量标准将用于营销活动。</li><li>Adobe测量定义与第三方定义不同，因此与第三方数据可能存在细微差异。</li></ul> | 最佳做法是将优化目标和任何竞价前过滤器设置与促销活动的[!UICONTROL Viewability Sensitivity]设置相匹配。 |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [DSP如何优化您的营销活动](optimization-how-dsp-optimizes-campaigns.md)
>* [包设置](/help/dsp/campaign-management/packages/package-settings.md)
>* [版面设置](/help/dsp/campaign-management/placements/placement-settings.md)
>* [营销活动设置](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [优化目标及其使用方法](optimization-goals.md)

