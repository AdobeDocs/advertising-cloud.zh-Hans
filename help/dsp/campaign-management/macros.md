---
title: Advertising Cloud DSP宏
description: 引用可用的宏以进行常规跟踪和跟踪第三方显示广告的点击量。
feature: Ads
exl-id: e31cc2e5-ad1f-4555-a87b-0e4c3731fe5f
source-git-commit: 185fc7d79798a0a3a9ad5829b701aeb53a4a47c1
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Advertising Cloud DSP宏

宏是指令的短命令或简写，通常遵循格式`${MACRO_NAME}`。 Advertising Cloud DSP广告服务器在提供或单击广告时执行宏。

宏最常用于跟踪第三方和自定义创作代码或元数据（如第三方像素）。

## 常规跟踪宏

根据需要，在所有广告和标记类型中使用常规跟踪宏传递特定数据。

| 宏 | 描述 |
| --------------- | ---------------------- |
| `${USER_ID}` | 所有设备类型的用户标识符。 |
| `${TM_RANDOM}` | 卡舍巴斯特：1到1000000之间的随机数 |
| `${TM_PLACEMENT_ID_NUM}` | 版面ID |
| `${TM_SITE_URL_URLENC}` | 投标请求中传递的URL;URL编码 |
| `${TM_SITE_DOMAIN_URLENC}` | 从竞价请求中的URL解析的页面子域；URL编码 |

{style=&quot;table-layout:auto&quot;}

## 点击第三方显示广告的宏

要使用第三方显示标记准确跟踪广告的点击量，DSP需要显示点击宏。 只需要一个版本的宏；相关宏取决于标记类型。

| 宏 | 描述 |
| --------------- | ---------------------- |
| `${TM_CLICK_URL}` | 可让广告服务器在平台中跟踪和计数广告点击量的重定向URL |
| `${TM_CLICK_URL_URLENC}` | 重定向URL，该URL可启用需要URL编码的广告服务器，以便跟踪和计数平台中的广告点击量 |

{style=&quot;table-layout:auto&quot;}

DSP会在您执行以下操作时自动在显示标记中插入显示点击宏：

* 从Advertising Cloud广告服务器合作伙伴<!-- [Needs PM confirmation.] -->导出广告标记
* 直接在DSP中批量上传[!DNL Flashtalking]或[!DNL Google DoubleClick for Advertisers]广告标记

如果在构建显示广告时缺少点击宏，则DSP会显示一条警告消息，提示您在正确的标记区域中手动插入相应的显示点击宏。

>[!MORELIKETHIS]
>
>* [音频广告设置](/help/dsp/campaign-management/ads/ad-settings-audio.md)
>* [音频广告设置](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)
>* [音频广告设置](/help/dsp/campaign-management/ads/ad-settings-display.md)
>* [音频广告设置](/help/dsp/campaign-management/ads/ad-settings-mobile.md)
>* [音频广告设置](/help/dsp/campaign-management/ads/ad-settings-native.md)
>* [音频广告设置](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)

