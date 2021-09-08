---
title: 实施 [!DNL Analytics for Advertising Cloud]的先决条件和关键信息
description: 实施 [!DNL Analytics for Advertising Cloud]的先决条件和关键信息
feature: Integration with Adobe Analytics
exl-id: 08e54e2b-ed9b-4489-8de5-ab1379b7133c
source-git-commit: e2ee41c7e3e195f062ad1cc67080ed913d6d3d06
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 0%

---

# 实施[!DNL Analytics for Advertising Cloud]的先决条件和关键信息

*使用Advertising Cloud DSP和Advertising Cloud Search的广告商*

在将Advertising Cloud与Adobe Analytics集成之前，请查看以下信息。

## [!DNL Analytics]中报告Advertising Cloud数据的要求

* Experience Cloud标识服务：`visitorAPI.js`版本2.0或更高版本
* 任何版本的Adobe Analytics（包括[!DNL Prime]、[!DNL Premium]或[!DNL Ultimate]）
* Adobe Analytics:`appMeasurement.js`版本2.1或更高版本

>[!TIP]
>
>要提高Experience Cloud保真度，请使用支持CNAME的最新版本的Analytics Identity Service，以及最新版本的Analytics AppMeasurement for JavaScript。

## 与Advertising Cloud共享Analytics区段的要求

* Experience Cloud标识服务：`visitorAPI.js`版本2.1或更高版本
* Adobe Analytics:`!DNL appMeasurement.js`版本1.8或更高版本

## 在Advertising Cloud中报告[!DNL Analytics]数据的要求

为Advertising Cloud实施团队提供以下信息：

* [!DNL Analytics]报表包ID，用于报告付费媒体活动和为网站活动提供馈送，以在Advertising Cloud中优化和报告
* 公司的Experience Cloud组织ID（组织ID）。

您可以在Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/run-debugger.html)的“摘要”屏幕上找到这两个ID。[

![Experience Cloud Debugger摘要屏幕](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Advertising Cloud中的数据 {#lookback-a4adc}

由于[!DNL Analytics]数据会发送到Advertising Cloud以进行报告和优化，因此该数据受属性规则(包括为Advertising Cloud中的广告商配置的展示和点击回顾窗口)的约束。

![Advertising Cloud中的广告商级别回顾窗口设置](/help/integrations/assets/a4adc-lookbacks.png)

* Advertising Cloud归因点击回顾窗口：首次单击后发生的天数，在该天数内，点击可归因于转化。 默认情况下，此值为60天；最长为90天
* Advertising Cloud归因展示回顾窗口：广告展示后可将展示归因于转化的天数。 默认情况下，此值为14天；最长为30天

   >[!NOTE]
   >
   > 展示回顾窗口特定于Advertising Cloud，而不是[!DNL Analytics for Advertising Cloud]报表。

[!DNL Analytics for Advertising Cloud] JavaScript使用这些设置来确定在多久之前将站点的显示到达条目或点进条目视为有效。 有关如何确定显示到达次数和点进次数的更多信息，请参阅“[Analytics使用的Advertising Cloud ID](ids.md)”。

## Advertising Cloud数据([!DNL Analytics])

[!DNL Analytics] 在Analytics点击中设置Advertising Cloud ID(AMO ID)，但受广告商的eVar持久性设置的约束，该设置同时适用于点进次数和显示到达次数。持久性设置在Advertising Cloud后端配置，您的Adobe客户经理可以更改该设置。

* [!DNL Analytics for Advertising Cloud] eVar过期：AMO ID默认为60天

>[!NOTE]
>
>要对不同时间范围的数据进行分段，您可以[在Analysis Workspace中设置具有不同回顾窗口的自定义区段](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html)。

## 支持的广告环境

* 搜索
* 显示
* 视频
* 在线视频
* 本机

请联系您的Adobe客户经理，以了解每个渠道中支持的最新广告环境。

## 实施前注意事项

* 此集成不会收取任何额外费用，服务器调用也不会产生额外的[!DNL Analytics]或Advertising Cloud费用。

* [!DNL Analytics for Advertising Cloud] 与广告服务器无关：显示到达或点进可能会从任何广告服务器发生，并且在登入网站时会生成相应的ID。

* 该集成仅将[!DNL Analytics]标准事件和自定义事件传递到Advertising Cloud，以优化后续付费媒体和广告工作的竞价。 它不会将[!DNL Analytics]区段、计算量度和eVar传递到Advertising Cloud以进行竞价优化。

* Advertising Cloud会根据用户进入网站前点击或查看的上次广告在[!DNL Analytics]中创建永久性ID，具体取决于Advertising Cloud中配置的[点击和查看回顾窗口](#lookback-a4adc)。 如果网站访客在其配置文件中具有两种类型的网站登录交互，并且该点击位于回顾期内，则访客的点进ID将覆盖网站报表的显示到达ID。

* [!DNL Analytics for Advertising Cloud] Adobe Analytics中的转化跟踪使用可配置的跟踪回顾窗口（默认为60天）。Advertising Cloud报表反映整个跟踪回顾窗口结束时的网站转化和参与度。

* 支持所有广告类型。 但是，并非所有广告环境都受支持。

   例如，不跟踪连接的电视(CTV)广告，因为CTV中不会进行点击，并且同一设备上不会进行转化。 但是，如果在桌面环境中查看广告，则可能会跟踪一些浏览网站登入数据。

* [!DNL Analytics] 当前只跟踪转化并将其归因于同一设备上的访客。

* [!DNL Analytics for Advertising Cloud] 不支持应用程序内显示到达转化。

* 使用[!DNL Analytics]的服务器端转发实施的广告商不支持显示到达跟踪。

### 补充ID

为网站实施Experience Cloud标识服务后，包含[!DNL Analytics]或Advertising Cloud数据的点击将包含补充ID。

示例：`sdid=2F3C18E511F618CC-45F83E994AEE93A0`

为了实现准确的数据集成，[!DNL Analytics for Advertising Cloud]活动用于交付内容或记录目标量度的所有Advertising Cloud调用必须具有共享相同补充ID的对应[!DNL Analytics]点击。

在[!DNL Analytics]中进行故障诊断时，请务必确认[!DNL Analytics]点击存在补充ID。 在[Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html)中，您可以在Advertising Cloud选项卡中将此ID看作`sdid`参数。

>[!NOTE]
>
> 此实施的工作方式与[!DNL Analytics for Target]集成类似。

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [适用于Analytics for Advertising Cloud的JavaScript代码](/help/integrations/analytics/javascript.md)

