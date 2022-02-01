---
title: 创建 [!UICONTROL Simple Ad Serving] 交易
description: 了解 [!UICONTROL Simple Ad Serving] 使用事件跟踪像素的交易。
feature: DSP Simple Ad Serving
exl-id: d65d1d8e-4d10-4d1d-86d3-f4457c29ae8d
source-git-commit: 3e47fec28a17cb64de42309c0368293e1ef1cdea
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---

# 关于 [!UICONTROL Simple Ad Serving]

[!UICONTROL Simple Ad Serving] 通过单个专用版面，为指定的发布者和单个广告类型提供有保证的、非决策的广告投放和报告。 使用 [!DNL Simple Ad Serving] 当您的发布者无法通过交易ID执行交易时。 所有定位、预算步调和上限以及频率上限都由发布者处理。 通过事件跟踪像素执行这些交易。

使用 [!UICONTROL Simple Ad Serving]，则每个广告都由发布者（网站服务）直接提供，而DSP则提供一个事件跟踪像素，以发送给需要实施像素和流量DSP广告的发布者。 根据库存类型，事件像素可测量展示次数、点进次数和视频播放事件。

可用的广告类型如下：

* 桌面标准前置式广告
* 平板电脑和移动标准前置式广告
* 连接电视标准前置式
* 显示
* 音频

您可以创建 [!UICONTROL Simple Ad Serving] 交易 [!UICONTROL Inventory] > [!UICONTROL Deals] 中。 DSP会自动生成子类型为“[!DNL Simple ad serving]“ ”。 版面定位了交易，但不允许进行额外定位、预算或频度上限。 您只能编辑某些交易设置，如交易名称、CPM、展示次数和投放日期。<!-- If you need multiple tracking tags for a [!UICONTROL Simple Ad Serving] deal, create a duplicate deal. -->

[!UICONTROL Simple Ad Serving] 投放不符合帐户的可用资金或营销活动和一揽子预算。 但是，会跟踪支出并计入这些预算。 即使CPM为$0，也始终跟踪事件数据。

>[!MORELIKETHIS]
>
>* [创建 [!UICONTROL Simple Ad Serving] 交易](simple-deal-create.md)
>* [[!UICONTROL Simple Ad Serving] 设置](simple-deal-settings.md)
>* [查看事件跟踪像素 [!UICONTROL Simple Ad Serving] 交易](simple-deal-show-pixels.md)

