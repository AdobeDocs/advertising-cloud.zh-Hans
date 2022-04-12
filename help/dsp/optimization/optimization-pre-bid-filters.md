---
title: 版面级别的预竞价过滤器及其使用方法
description: 引用可用的版面级别的预竞价过滤器，并了解如何使用它们。
feature: DSP Optimization
exl-id: c699e970-84ca-429b-8062-81804e6c9f21
source-git-commit: d17adc94a211992899e9f2eec6f9e13c16aa02c0
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# 版面级别的预竞价过滤器及其使用方法

| 竞价前过滤器 | 描述 | 何时使用此过滤器 |
| ---------------| ----------- | ---------------------- |
| [!UICONTROL Click Through Rate] | 为拍卖产生点进的概率设置最小预测阈值。 例如，如果将阈值设置为0.1%，则除非预测的点击概率大于或等于0.1%，否则您不会在拍卖中竞价。<br><br><b>注意：</b> 在优化目标之前应用过滤器。 因此，非常严格的过滤器可能会阻止支出。 | 当您的点进率(CTR)的KPI目标达到最低值，并且不想在CTR低于阈值时花费您的预算时，可使用。 此过滤器可能具有相当的限制，因此设置实际目标很重要。 根据对版面的其他限制，.03-.07%的目标通常是一个很好的起点。 您可以根据需要在网站级别对其进行优化，以帮助改进量度。<br><br>如果您的目标是实现最低CTR和最佳CPM，则建议的设置是将 [!UICONTROL Click Through Rate] 筛选，优化目标为“[!UICONTROL Lowest CPM].&quot; 如果您的目标是最大CPM，但没有对超额实现带来实际好处，则为最小CTR，则对 [!UICONTROL Click Through Rate] 筛选，优化目标为“[!UICONTROL Always Max Bid + Highest CTR]“ ”可能更合适。 |
| [!UICONTROL 100% Completion Rate] | 设置在展示竞价之前必须满足的最低完成率。 | 当营销活动的主要目标是完成率时，请使用此过滤器。 其他定位参数中的系数，但建议的起始百分比为65%。 |
| [!UICONTROL Player Size - Adobe] | 使用来自Advertising Cloud DSP的数据设置所需的最小播放器大小。 您会根据 [!UICONTROL Player Size] 阈值。 | 使用可确保使用DSP中的数据来交付整集播放器库存。 |
| [!UICONTROL Player Size 3rdParty (Moat/IAS)] | 使用 [!DNL Moat] 或 [!DNL Integral Ad Science] ([!DNL IAS])。 您会根据 [!UICONTROL Player Size] 阈值。 | 使用可确保您使用平台范围的内容交付整集播放器内容 [!DNL Moat] 或 [!DNL IAS] 数据。<br><br><b>注意：</b> 仅当营销活动配置为使用 [!DNL Moat] 或 [!DNL IAS] 数据。 |
| [!UICONTROL Viewability Adobe (MRC or [!DNL GroupM])] | 使用Advertising Cloud DSP可视性数字和测量值，设置所需的最小可视性百分比。 当满足指定的阈值时，您将根据展示进行竞价。<br><br><b>注意：</b><ul><li>如果营销活动的 [!UICONTROL Viewability Sensitivity] 设置为&quot;[!UICONTROL Standard (50% of ad in view for 2 consecutive seconds)]，” [!DNL Media Rating Council] (MRC)可见性度量标准用于营销活动。 如果 [!UICONTROL Viewability Sensitivity] 设置为&quot;[!UICONTROL Strict (100% of ad in view & audio on for 50% duration)]，” [!DNL GroupM] 可视性测量标准用于营销活动。</li><li>Adobe测量定义与第三方定义不同，因此与第三方数据可能存在细微差异。</li></ul> | 最佳做法是将优化目标和任何竞价前过滤器设置与营销活动的 [!UICONTROL Viewability Sensitivity] 设置。 |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [DSP如何优化您的营销活动](optimization-how-dsp-optimizes-campaigns.md)
>* [包设置](/help/dsp/campaign-management/packages/package-settings.md)
>* [版面设置](/help/dsp/campaign-management/placements/placement-settings.md)
>* [营销活动设置](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [优化目标及其使用方法](optimization-goals.md)

