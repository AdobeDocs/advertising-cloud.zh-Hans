---
title: 通用视频广告设置
description: 请参阅通用视频广告的可用广告设置描述。
feature: DSP Ads
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 0%

---

# 通用视频广告设置

*开放测试版功能*

## [!UICONTROL Insert Ad Tag]

*仅新广告*

**[!UICONTROL URL]:** VAST标记URL。

**[!UICONTROL Title]:** 文件的标题，位于 [!UICONTROL Ads] 查看和报表。

>[!TIP]
>
> 要检查VAST标记的有效性，请将其粘贴到浏览器中，然后点击 **[!UICONTROL Enter]** 键。 如果标记有效，您将看到一个XML文件，其中包含 `<VAST>` 靠近顶部。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （只读）您创建的广告类型，与广告可附加到的版面类型相对应。

**[!UICONTROL Ad Name]:** 广告名称。 默认情况下，会使用资产标题，但您可以更改名称。

>[!TIP]
>
> 在 [!UICONTROL Ads] 视图和报表中。 例如，描述设备类型和一些关键属性(例如“假日产品预览”：30秒通用视频”)。

**[!UICONTROL Show Controls]:** 广告的视频控件的包含位置： *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]*&#x200B;或 *[!UICONTROL None]* （默认）。

**[!UICONTROL Preserve Aspect Ratio]:** 是否保留视频的宽度和高度比例(*[!UICONTROL Yes]*)或拉伸视频以填充可用空间(*[!UICONTROL No]*)。

**[!UICONTROL VAST Tag]:** (仅使用VAST标记的广告；只读)作为广告源输入的第三方VAST标记。

**[!UICONTROL Final VAST Tag]:** (仅使用VAST标记的广告；只读)您作为广告源输入的第三方VAST标记，且 [Advertising DSP跟踪宏](/help/dsp/campaign-management/macros.md) 插入（如果适用）。

**[!UICONTROL Wmode]:** 窗口模式： *[!UICONTROL window]*, *[!UICONTROL transparent]*&#x200B;或 *[!UICONTROL opaque]*. 如果此设置不适用，请将其留空。

**[!UICONTROL Video Format]:** 潜在清单的广告播放器的格式： *[!UICONTROL VPAID]*, *[!UICONTROL VPAID & VAST]*&#x200B;或 *[!UICONTROL VAST]*. 可视性始终以 [!UICONTROL VPAID]，但 [!UICONTROL VPAID & VAST] 包括不允许可视性测量的库存。 如果可见性量度对您的营销活动很重要，请考虑这一区别。

使用 *[!UICONTROL VAST]*，当您定位的连接电视或清单仅严格要求使用VAST格式时(通常来自诸如Google Ad Manager、Appnexus、SpotX和Freewheel之类的供应源)，则不允许进行可视性测量。

**[!UICONTROL Clock Number]**:(仅在英国使用；仅供具有权限的用户使用)用于确保广播正确广告的唯一标识符。 如果此设置不适用，请将其留空。

### [!UICONTROL Pixel]

用于放置的所有现有事件跟踪像素都会自动附加。 您可以根据您对单个广告的跟踪需求，分离现有像素并根据需要创建新像素。

以下设置适用于您创建或编辑的每个像素。

**[!UICONTROL Integration Event]:** 触发像素的事件。 对于此广告类型，请使用 *[!UICONTROL Impression]* 或 *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** 像素是否为 *[!UICONTROL IMG URL]* （1x1像素图像文件）， *[!UICONTROL HTML]*&#x200B;或 *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** 像素图像的URL，格式与指定的 [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** 像素名称。 使用有助于您轻松识别像素的名称。

**[!UICONTROL Pixel Provider]:** 像素提供程序： *[!UICONTROL None]*, *[!UICONTROL Nielsen]*&#x200B;或 *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [关于广告管理](ad-about.md)
>* [创建单个广告](ad-create.md)
>* [列出与广告关联的版面](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [广告规范](ad-specs.md)
>* [DSP宏](/help/dsp/campaign-management/macros.md)

