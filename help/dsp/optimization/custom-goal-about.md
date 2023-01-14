---
title: 关于自定义目标
description: 了解自定义目标，以在针对最低CPA或最高ROAS优化的资源包中定义成功事件。
feature: DSP Optimization
exl-id: 623cb1ef-85ab-4535-aa3a-8e6ec8ae15ee
source-git-commit: ad4ab8b9b0a4b5b1cc4aab540900363d2fe671c2
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---

# 关于自定义目标

自定义目标定义广告商实现其业务目标所需的成功事件。 每个使用优化目标的包“[!UICONTROL Highest ROAS - Custom Goal]&quot;或&quot;[!UICONTROL Lowest CPA - Custom Goal]“必须包含有助于实现整体优化目标的自定义目标。 您可以将自定义目标创建为 *目标* in [!DNL Adobe Advertising Search].

![自定义目标](/help/dsp/assets/objective-goals.png)

每个自定义目标都包含一个或多个量度，或 *交易属性*，以及这些事务属性的相对权重。 可用的交易属性包括使用Adobe广告转化像素和通过Adobe Analytics跟踪的所有量度。

>[!NOTE]
>
>* [!DNL Analytics] 维度和区段不可用于Adobe广告优化。
>* 要在DSP中使用Analytics事件，请使用 [!DNL Adobe] 帐户团队来配置广告商级别的集成。
>* [!DNL Analytics] 自定义事件遵循以下命名约定： `custom_event_[*event #*]_[*Analytics report suite ID*]`. 示例： `custom_event_16_examplersid`


例如，假设三个量度（交易属性）与您其中一个营销活动中的特定包相关：“PDF下载”价值为20美元、“电子邮件注册”价值为30美元和“订单确认”价值为40美元。 如果您想要根据客户操作的一次性货币价值赋予权重，则属性的相对权重将为1、2和1.5。

请参阅 [创建自定义目标的最佳实践](custom-goal-best-practices.md) 以获取有关如何配置自定义目标的提示。

一旦 [创建自定义目标](custom-goal-create.md)，您可以 [将其分配给包](/help/dsp/campaign-management/packages/package-settings.md) 用于使用Adobe Sensei进行报告和算法优化。

>[!MORELIKETHIS]
>
>* [创建自定义目标](custom-goal-create.md)
>* [构建自定义目标的最佳实践](custom-goal-best-practices.md)
>* [优化目标及其使用方法](optimization-goals.md)
>* [包设置](/help/dsp/campaign-management/packages/package-settings.md)
> * [DSP如何优化您的营销活动](optimization-how-dsp-optimizes-campaigns.md)

