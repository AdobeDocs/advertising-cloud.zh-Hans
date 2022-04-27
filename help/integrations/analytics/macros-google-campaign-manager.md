---
title: 附加 [!DNL Analytics for Advertising Cloud] 宏 [!DNL Google Campaign Manager 360] 广告标记
description: 了解添加原因和方法 [!DNL Analytics for Advertising Cloud] 宏 [!DNL Google Campaign Manager 360] 广告标记
feature: Integration with Adobe Analytics
source-git-commit: 2dfb609e73902fcd929d96c55fbc79588074c65e
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 0%

---

# 附加 [!DNL Analytics for Advertising Cloud] 宏 [!DNL Google Campaign Manager 360] 广告标记

*仅具有Advertising Cloud-Adobe Analytics集成的广告商*

*仅适用于Advertising Cloud DSP*

如果您使用 [!DNL Google Campaign Manager 360] 对于您的Advertising Cloud DSP广告，请使用 [`%p` 宏](https://support.google.com/campaignmanager/table/6096962). 参数记录 `s_kwcid` 和 `ef_id` 查询登陆页面URL中的字符串参数，允许Advertising Cloud将广告的点击数据发送到Adobe Analytics。

对使用宏 [!DNL Campaign Manager 360] 以下类型的显示和视频广告 [!DNL Analytics for Advertising Cloud] 实施：

* **具有 [!DNL Adobe] [!DNL Analytics for Advertising Cloud] 在其网站上实施的JavaScript代码**:JavaScript代码已记录 `s_kwcid` 和 `ef_id` 查询字符串参数。 但是，当不支持第三方Cookie时，使用宏会扩展跟踪以包含基于点击的转化。 最佳做法是将以下部分中的宏添加到您的广告标记中，以捕获未通过JavaScript代码捕获的其他点进数据。

>[!NOTE]
>
>JavaScript代码是仅在Cookie仍然可用时用于点击跟踪的解决方案。 停止Cookie后，将需要实施以下宏。

* **网站不使用的广告商 [!DNL Analytics for Advertising Cloud] JavaScript代码，而是依赖 [!DNL Analytics] 仅用于点进数据的服务器端转发** （不含任何显示到达数据）：要报告通过Advertising Cloud购买的广告所驱动的上门点击活动，需要以下宏。

## 将宏附加到 [!DNL Google Campaign Manager 360] 广告

在 [!DNL Google Campaign Manager 360]，将以下参数附加到登陆页面URL中每个显示广告和视频广告的： `%pamo=!;`

您可以通过多种方式指定登陆页面URL。 以下子部分中包含每个选项的说明。

以下是带后缀的登陆页面URL的示例。

```
https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;
```

>[!NOTE]
>
>
>* 如果登陆页面URL包含不常见的井号(#)，请将 `amo` 参数。
>* 如果在 `amo` 参数，然后在其后添加参数（例如&amp;a=b）。 示例：`https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;&a=b#login`


### 配置广告商级别的登陆页面URL后缀

1. 在主菜单中，单击 [!UICONTROL Advertisers] 选项卡。
1. 单击广告商名称。
1. 在 [!UICONTROL Landing page URL suffix] 设置，包括 `%pamo!;` 在 [!UICONTROL URL suffix] 字段。

![广告商级别设置](/help/integrations/assets/macro-ggl360-advertiser.png)

### 配置营销活动级别的登陆页面URL后缀

1. 在主菜单中，单击 [!UICONTROL Campaigns] 选项卡。
1. 单击营销活动名称。
1. 单击 [!UICONTROL Properties].
1. 在 [!UICONTROL Landing page URL suffix] 设置，包括 `%pamo!;` 在 [!UICONTROL URL suffix] 字段。

![营销活动级别设置](/help/integrations/assets/macro-ggl360-campaign.png)

### 配置创意级别的登陆页面URL后缀

1. 在主菜单中，单击 [!UICONTROL Campaigns] 选项卡。
1. 单击营销活动名称。
1. 在 [!UICONTROL Views] 菜单，选择 [!UICONTROL Creatives].
1. 单击创作名称。
1. 在 [!UICONTROL Click tags] 设置，包含 `%pamo!;` 在 [!UICONTROL Landing page] 列。

![创意级别设置](/help/integrations/assets/macro-ggl360-creative.png)

## 如何 [!DNL Analytics for Advertising Cloud] 宏在DSP中扩展

在DSP中，当您创建的广告包含 [!DNL Analytics for Advertising Cloud] 参数(`amo`)、 `ef_id` 和 `s_kwcid` 宏会自动附加到点击URL中。 最佳实践是在DSP中检查标记，以确保 `ef_id` 和 `s_kwcid` 宏存在。

以下是 [!DNL Google Campaign Manager 360] [ins标记](https://support.google.com/campaignmanager/answer/6080468) 与在DSP中显示时一样。

```
<ins class='dcmads' style='display:inline-block;width:160px;height:600px'
data-dcm-placement='N6482.2155306TUBEMOGUL/B23486129.261313631'
data-dcm-rendering-mode='iframe'
data-dcm-https-only
data-dcm-resettable-device-id=''
data-dcm-app-id='' data-dcm-click-tracker='${TM_CLICK_URL}'
data-dcm-param-amo='ef_id=${TM_USER_ID}:${TM_DATETIME}:d&s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}'>
<script src='https://www.googletagservices.com/dcm/dcmads.js'></script>
</ins>
```

当用户点击广告时， [!DNL Google Campaign Manager 360] sees `%pamo` 后缀中，并动态插入 `amo` 参数添加到URL中。


>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Advertising Cloud ID使用者 [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [附加 [!DNL Analytics for Advertising Cloud] 宏 [!DNL Flashtalking] 广告标记](macros-flashtalking.md)

