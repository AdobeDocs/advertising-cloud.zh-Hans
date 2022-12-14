---
title: Advertising Cloud DSP宏
description: 引用可用的宏以进行常规跟踪和跟踪第三方显示广告的点击量。
feature: DSP Ads
exl-id: e31cc2e5-ad1f-4555-a87b-0e4c3731fe5f
source-git-commit: b3fc18cf84713adcff5a4208db537b03904cfa08
workflow-type: tm+mt
source-wordcount: '935'
ht-degree: 0%

---

# Advertising Cloud DSP宏

宏是指令的短命令或简写，通常遵循格式 `${MACRO_NAME}`. 创意代码或点进URL中包含的宏会展开为广告服务器可以理解的较长代码字符串。 Advertising Cloud DSP广告服务器在提供或单击广告时执行宏。

广告服务器宏对于将重要信息传递到DSP或第三方广告服务器非常有用。 宏最常用于跟踪第三方和自定义创作代码或元数据（如第三方像素）。

您可以在任意位置手动插入宏，例如在VAST标记中、在任何URL中，或在DSP或第三方事件像素中。 但是，每个DSP客户端和合作伙伴都有不同的广告标记格式，因此应该将宏相应地插入标记的不同位置。 每次您与新客户或合作伙伴合作时，都会要求他们提供有关在其广告标记(用于DSP流量)中插入宏的位置的文档。

## 常规跟踪宏

根据需要，在所有广告和标记类型中使用常规跟踪宏传递特定数据。

| 宏 | 替换说明 | 类型 |
| ----- | ----------------------- | ---- |
| `${TM_ACCOUNT_ID}` | 帐户ID。 | 整数 |
| `${TM_AD_ID}` | 广告键(adKey)。 | 字符串 |
| `${TM_AD_ID_NUM}` | 广告ID。 | 整数 |
| `${TM_ADVERTISER_ID}` | 广告商ID。 | 整数 |
| `${TM_CAMPAIGN_ID}` | 促销活动键。 | 字符串 |
| `${TM_CAMPAIGN_ID_NUM}` | 营销活动ID。 | 整数 |
| ` ${TM_CLICK_URL}` | 重定向URL，它允许广告服务器跟踪和计数广告点击量。 当广告投放时，如果用户点击该广告，则会激活宏，并记录该点击并计数以用于报告目的。 | 字符串 |
| ` ${TM_CLICK_URL_URLENC}` | 编码的重定向URL，广告服务器可跟踪和计数广告点击量。 当广告投放时，如果用户点击该广告，则会激活宏，并记录该点击并计数以用于报告目的。 除非您要创建第三方广告，并且供应商需要URL编码，否则请勿使用此宏。 | 字符串 |
| `${TM_FEED_ID}` | 用于媒体投放的键(feedKey)。 | 字符串 |
| `${TM_FEED_ID_NUM}` | 媒体投放的ID。 | 整数 |
| ` ${TM_MACRO_PLACEMENT_SITE_KEY` | 用于版面的网站键。 必需 [!DNL AppsFlyer] 单击移动设备应用程序安装广告的跟踪器。<!-- should map to placement_site_key column of placement_site table --> | 字符串 |
| `${TM_PLACEMENT_ID}` | 放置键(cpKey)。 | 字符串 |
| `${TM_PLACEMENT_ID_NUM}` | 版面ID。 | 整数 |
| `${TM_RANDOM}` | 卡舍巴斯特：1到1000000之间的随机数。 | long |
| `${TM_SESSION_ID}` | 会话的ID，对应于广告标记的单次检索。 | 字符串 |
| `${TM_SITE_DOMAIN_URLENC}` | 从竞价请求中的URL解析的页面子域；URL编码。 横幅内点击播放广告不受支持。 | 字符串 |
| ` ${TM_SITE_NAME}` | 版面的网站名称。 | 字符串 |
| `${TM_SITE_URL_URLENC}` | 投标请求中传递的URL;URL编码。 横幅内点击播放广告不受支持。 | 字符串 |
| `${TM_SITE_ID_NUM}` | 版面的网站ID。 | 整数 |
| `${TM_TIMESTAMP}` | Unix时间戳，指示自1970年1月1日午夜（UTC时间）起经过的秒数。 | long |
| ` ${TM_VIDEO_DURATION}` | 广告视频的持续时间（以秒为单位）。 | 整数 |

{style=&quot;table-layout:auto&quot;}

<!-- Removed because not found in code base:
|` ${TM_MACRO_PROMOTED_AD_KEY}` | The promoted ad key for the placement. Required for [!DNL AppsFlyer] click trackers for mobile app install ads. | string |
 -->

## 特定于移动设备的宏

| 宏 | 替换说明 | 类型 |
| ----- | ----------------------- | ---- |
| `${CS_PLATFORM_ID}` | ([!DNL ComScore])平台ID，对应于设备的操作系统：<ul><li>`ios` = [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>`other` 当平台不是上述任何一个时</li></ul> | varchar(50) |
| `${CS_DEVICE_MODEL}` | ([!DNL ComScore])设备型号名称，URL编码。 | 字符串 |
| `${CS_IMPLEMENTATION_TYPE}` | ([!DNL ComScore])投放广告的环境：<ul><li>`a` =移动应用程序</li><li>`b` =移动网站</li></ul> | 字符串(`a` 或 `b`) |
| `${NS_PLATFORM_ID}` | ([!DNL Nielsen])平台ID，对应于设备的操作系统：<ul><li>`ios`= [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>`other` 当平台不是上述任何一个时</li></ul> | 字符串 |
| `${NS_DEVICE_GROUPING}` | ([!DNL Nielsen])广告所在的设备类型：<ul><li>`TAB` =平板电脑</li><li>`PHN` = mobile</li><li>`computer` =计算机</li></ul> | 字符串 |
| `${UOO}` | ([!DNL Nielsen])用户是否已选择退出广告跟踪：<ul><li>`1` （DNT标记= 1）=用户已选择退出广告跟踪</li><li>`0` （DNT标记= 0）=用户已选择加入广告跟踪</li></ul> | 整数(`0` 或 `1`) |
| `${TM_BUNDLE}` | 的 [!DNL iOS] 或 [!DNL Android] 应用商店包ID。 示例：com.zynga.wwf2.free或id804379658 | 字符串 |
| `gdpr=${GDPR_ENFORCED}&gdpr_consent=${GDPR_CONSENT}` | `gdpr=${GDPR_ENFORCED}` 指示投标人是否确定竞价请求来自欧盟来源并需要执行GDPR:<ul><li>`1` =应强制执行GDPR</li><li>`0` =不应强制执行GDPR</li></ul>`gdpr_consent=${GDPR_CONSENT}` 是从供应合作伙伴在入站竞价请求中传递的同意值：<ul><li>在大多数情况下，这是基于64url编码的同意字符串，或daisybit(例如：BN5lERiOMYEdiAKAWXEND1HoSBE6CAFAApAMgBkIDIgM0AgOJxAnQA)</li><li>`0` =未同意</li><li>`1` =同意</li></ul> | daisybit或整数 |

{style=&quot;table-layout:auto&quot;}

## 点击第三方显示广告的宏

要使用第三方显示标记准确跟踪广告的点击量，DSP需要显示点击宏。 只需要一个版本的宏；相关宏取决于标记类型。

| 宏 | 替换说明 | 类型 |
| ----- | ----------------------- | ---- |
| `${TM_CLICK_URL}` | 允许广告服务器跟踪和计数平台中广告点击量的重定向URL。 | 字符串 |
| `${TM_CLICK_URL_URLENC}` | 重定向URL，用于启用需要URL编码的广告服务器以跟踪和计数平台中的广告点击量。 | 字符串 |

{style=&quot;table-layout:auto&quot;}

当您执行以下操作时，DSP会自动将显示点击宏插入第三方显示标记中：

* 从Advertising Cloud广告服务器合作伙伴导出广告标记 <!-- [Needs PM confirmation.] -->
* 批量上传 [!DNL Flashtalking] 或 [!DNL Google DoubleClick for Advertisers] 直接在DSP中添加标记

如果在构建显示广告时缺少点击宏，则DSP会显示一条警告消息，提示您在正确的标记区域中手动插入相应的显示点击宏。

## 宏错误疑难解答

在向代码中添加宏时，请确保使用宏的确切语法。 验证宏时， DSP会检查该宏是否与其中一个有效宏完全匹配。

如果宏名称的开头或结尾缺少字符，则会生成错误。 例如，在以下情况下，您将看到一条错误消息：

* 您会在宏名称的开头忘记一个或多个字符，例如 `${`. 如果不包含完整语法，则该条目将不被识别为有效的宏。
* 宏不以一组有效的字符结尾，例如 `}`.

>[!MORELIKETHIS]
>
>* [音频广告设置](/help/dsp/campaign-management/ads/ad-settings-audio.md)
>* [连接的电视广告设置](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)
>* [显示广告设置](/help/dsp/campaign-management/ads/ad-settings-display.md)
>* [移动设备广告设置](/help/dsp/campaign-management/ads/ad-settings-mobile.md)
>* [本机广告设置](/help/dsp/campaign-management/ads/ad-settings-native.md)
>* [前置广告设置](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)
>* [通用视频广告设置](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)

