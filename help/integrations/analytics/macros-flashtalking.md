---
title: 附加 [!DNL Analytics for Advertising] 宏 [!DNL Flashtalking] 广告标记
description: 了解添加原因和方法 [!DNL Analytics for Advertising] 宏 [!DNL Flashtalking] 广告标记
feature: Integration with Adobe Analytics
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---

# 附加 [!DNL Analytics for Advertising] 宏 [!DNL Flashtalking] 广告标记

*仅具有Adobe广告与Adobe Analytics集成的广告商*

*仅适用于Advertising DSP*

如果您使用 [!DNL Flashtalking] 对于您的Advertising DSP广告，将Analytics for Advertising参数附加到登陆页面URL。 参数记录 `s_kwcid` 和 `ef_id` 查询登陆页面URL中的字符串参数，允许Adobe广告将广告的点击数据发送到Adobe Analytics。

对使用宏 [!DNL Flashtalking] 以下类型的显示和视频广告 [!DNL Analytics for Advertising] 实施：

* **具有 [!DNL Adobe] [!DNL Analytics for Advertising] 在其网站上实施的JavaScript代码**:JavaScript代码已记录 `s_kwcid` 和 `ef_id` 查询字符串参数。 但是，当不支持第三方Cookie时，使用宏会扩展跟踪以包含基于点击的转化。 最佳做法是将以下部分中的宏添加到您的广告标记中，以捕获未通过JavaScript代码捕获的其他点进数据。

>[!NOTE]
>
>JavaScript代码是仅在Cookie仍然可用时用于点击跟踪的解决方案。 停止Cookie后，将需要实施以下宏。

* **网站不使用的广告商 [!DNL Analytics for Advertising] JavaScript代码，而是依赖 [!DNL Analytics] 仅用于点进数据的服务器端转发** （不含任何显示到达数据）：要报告由您通过Adobe广告购买的广告所驱动的网站点击活动，需要以下宏。

## 显示广告标记

在 [!DNL Flashtalking] 广告标记设置中，将以下宏附加到点进URL的末尾 `Clicktag` 字段：

```html
?[ftqs:[AdobeAMO]]
```

示例：  `https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

## 视频广告标记

在 [!DNL Flashtalking] 广告标记设置中，将以下宏附加到点进URL的末尾 `Clicktag` 字段：

```html
?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

示例：  `https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* [Adobe使用的广告ID [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [附加 [!DNL Analytics for Advertising] 宏 [!DNL Google Campaign Manager 360] 广告标记](/help/integrations/analytics/macros-google-campaign-manager.md)

