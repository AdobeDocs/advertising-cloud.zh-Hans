---
title: 附加 [!DNL Analytics for Advertising Cloud] 宏 [!DNL Flashtalking] 广告标记
description: 了解添加原因和方法 [!DNL Analytics for Advertising Cloud] 宏 [!DNL Flashtalking] 广告标记
feature: Integration with Adobe Analytics
source-git-commit: 915eea83b2dd246f0f512981efca7ac481cf0c6c
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# 附加 [!DNL Analytics for Advertising Cloud] 宏 [!DNL Flashtalking] 广告标记

*仅具有Advertising Cloud-Adobe Analytics集成的广告商*

*仅适用于Advertising Cloud DSP*

如果您使用 [!DNL Flashtalking] 对于Advertising Cloud DSP广告，将Analytics for Advertising Cloud参数附加到登陆页面URL。 这些参数允许Advertising Cloud将广告的点击数据发送到Adobe Analytics。

对使用宏 [!DNL Flashtalking] 以下类型的显示和视频广告 [!DNL Analytics for Advertising Cloud] 实施：

* **具有 [!DNL Adobe] [!DNL Analytics for Advertising Cloud] 在其网站上实施的JavaScript代码**:您应会在Adobe Analytics中通过Advertising Cloud购买的广告看到一些点进数据，这些数据中没有额外的宏。 要在不支持第三方Cookie的浏览器中捕获点进数据，因此不会通过JavaScript代码捕获这些数据，请将以下部分中的宏添加到您的 [!DNL Flashtalking] 广告标记。

>[!NOTE]
>
>JavaScript代码是仅在Cookie仍然可用时用于点击跟踪的解决方案。 Advertising Cloud中断Cookie后，将需要实施以下宏。

* **网站不使用的广告商 [!DNL Analytics for Advertising Cloud] JavaScript代码，而是依赖 [!DNL Analytics] 仅用于点进数据的服务器端转发** （不含任何显示到达数据）：要报告通过Advertising Cloud购买的广告所驱动的上门点击活动，需要以下宏。

## 显示广告标记

在 [!DNL Flashtalking] 广告标记设置中，将以下宏附加到点进URL的末尾 `Clicktag` 字段：

```html
?[ftqs:[AdobeAMO]]
```

示例：  `https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

![示例 [!DNL Flashtalking] 广告标记设置](/help/integrations/assets/macro-flashtalking-display-ad.png)

## 视频广告标记

在 [!DNL Flashtalking] 广告标记设置中，将以下宏附加到点进URL的末尾 `Clicktag` 字段：

```html
?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

示例：  `https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

![示例 [!DNL Flashtalking] 广告标记设置](/help/integrations/assets/macro-flashtalking-video-ad.png)

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising Cloud]](overview.md)


<!-- >* [Append [!DNL Analytics for Advertising Cloud] Macros to [!DNL Google Campaign Manager 360] Ad Tags](macros-google-campaign-manager.md) -->
