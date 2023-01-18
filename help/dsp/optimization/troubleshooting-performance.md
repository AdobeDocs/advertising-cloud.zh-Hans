---
title: 性能疑难解答
description: 参考常见性能问题并了解如何对其进行故障诊断。
feature: DSP Optimization
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---

# 性能疑难解答

| 问题 | 可能的原因 | 要采取的操作 |
| --- | --- | --- |
| 在职位上没有支出 | 版面不包括广告，和/或广告不活动。 | 验证所有预期广告是否已附加到版面并且已获得批准和激活。<br><br>此外，查看版面是否包含自定义广告时间表，这可能会限制每个广告的投放期限。 要从版面视图查看版面的广告计划，请单击  **[!UICONTROL ...]>[!UICONTROL Ad schedule]** 版面名称旁边。 |
|  | 受影响的日期不在配置的飞行日期之内。 | 检查投放日期在营销活动、包和版面级别是否&#x200B;有效。 |
|  | 预算目标已达到和/或不够高。 | 在营销活动、资源包和版面级别查看预算设置。 |
|  | 账户资金不够。 | 要查看您的帐户是否有充足资金，请转至 **[!UICONTROL Settings]>[!UICONTROL Account]** 看看 [!UICONTROL Usable Funds]. 如果需要添加更多资金，请联系 [!DNL Adobe] 客户团队。 |
|  | 没有可用的库存。 | 验证是否指定的库存源([!UICONTROL Public], [!UICONTROL Private]或 [!UICONTROL On Demand])包括：<ul><li>正确设置。</li><li>通过拍卖进行活动和发送。</li><li>与适用的广告和版面类型兼容。</li></ul><br>如果库存来源全部有效且有效，则尽可能定位其他或所有库存来源。 |
|  | 没有可用用户。 | 检查指定的受众目标是否包含足够的活动用户。 如果没有，请通过添加更多受众来扩展目标。 |
| 在职位上的低支出 | 的 [!UICONTROL Non Bids] 版面诊断报告的部分显示了版面未竞价的可能原因。 | [查看 [!UICONTROL Non Bids] 报告](/help/dsp/campaign-management/reports/placement-diagnostics.md) 以了解投资为何没有出价。  <!-- add link/edit text when file available: See the [in-depth guide to possible Non-Bid Reasons (NBR)](link) for more information. --> |
|  | 版面使用 [预竞价过滤器](/help/dsp/campaign-management/placements/placement-settings.md) 这就限制了投标。 | 将投标前过滤器的阈值降低5%，以评估支出和绩效的平衡。 <!-- wording? and are users just supposed to manually monitor whether it makes a difference? --><br><br>请记住，使用多个版面目标（如预先竞价过滤器、地理、库存和受众），可能会累积限制竞价和支出。 |
|  | 该职位的获胜率很低。 | 增加 [!UICONTROL Max Bid] 提高获胜率。<br><br><b>注意：</b> 库存价格可能因版面的定位而异。<br><br>10%的成功率被认为是健康的。 |
|  | 可用的库存数量较少。 | 尽可能定位其他或所有库存来源。<br><br>请记住，使用多个版面目标（如预先竞价过滤器、地理、库存和受众），可能会累积限制竞价和支出。 |
|  | 可用的用户数量较少。 | 检查指定的受众目标是否包含足够的活动用户。 如果没有，请通过添加更多受众来扩展目标。<br><br>请记住，使用多个版面目标（如预先竞价过滤器、地理、库存和受众），可能会累积限制竞价和支出。 |
|  | 该资源包包含大量活动版面。 | 减少资源包中的活动版面数量，或增加整个资源包预算。<br><br>如果资源包包含多个版面，但预算不足，则DSP可能无法为每个版面分配足够的预算。 每次投放应有机会每天至少花费2美元。 例如，如果您的资源包预算为每天10美元，则最好包含五个或更少的版面。&#x200B; |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [版面设置](/help/dsp/campaign-management/placements/placement-settings.md)
>* [包设置](/help/dsp/campaign-management/packages/package-settings.md)
>* [营销活动设置](/help/dsp/campaign-management/campaigns/campaign-settings.md)

