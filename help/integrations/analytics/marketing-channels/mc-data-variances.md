---
title: 渠道数据为何会因Adobe广告和 [!DNL Marketing Channels]
description: 了解为何AMO ID跟踪的渠道数据会因跟踪的渠道数据而有所不同 [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# 渠道数据为何会因Adobe广告和 [!DNL Marketing Channels]

*仅具有Adobe广告与Adobe Analytics集成的广告商*

用户了解Adobe广告与 [!DNL Marketing Channels] 数据集是“导致AMO ID和 [!DNL Marketing Channels]?&quot; 或者，有时，“为什么数据会损坏？ 我需要所有量度才能在报表中进行匹配。” 幸运的是，差异并不表示数据是“已损坏”的，差异是预期甚至是预期的。 让我们来了解为何会以这种方式设计集成。

这两个数据集的主要用例不同：

* [!DNL Marketing Channels]:的主要用例 [!DNL Marketing Channels] 即使用通用的归因模型来比较多个渠道之间的数据。 分析人员可以使用 [!UICONTROL Marketing Channel] 维度，以更深入地了解渠道如何彼此交互。 此洞察有助于推动就如何投资每个渠道做出宏观决策，并有助于分析每个渠道的访客如何与网站交互。

   的 [!DNL Analytics] [!UICONTROL Marketing Channel] 因此，维度配置为捕获和跟踪所有渠道。 [!DNL Marketing Channels] 还可以配置为捕获DSP显示点进次数和点进次数，并且这与其他营销渠道相关。

* Adobe广告AMO ID:Adobe广告AMO ID数据的主要用例是为高级 [!DNL Adobe Sensei]竞价算法。 这些算法会自动做出每天成千上万个微观层面的竞价决策，以最大化广告支出并实现 [!DNL DSP] 营销活动或 [!DNL Search] 组合。 算法可以将促销活动连接到的转化数据越多，算法就越能做出这些竞价决策。

   要收集此数据，请 [!DNL Analytics for Advertising] 集成会传递原始AMO ID，这些ID可在Adobe Analytics的AMO ID维度中转换为点进和显示跟踪代码，该维度存储为自定义变量(eVar)或保留变量(rVar)。 AMO ID维度中未设置其他渠道的点进次数，因此AMO ID维度无法跟踪来自这些其他渠道的登入。 结果，AMO ID会在 [!DNL Marketing Channels] 入口点。

有关Adobe广告跟踪数据和 [!DNL Analytics] — 跟踪数据，请参阅“[之间的预期数据差异 [!DNL Analytics] 和Adobe广告](../data-variances.md).&quot;

>[!MORELIKETHIS]
>
>* [之间的预期数据差异 [!DNL Analytics] 和Adobe广告](/help/integrations/analytics/data-variances.md)
>* [的基本原理 [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [使用Adobe广告ID创建 [!DNL Marketing Channels] 处理规则](mc-ids.md)
>* [使用 [!DNL Analytics Marketing Channels] 使用Adobe广告数据](mc-ac-data.md)
>* [视频：使用 [!DNL Marketing Channels] (用于Adobe广告报告)](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)

