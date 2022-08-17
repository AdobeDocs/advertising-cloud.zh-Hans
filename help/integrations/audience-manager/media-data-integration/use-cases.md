---
title: 用例
description: 了解与Advertising Cloud DSP共享媒体数据的用例Audience Manager
feature: Integration with Adobe Audience Manager
source-git-commit: 3980af19efa785c437cacbf479ca3eabbed73b1b
workflow-type: tm+mt
source-wordcount: '796'
ht-degree: 0%

---

# 在Adobe Audience Manager中捕获媒体曝光数据的用例

*仅使用Advertising Cloud DSP的广告商*

*仅具有Advertising Cloud-Adobe Audience Manager集成的广告商*

以下是从捕获Advertising Cloud DSP媒体曝光数据中获益的一些方法 <!-- ad impression data? --> Audience Manager。

## 回访间隔和频度管理

通过在Audience Manager中捕获展示数据，您可以通过创建已接触特定广告或营销策划的用户区段来增强频率管理。 如果要提高频度，可以将这些区段用于广告定位；如果要限制频度，则可以将其用于广告抑制。

此外，使用Audience Manager [!DNL Segment Builder]，您可以 [回访和频率控制](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/recency-and-frequency.html) 任意 [基于规则的特征](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) 包含可操作信号。 例如，这允许您限制在媒体营销活动中向用户显示特定创意内容的次数。 读取“[即时跨设备抑制](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/instant-cross-device-suppression.html)”以了解如何执行此操作。<!-- The AM pulled this paragraph verbatim from AEM doc; I change only a word or two. -->

## 顺序消息

通过捕获展示数据，您可以创建一个展示给营销活动或广告的用户区段，并使用该区段进行连续消息传送或抑制。 例如，您可以重新定位查看了创意内容的用户 `123` 但是没有通过显示创作元素来单击或转换 `456`.

要在Audience Manager中执行此示例，请执行以下步骤：<!-- The AM pulled this example/procedure verbatim from AEM doc; I changed only a word or two. -->

1. 创建特征以捕获查看了该创作元素的用户。

   例如，要命名特征 `Creative Trait 123`，请使用以下特征规则：

   `d_creative == 123 AND d_event == imp`

1. 创建特征以捕获单击或转换的用户。

   例如，要命名此特征，请执行以下操作 `Click and Converter`，请使用以下特征规则：

   `d_event == click OR d_event=conv`

1. 创建一个名为 `Retarget Users` 填充看到创意的用户 `123` 但未单击或转换。 使用以下特征规则：

   `Creative Trait 123 AND NOT Click and Converter`

1. 映射区段 `Retarget Users` 目标，并通过创意定位目标中的用户 `456`.

## [!DNL Adobe Audience Analytics] 和营销活动曝光数据

在Audience Manager中提供营销活动展示和点击数据后，您可以为接触特定营销活动或策略或与之进行交互的用户创建特征和区段。 使用 [[!DNL Audience Analytics] 集成](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html)，则您的Audience Manager区段可以与 [!DNL Analytics] 供进一步分析。 潜在用例包括：

* **DSP和Advertising Cloud Search广告之间的交互分析：** 标准 [[!DNL Analytics for Advertising Cloud] 集成](/help/integrations/analytics/overview.md) 无法深入分析DSP与 [!DNL Search] 因为两个渠道都使用遵循AMO ID归因规则的AMO ID，搜索点击会覆盖该规则的显示显示显示到达。 通过在Audience Manager中创建DSP曝光区段，您可以使用 [!DNL Audience Analytics] 分析DSP与 [!DNL Search] 广告 [!DNL Analytics].

* **频率分析：** 您可以在Audience Manager中创建区段，具体内容取决于用户在某个特定广告或营销策划中被显示的次数。 然后，您可以在Analytics中分析不同的曝光区段，以了解用户行为如何根据DSP的曝光数量而发生更改。

## [!DNL Audience Optimization Reports]

您可以利用 [Audience Manager [!DNL Audience Optimization Reports]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-reports.html) 为营销活动中的区段确定潜在的绩效机会。 这些报表将促销活动展示次数、点击次数和转化数据与区段量度相结合，以支持以区段为中心的优化以及有效的渠道组合。

### 相关Audience Optimization报表的类型

| 报表 | 描述 |
| ------ | ----------- |
| [[!UICONTROL Segment Performance] 报表](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/segment-performance.html) | 按展示次数和转化率比较映射区段和未映射区段。 |
| [[!UICONTROL Trend Analysis and Volume Analysis] 报告]9https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/trend-analysis-volume-analysis.html) | 返回广告维度的展示次数、点进率和转化数据。 |
| [[!UICONTROL Optimal Frequency] 报表](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/optimal-frequency.html) | 帮助您在提供的展示次数与转化次数之间找到最佳平衡。 它允许您调整要显示的展示次数，然后才能开始看到回报递减。 |
| [[!UICONTROL Unique User Reach] 报表](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/unique-user-reach.html) | 泡泡图，其中每个泡泡的大小与所选维度的独特用户数量成正比。 |

### 注意事项

* 如果 [!DNL Audience Optimization Reports] 用户具有基于角色的访问控制(RBAC), [!DNL Adobe Customer Care] 必须配置广告商ID与组织的Audience Manager数据源集成代码之间的映射。 然后，管理员用户可以向不同用户提供RBAC权限。

* 中的转化报表 [!DNL Audience Optimization Reports] 需要最终用户进行一些设置。 用户必须填充元数据文件。

* [!DNL Audience Optimization Reports] 不支持对促销活动元数据（例如促销活动名称或版面名称）进行更改。

* 搜索广告的点击量包含在 [!DNL Audience Optimization Reports] 只有在它们与展示次数相关时。 换言之，搜索点击将被视为展示次数后的转化。 因此，许多搜索点击可能未包含在 [!DNL Audience Optimization Reports].

>[!MORELIKETHIS]
>
>* [将DSP媒体曝光数据发送到Adobe Audience Manager概述](overview.md)
>* [从Advertising Cloud DSP促销活动中收集点击和展示数据](collect.md)

