---
title: 包设置
description: 请参阅可用包设置的描述。
feature: DSP Packages
exl-id: b4d415d1-86a5-40bd-b645-1709b267c174
source-git-commit: 7fe6eb31d3330c5470077ca2766c41ae07c6c67f
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 0%

---

# 包设置

## [!UICONTROL Basic Details]

**[!UICONTROL Name]:** 包名称。 最大长度为60个字符。

**[!UICONTROL Description]:** （可选）包的描述。

**[!UICONTROL 3rd Party Billed Fees]:** （可选）要作为不可计费成本进行跟踪的静态第三方费用：

>[!NOTE]
>
>计费费用反映在 [!UICONTROL Net CPM] 量度。
* **[!UICONTROL CPM]:** 每1000次展示次数的成本(CPM)。

* **[!UICONTROL CPM Description]:** CPM费用的描述。

您可以在 [投放级别](/help/dsp/campaign-management/placements/placement-settings.md).

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]:** （现有包的只读）在哪个级别上调整和限制包中的放置：

* **[!UICONTROL Package level pacing]:** 此步调策略通过步调和将所有包含的版面设置为 *群组*. 此策略可确保整体优化给定包中的所有版面，并根据绩效和规模将支出分配到选定的关键绩效指标(KPI)。

* **[!UICONTROL Placement level pacing]:**  此步调策略通过步调和封顶所有包含的版面来操作 *单独*. 最佳做法是仅使用此策略执行有保证的私有市场交易。

**[!UICONTROL Flight Dates]:** 包的开始日期和结束日期。

要选择为包创建非均匀步调，请选择 *[!UICONTROL *Activate Custom Flighting]**并在 [!UICONTROL Flighting] 部分。 启用自定义照明并保存包后，便无法禁用自定义照明。

>[!NOTE]
>
>* 投放日期必须包含在营销活动投放日期中。 此外，分配给此包的所有版面的投放日期必须包含在这些日期内。
> * 激活自定义照明时，无法编辑包的开始日期。


**[!UICONTROL Budget]:** （仅包级步调的包）总预算上限和预算间隔。

对于具有自定义照明的包，预算间隔始终为 *[!UICONTROL All time]*. 对于没有自定义闪烁的包，指定预算间隔： *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* 或 *[!UICONTROL Weekly]*.

**[!UICONTROL Gross Budget]:** （仅具有包级别步调和动态利润管理的包）包期间的总预算上限。

**[!UICONTROL Optimization Goal]:** （仅具有包级别步调的包）包的优化目标。 请参阅 [优化目标及其使用方法](/help/dsp/optimization/optimization-goals.md).

**[!UICONTROL Custom Goals]:** （仅包含自定义优化目标） [自定义目标](/help/dsp/optimization/custom-goal-about.md) 包。 有关自定义目标和使用这些目标的营销活动的最佳实践的更多信息，请参阅  [构建自定义目标的最佳实践](/help/dsp/optimization/custom-goal-best-practices.md) 和 [设置效果促销活动的最佳实践](/help/dsp/optimization/campaign-best-practices-performance.md).

**[!UICONTROL Package Goal Type]:** （仅包含自定义优化目标）包的用途。 此设置有助于确定如何优化资源包：

* *[!UICONTROL Prospecting]:* 潜在客户包的重点是获取新客户。

* *[!UICONTROL Retargeting]:* 重定位资源包的重点是重新公开先前的访客或客户。

* *[!UICONTROL Other]:* 所有其他目的。

**[!UICONTROL Linked Package for Optimization Learnings Carryover]:** （仅限具有自定义优化目标的包）其历史数据用作优化包的输入的其他包。

**[!UICONTROL Target]:** （仅具有包级别步调的包）目标目标，用于跟踪性能。

>[!NOTE]
>
>此字段仅作为基准，不用于决策。

**[!UICONTROL Frequency Cap]:** （仅具有包级步调的包）唯一设备或人员的次数(取决于指定的 [!UICONTROL Cross Device Level] （对于促销活动）可以从包中投放广告。 选项包括 *[!UICONTROL Unlimited]* 或每天、每周或每月的特定金额。

>[!NOTE]
>
>* 您可以在营销活动、资源包和版面级别设置频率上限。 DSP遵循营销活动层次结构中最严格的频率上限。
>* 最佳做法是在资源包级别为潜在客户和重定向设置频率上限。
> * 频率上限越高，支出和展示次数就越高，但访问次数越低。 较低的频率限制会降低花费和展示次数，但会提高访问范围。


**[!UICONTROL Pace on]:** （仅包含包级步调的包）步调基于：

* *[!UICONTROL Budget]:* （默认）此选项在分配的资源包预算内提供尽可能多的展示次数。

* *[!UICONTROL Impressions]:* 此选项提供展示次数，直到在指定的间隔内达到指定数量为止。 选择此选项时，请指定展示次数和间隔： *总是，* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* 或 *[!UICONTROL Weekly]*.

**[!UICONTROL Pacing Fill Strategy]:** （仅具有包级步调的包）如何调整和交付步调：

* *[!UICONTROL Even]:* 在每次飞行中均匀地进行投放，目标是在上半段投放量的50%。

* *[!UICONTROL Slightly Ahead]:* （默认）加快交付速度，以便在飞行时长的一半内完成55-65%的交付。

<!-- replaced with ASAP -->
* *[!UICONTROL Frontload]:* 加快交付速度，使其在飞行途中完成65-75%。

* *[!UICONTROL Aggressive Frontload]:* 加快交付速度，使其在飞行途中完成75-85%。

## [!UICONTROL Flighting]

(具有包级步调和“[!UICONTROL Activate Custom Flighting]“启用”)整个 [!UICONTROL Flight Dates] 在 [!UICONTROL Goals & Budget] 中。

对于每次投放，输入开始日期、结束日期和目标展示次数。 要添加另一个飞行，请单击 **[!UICONTROL Add Flight]**.

>[!MORELIKETHIS]
>
>* [关于包管理](package-about.md)
>* [创建资源包](package-create.md)
>* [编辑资源包](package-edit.md)
>* [将版面附加到包](package-attach-placement.md)
>* [关于Campaign Management的常见问题解答](/help/dsp/campaign-management/campaign-management-faq.md)

