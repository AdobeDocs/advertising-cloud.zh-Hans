---
title: 为何Advertising Cloud和 [!DNL Marketing Channels]之间的渠道数据可能有所不同
description: 了解为何AMO ID跟踪的渠道数据会因 [!DNL Analytics Marketing Channels]跟踪的渠道数据而异。
feature: Integration with Adobe Analytics
exl-id: null
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# 为何Advertising Cloud和[!DNL Marketing Channels]之间的渠道数据可能有所不同

*仅具有Advertising Cloud-Adobe Analytics集成的广告商*

用户在了解Advertising Cloud与[!DNL Marketing Channels]数据集集成时遇到的一个常见问题是：“AMO ID与[!DNL Marketing Channels]之间数据差异的原因是什么？” 或者，有时，“为什么数据会损坏？ 我需要所有量度才能在报表中进行匹配。” 幸运的是，差异并不表示数据是“已损坏”的，差异是预期甚至是预期的。 让我们来了解为何会以这种方式设计集成。

这两个数据集的主要用例不同：

* [!DNL Marketing Channels]:的主要用例是 [!DNL Marketing Channels] 使用通用的归因模型比较多个渠道的数据。分析人员可以使用[!UICONTROL Marketing Channel]维度更深入地了解渠道如何彼此交互。 此洞察有助于推动就如何投资每个渠道做出宏观决策，并有助于分析每个渠道的访客如何与网站交互。

   因此， [!DNL Analytics] [!UICONTROL Marketing Channel]维度配置为捕获和跟踪所有通道。 [!DNL Marketing Channels] 还可以配置为捕获Advertising Cloud DSP显示点进次数和点进次数，并且这与其他营销渠道相关。

* Advertising Cloud AMO ID:Advertising Cloud AMO ID数据的主要用例是为Advertising Cloud支持的高级[!DNL Adobe Sensei]竞价算法提供信息。 这些算法会自动做出每天数千个微观级别的竞价决策，以最大化广告支出并实现[!DNL DSP]促销活动或[!DNL Search]产品组合的目标。 算法可以将促销活动连接到的转化数据越多，算法就越能做出这些竞价决策。

   要收集此数据，[!DNL Analytics for Advertising Cloud]集成会传递原始AMO ID，这些ID可在Adobe Analytics的AMO ID维度中转换为点进和显示跟踪代码，该跟踪代码可存储为自定义变量(eVar)或保留变量(rVar)。 AMO ID维度中未设置其他渠道的点进次数，因此AMO ID维度无法跟踪来自这些其他渠道的登入。 结果，AMO ID会一直保留到[!DNL Marketing Channes]l个入口点。

有关Advertising Cloud跟踪数据与[!DNL Analytics]跟踪数据之间可能存在的数据差异的更多信息，请参阅“[ [!DNL Analytics] 和Advertising Cloud](../data-variances.md)之间的预期数据差异”。

>[!MORELIKETHIS]
>
>* [和之间的预期数 [!DNL Analytics] 据差异Advertising Cloud](/help/integrations/analytics/data-variances.md)
>* [的基本原理 [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [使用Advertising Cloud ID创建 [!DNL Marketing Channels] 处理规则](mc-ids.md)
>* [ [!DNL Analytics Marketing Channels] 使用Advertising Cloud数据](mc-ac-data.md)
>* [视频：使用Advertising Cloud报告 [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)

