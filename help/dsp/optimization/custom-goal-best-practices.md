---
title: 构建自定义目标的最佳实践
description: 了解构建自定义目标以定义成功事件的最佳实践。
feature: DSP Optimization, DSP Best Practices
exl-id: 54b16325-4b72-48a3-a2e0-4e342229211c
source-git-commit: 7cb39998041d151ece7809adc8a2e872b922e5fc
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 0%

---

# 构建自定义目标的最佳实践

## 具有单个属性的自定义目标

以下示例显示如何配置定向单个属性（量度）的目标。

### 具有“[!UICONTROL Highest ROAS - Custom Goal]“优化目标

如果您的营销活动目标是收入([!UICONTROL Highest ROAS - Custom Goal])，则您的自定义目标（目标）将包括“[!UICONTROL Revenue]“属性，权重为一(1)。

![单个资产的ROAS自定义目标示例](/help/dsp/assets/custom-goal-roas.png)

>[!NOTE]
>
> A [!UICONTROL Property Weight] 一等于每跟踪1美元收入的值一。
>
> 例如，权重为1的250美元转化报告为250美元。 如果为转化量度分配的权重为0.5，则250美元的转化在Advertising Cloud中将报告为125美元（250美元的转化* 0.5） [!UICONTROL Property Weight] = $125)。

### 具有“[!UICONTROL Lowest CPA - Custom Goal]“优化目标

如果您的促销活动目标是每次客户获取(CPA)成本最低，并且只需要一个成功事件，则您将包含一个量度（在以下示例中为“应用程序提交”）。 最佳做法是将权重设置为一(1)。

![单个资产的CPA自定义目标示例](/help/dsp/assets/custom-goal-roas.png)

>[!NOTE]
>
> A [!UICONTROL Property Weight] 1等于跟踪的每次转化的值为1。
>
> 例如，如果跟踪了10个应用程序提交转化，则会报告10个应用程序提交转化。  如果为转化量度分配的权重为0.5，则在Advertising Cloud中，10个转化将报告为5(5)个（10个转化* 0.5） [!UICONTROL Property Weight] = 5)。

## 具有多个属性的自定义目标

在以下两种情况下，您可以在自定义目标中使用多个资产：

* 您的营销活动目标包含多个成功事件。 例如，您可能正在为多个现场操作进行广告，并且所有这些操作都归因于您的CPA目标。 以下示例目标包括三个不同的属性(“PDF下载”、“联系我们”和“电子邮件注册”)，每个属性的权重为一(1)，用于告知 [!DNL Adobe Sensei] 算法，每个属性具有同等的重要性。 如果包含具有不同成本或重要性的属性，则可以相应地调整其相对权重。

   ![具有多个属性的自定义目标示例](/help/dsp/assets/custom-goal-multiple-properties.png)

* 自定义目标中的单个属性未能达到优化性能所需的每日至少10次转化。 由于每日资源包支出最少或自然转化次数有限，可能会发生这种情况。 向自定义目标添加其他支持属性可以帮助您达到每天10次转化的阈值。 10个支持事件可帮助资源包达到10天/天的阈值，即使其每个权重都低于一(1)。 但是，您可能不需要添加这么多事件。

   在向自定义目标中添加支持属性时，请根据属性对主要成功事件的相对重要性对其进行加权，并记住数据点的数量。 这允许Adobe Sensei算法平衡多个属性并针对您的目标进行优化。

   以下示例目标包括三个属性，每个属性的权重不同：应用程序提交= 1，应用程序开始= 0.1，广告商登陆页= 0.01。这意味着，每个应用程序提交转化对您的业务具有与平均10个应用程序开始转化和100个广告商登陆页转化相同的价值。

   ![具有多个属性的自定义目标示例](/help/dsp/assets/custom-goal-multiple-properties2.png)

   相反，如果您对提交的登陆页面访问量进行同等的加权，则登陆页面访问量自然会更高，从而无法满足您的目标并导致登陆页面访问量出现偏差。<!--reword-->

>[!MORELIKETHIS]
>
>* [关于自定义目标](custom-goal-about.md)
>* [创建自定义目标](custom-goal-create.md)
>* [优化目标及其使用方法](optimization-goals.md)
>* [包设置](/help/dsp/campaign-management/packages/package-settings.md)
> * [DSP如何优化您的营销活动](optimization-how-dsp-optimizes-campaigns.md)

