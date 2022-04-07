---
title: 关于Advertising Cloud DSP中的广告管理
description: 了解广告管理。
feature: DSP Ads
exl-id: 72c8bbef-d09c-4cf4-994d-99578d043d39
source-git-commit: ff0e153344f8245ff217cc8b2b276184dd7422b5
workflow-type: tm+mt
source-wordcount: '664'
ht-degree: 0%

---

# 关于Advertising Cloud DSP中的广告管理

<!-- add "The Ads View (Dashboard?)" section -->

Advertising Cloud DSP支持通过第三方广告服务标记(如Google、Flashtalking或Sizmek)来交付各种广告类型的广告，以及通过本机显示广告的直接资产上传。 您可以单独或批量上传第三方标记。 批量上载使用合作伙伴标签表或批量标记模板。

<!-- The bulk upload feature requires you to either a) upload DoubleClick and Flashtalking tag sheets or b) download a template, input your tags into the template, and then re-upload the template. -->
<!-- need a list of all supported third-party ad servers; see file in future-tbd folder -->

设置广告后，您需要将每个广告附加到版面，其中包括将控制营销活动投放方式的定位参数（如地域、受众、设备和库存定位）。 您可以将单个广告附加到一个或多个版面。

## 可用广告类型 {#ad-types}

以下所有广告类型在Advertising Cloud DSP中均可用。 有关每种广告类型的完整规范，请参阅 [广告规范](/help/dsp/assets/ad-specs.pdf).

* **音频广告（仅限第三方）**:音频广告在数字出版商网站上的内容之间播放，并且可以作为音频文件或与伴随横幅一起独立运行。 音频最适用于提高品牌知名度和吸引现成受众。 音频的关键绩效指标包括 [!UICONTROL Completion Rate] 和 [!UICONTROL Cost per Completion].

* **显示广告（仅限第三方）**:显示广告是在Web浏览器或应用程序中显示的动画或静态图像。 单击广告单元可将用户转到品牌网站或微型网站。 显示功能最适合促进高效CPM、增加消息关联、添加其他品牌或产品接触点，以及推动用户向下访问购买漏斗。 用于显示的关键绩效指标包括 [!UICONTROL Clicks], [!UICONTROL Cost per Click], [!UICONTROL Conversions]和 [!UICONTROL Cost per Conversion]. DSP支持多种显示横幅广告大小。

* **Mobile Ads（仅限第三方）**:Mobile广告可以采用前置视频(VAST、MRAID)或标准显示格式。 Mobile前置视频可以自动播放或点击播放，最适合用于跨屏幕吸引查看者。 Mobile标准显示屏是在移动Web浏览器或应用程序中显示的静态图像，最适合用于补充数字视频购买、促进消息关联，以及添加其他品牌或产品接触点。 Mobile广告还可以用作全屏收购或移动插播式广告，这些广告是全屏、高影响力的移动广告，最适合用于提高移动受众的品牌知名度并促进转化。

* **本机显示广告（仅限第一方）**:标准显示格式支持本机广告。 本机广告包括标题和/或标题、描述、徽标和图像。 广告元素经过组合和渲染以与发布者的页面样式相匹配，以便广告与发布者的有机内容融合在一起，从而提高参与度。 Native最适用于提高品牌知名度，以及通过有利于查看者的广告提高受众查看率和参与率。 主要业绩指标包括 [!UICONTROL Clicks], [!UICONTROL Cost Per Click], [!UICONTROL Conversions]和 [!UICONTROL Cost Per Conversion].

* **前置广告（仅限第三方）**:前置广告（VAST和VPAID）在优质视频内容之前显示，并提供沉浸式、引人入胜的观看体验。 前置视频可以是交互式的，包含富媒体功能，并且包含叠加图、滚动播放和行动动员。 前置视频广告的关键绩效指标包括 [!UICONTROL Video Completion Rate] 和 [!UICONTROL Viewability Rate].

* **连接的电视广告（仅限第三方）**:连接的电视广告在优质电视视频内容之前和期间显示。 所有连接的电视清单都在电视设备上运行，这意味着视频在观看者无法跳过的精益全屏环境中自动播放。 “连接的电视”是最接近电视广告的数字视频格式。 连接电视的关键绩效指标包括 [!UICONTROL Completion Rate].

## Advertising Cloud DSP广告批准

创建广告时，Advertising Cloud DSP会针对敏感类别对其进行审核，单击URL功能并预览渲染。

最初，您会在 [!UICONTROL Status] 列。 审核过程通常需要24-48小时。 但是，损坏的广告可能具有超过48小时的待决状态，因此您有时间在广告被拒绝之前修复错误。 被拒绝的广告包括拒绝的原因。

当DSP批准广告时，“状态”列中将显示一个绿色圆点。

![批准指示器 [!UICONTROL Status] 列](/help/dsp/assets/ad-approval-status.png)

>[!NOTE]
>
>仅当DSP和SSP都批准了创作元素时，才会提供您的广告。 每个SSP都有自己的批准要求和流程。

>[!MORELIKETHIS]
>
>* [创建单个广告](ad-create.md)
>* [创建多个第三方广告](ad-create-multiple.md)
>* [广告规范](/help/dsp/assets/ad-specs.pdf)

