---
title: 优化目标及其使用方法
description: 引用可用的优化目标并查看何时使用它们。
feature: DSP Optimization
exl-id: 9bca09b5-9aa7-4009-a576-9b30cfddfd55
source-git-commit: 3852df160ec242f4755800ed44a30f42dff749fc
workflow-type: tm+mt
source-wordcount: '1611'
ht-degree: 0%

---

# 优化目标及其使用方法

| 优化目标 | 描述 | 何时使用此目标 |
| -----------| ---------- | ---------- |
| [!UICONTROL Always Max Bid & Highest Clickthrough Rate] | 通过包级别优化，预算分配将以最高点进率优先安排投放。<br><br>如果支出目标得到实现，拍卖评估将优先考虑CTR。 提交的竞价将始终为 [!UICONTROL Max Bid]但是，如果投资方案花得不错，那么预测的CTR门槛将会变得更严格。 | 促销活动类型：品牌策略<br><br>基准：最高点进率<br><br>广告类型：前置、显示<br><br><b>注意：</b> 如果您具有不需要超过的固定CPM目标和需要最大化的CTR目标，则使用此目标。 将最高竞价设置为所需的CPM目标，DSP将在尝试花费全部预算时实现尽可能最佳的CTR。 |
| [!UICONTROL Always Max Bid & Highest Completion Rate] | 通过包级别优化，预算分配将优先安排具有最高完成率的投放。<br><br>如果支出目标得到实现，拍卖评估将优先处理完成率。 提交的竞价将始终为设置的最高竞价，但如果投放投资效果好，预计的完成率阈值将会更加严格。 | 促销活动类型：品牌策略<br><br>基准：最高完成率<br><br>广告类型：仅前置广告<br><br><b>注意：</b> 如果您具有不需要超出的固定CPM目标和需要最大化的完成率目标，则使用此目标。 将最高竞价设置为所需的CPM目标，DSP将在尝试花费全部预算时达到尽可能最佳的完成率。 |
| [!UICONTROL Always Max Bid & Highest Engagement Rate] | 通过包级别优化，预算分配将优先安排具有最高参与率的投放。<br><br>如果支出目标得到实现，拍卖评估将优先考虑参与率。 提交的竞价将始终为设置的最高竞价，但如果投放投资效果好，预计的参与率阈值将会更加严格。 | 促销活动类型：品牌策略<br><br>基准：最高参与率<br><br>广告类型：仅限移动设备插播式广告<br><br><b>注意：</b> 如果您具有无需超出的固定CPM目标和需要最大化的参与目标，则使用此目标。 将最高竞价设置为所需的CPM目标，DSP将在尝试花费全部预算时达到尽可能最佳的参与率。 |
| [!UICONTROL Always Max Bid & Highest Viewability Rate (Adobe – GroupM)] | 通过包级别优化，预算分配将优先分配具有最高可见率的版面。<br><br>如果支出目标得到实现，拍卖评估将优先考虑可见性比率。 提交的竞价将始终为设置的“最高竞价”，但如果投放投资效果良好，则预计的可见性阈值将会更加严格。 | 促销活动类型：品牌策略<br><br>基准：最高可见性率<br><br>广告类型：仅交互式前置广告<br><br><b>注意：</b> 此目标将始终使用版面级别的最高竞价。<br><br>如果营销活动的“可视性敏感度”设置设置为“标准（连续2秒内50%的广告显示）”，则将为营销活动使用媒体评级委员会(MRC)可视性测量标准。 如果将营销活动设置为“严格（视频中广告的100%，持续时间为50%）”，则营销活动将使用GroupM可视性测量标准。 理想情况下，您应将促销活动设置与优化目标和竞价前过滤器设置相匹配。 |
| [!UICONTROL Always Max Bid & Highest Viewability Rate (Adobe – MRC)] | 通过包级别优化，预算分配将优先分配具有最高可见率的版面。<br><br>如果支出目标得到实现，拍卖评估将优先考虑可见性比率。 提交的竞价将始终为设置的“最高竞价”，但如果投放投资效果良好，则预计的可见性阈值将会更加严格。 | 促销活动类型：品牌策略<br><br>基准：最高可见性率<br><br>广告类型：仅交互式前置广告<br><br><b>注意：</b> 此目标将始终使用版面级别的最高竞价。<br><br>如果营销活动的“可视性敏感度”设置设置为“标准（连续2秒内50%的广告显示）”，则将为营销活动使用媒体评级委员会(MRC)可视性测量标准。 如果将营销活动设置为“严格（视频中广告的100%，持续时间为50%）”，则营销活动将使用GroupM可视性测量标准。 理想情况下，您应将促销活动设置与优化目标和竞价前过滤器设置相匹配。 |
| [!UICONTROL Always Max Bid & Highest Viewability Rate (IAS – MRC)] | 通过包级别优化，预算分配将优先分配具有最高可见率的版面。<br><br>如果支出目标得到实现，拍卖评估将优先考虑可见性比率。 提交的竞价将始终为设置的“最高竞价”，但如果投放投资效果良好，则预计的可见性阈值将会更加严格。 | 促销活动类型：品牌策略<br><br>基准：最高可见性率<br><br>广告类型：仅交互式前置广告<br><br><b>注意：</b> 此目标将始终使用版面级别的最高竞价。<br><br>当IAS的第三方数据通知算法时，此设置最有效。 仅当您为营销活动启用IAS集成时，才使用此目标。 |
| [!UICONTROL Highest ROAS – Custom Goal] | （仅在包级别提供）预算分配将优先分配具有最高广告支出回报(ROAS)的版面。<br><br>拍卖评估将优先处理ROAS。 如果支出目标已实现，则DSP将在降低CPM与提高ROAS之间取得平衡。 | 促销活动类型：性能<br><br>基准：最高收入<br><br>广告类型：显示、本机和视频<br><br><b>注意：</b> 请参阅“设置效果促销活动的最佳实践”以了解更多信息。 |
| [!UICONTROL Lowest CPA – Custom Goal] | （仅在资源包级别提供）预算分配将优先安排使用最低CPA的版面。<br><br>拍卖评估将优先考虑注册会计师。 如果支出目标已实现，则DSP将在降低CPM与降低CPA之间取得平衡。 | 促销活动类型：性能<br><br>基准：最低CPA<br><br>广告类型：显示、本机和视频<br><br><b>注意：</b> 请参阅“设置效果促销活动的最佳实践”以了解更多信息。 |
| [!UICONTROL Lowest Cost Per Click] | 通过资源包级别优化，预算分配将优先安排具有最低CPC的投放。<br><br>拍卖评估将优先考虑中油。 如果支出目标已实现，则DSP将在降低CPM与提高CTR之间取得平衡，以尝试降低CPC。 | 促销活动类型：品牌策略<br><br>基准：高效CPM和最高点进率<br><br>广告类型：前置、显示<br><br><b>注意：</b> 利用此目标，实现最佳CPC。 要保证最大CPM，请将其用作版面的最高竞价。 |
| [!UICONTROL Lowest Cost Per Completion] | 通过包级别优化，预算分配将优先安排置入项目，并在每次完成时以最低的成本完成。<br><br>拍卖评估将优先处理视频完成率(VCR)。 如果支出目标已实现，则DSP将在降低CPM与增加VCR之间取得平衡，以尝试降低每次完成的成本。 | 促销活动类型：品牌策略<br><br>基准：高效CPM和最高完成率<br><br>广告类型：仅前置广告 |
| [!UICONTROL Lowest Cost Per Engagement] | 通过包级别优化，预算分配将以最低的参与率优先安排投放。<br><br>拍卖评估将优先考虑参与率。 如果支出目标已实现，则DSP将尝试在降低CPM与降低每次参与成本之间取得平衡。 | 促销活动类型：品牌策略<br><br>基准：高效CPM和最高参与率<br><br>广告类型：仅限移动设备插播式广告 |
| [!UICONTROL Lowest CPM] | 通过包级别优化，预算分配将优先安排具有最低CPM的投放。<br><br>拍卖评估将优先考虑CPM。 如果支出目标已实现，则DSP将逐步降低CPM。 | 促销活动类型：品牌策略<br><br>基准：高效CPM<br><br>广告类型：前置、显示、CTV、本机、音频 |
| [!UICONTROL Lowest Cost Per View] | 与最低CPM的操作方式类似。 通过包级别优化，预算分配将优先安排具有最低CPM的投放。<br><br>拍卖评估将优先考虑CPM。 如果支出目标已实现，则DSP将逐步降低CPM。 | 促销活动类型：品牌策略<br><br>基准：高效CPM和最高点进率<br><br>广告类型：前置、显示 |
| [!UICONTROL Lowest vCPM (Adobe - GroupM)] | 通过资源包级别优化，预算分配将优先安排具有最低vCPM的投放。<br><br>拍卖评估将优先考虑vCPM。 如果支出目标已实现，则DSP将尝试在降低CPM与提高可见度之间取得平衡。 | 促销活动类型：品牌策略<br><br>基准：高效CPM和最高vCPM<br><br>广告类型：前置、显示<br><br><b>注意：</b> 使用此目标可实现最佳vCPM。<br><br>要保证最大CPM，请将其用作版面的最高竞价。 |
| [!UICONTROL Lowest vCPM (Adobe - MRC)] | 通过资源包级别优化，预算分配将优先安排具有最低vCPM的投放。<br><br>拍卖评估将优先考虑vCPM。 如果支出目标已实现，则DSP将尝试在降低CPM与提高可见度之间取得平衡。 | 促销活动类型：品牌策略<br><br>基准：高效CPM和最高vCPM<br><br>广告类型：前置、显示<br><br><b>注意：</b> 使用此目标可实现最佳vCPM。<br><br>要保证最大CPM，请将其用作版面的最高竞价。 |
| [!UICONTROL Lowest vCPM (IAS - MRC)] | 通过资源包级别优化，预算分配将优先安排具有最低vCPM的投放。<br><br>拍卖评估将优先考虑vCPM。 如果支出目标已实现，则DSP将尝试在降低CPM与提高可见度之间取得平衡。 | 促销活动类型：品牌策略<br><br>基准：高效CPM和最高vCPM<br><br>广告类型：前置、显示<br><br><b>注意：</b> 使用此目标可实现最佳vCPM。<br><br>要保证最大CPM，请将其用作版面的最高竞价。<br><br>当IAS的第三方数据通知算法时，此设置最有效。 仅当您为营销活动启用IAS集成时，才使用此目标。 |
| [!UICONTROL Lowest vCPM (Moat - GroupM)] | 通过资源包级别优化，预算分配将优先安排具有最低vCPM的投放。<br><br>拍卖评估将优先考虑vCPM。 如果支出目标已实现，则DSP将尝试在降低CPM与提高可见度之间取得平衡。 | 促销活动类型：品牌策略<br><br>基准：高效CPM和最高vCPM<br><br>广告类型：前置、显示<br><br><b>注意：</b> 使用此目标可实现最佳vCPM。<br><br>要保证最大CPM，请将其用作版面的最高竞价。<br><br>此设置在以下来源的第三方数据时最有效 [!DNL Moat] 通知算法。 仅当您启用了 [!DNL Moat] 集成。 |
| [!UICONTROL Lowest vCPM (Moat - MRC)] | 通过资源包级别优化，预算分配将优先安排具有最低vCPM的投放。<br><br>拍卖评估将优先考虑vCPM。 如果支出目标已实现，则DSP将尝试在降低CPM与提高可见度之间取得平衡。 | 促销活动类型：品牌策略<br><br>基准：高效CPM和最高vCPM<br><br>广告类型：前置、显示<br><br><b>注意：</b> 使用此目标可实现最佳vCPM。<br><br>要保证最大CPM，请将其用作版面的最高竞价。<br><br>此设置在以下来源的第三方数据时最有效 [!DNL Moat] 通知算法。 仅当您启用了 [!DNL Moat] 集成。 |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [设置效果促销活动的最佳实践](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [版面级别的预竞价过滤器及其使用方法](optimization-pre-bid-filters.md)
>* [营销活动设置](/help/dsp/campaign-management/campaigns/campaign-settings.md)

