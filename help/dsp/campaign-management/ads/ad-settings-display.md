---
title: 显示广告设置
description: 请参阅展示广告的可用广告设置的描述。
feature: DSP Ads
exl-id: ae88dfab-0b0c-42ab-9135-422b20a4b6cd
source-git-commit: bcece4bfec6f8a765cced3ee230fd8cbf3055b7b
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 0%

---

# 显示广告设置

以下设置适用于标准显示广告。

## [!UICONTROL Ad Options]

### 基本

**[!UICONTROL Ad Type]:** (Read-only) The ad type you&#39;re creating, which corresponds to the placement type to which the ad can be attached. 默认为 *[!UICONTROL Display]*.

**[!UICONTROL Ad Name]:** 广告名称。 默认情况下，会使用资产标题，但您可以更改名称。

>[!TIP]
>
> Use a name that will be easy to find when you attach the ad to a placement, in the [!UICONTROL Ads] view, and in reports. For example, describe the unit type and some key attributes (such as Holiday Product Preview: 300x250 Gamer”).

**\[广告源\]**:（只读） *[!UICONTROL 3rd party]*.

**[!UICONTROL This is an expandable Banner]:** (Third-party ads only) Indicates the ad is an expandable banner ad. 相关的扩展设置可确定要购买的库存，因此请确保它们反映广告行为。

**[!UICONTROL Expansion Method]:** （仅限第三方可扩展的横幅广告）横幅是否在 *[!UICONTROL Click]* 或 *[!UICONTROL Rollover]*.

**[!UICONTROL Expansion Directions]:** （仅限第三方可扩展的横幅广告）广告展开的方向： *[!UICONTROL Up]*, *[!UICONTROL Down]*, *[!UICONTROL Left]*&#x200B;或 *[!UICONTROL Right]*.

**[!UICONTROL Certified Vendors]:** （仅限第三方可扩展横幅广告）广告可用的认证供应商： *[!UICONTROL DCM]* ([!DNL Google DoubleClick for Advertisers])、 *[!UICONTROL Flashtalking]*, *[!UICONTROL Sizmek]*&#x200B;或 *[!UICONTROL Jivox]*.

**[!UICONTROL Display Code]:** （仅限第三方广告）第三方创意资产的URL。 Any [timestamp] and [[timestamp]] parameters will be replaced with actual values.

**[!UICONTROL Final Display Code]:** （仅限第三方广告）第三方创意资产的URL，并且必要 [Advertising Cloud DSP跟踪宏](/help/dsp/campaign-management/macros.md) 插入（如果适用）。

**[!UICONTROL Ad Size]:** The width and height of the ad. It must be a [supported standard display ad size](ad-specs.md). 您可以在上传广告之前手动输入广告大小或输入 [!UICONTROL Display Code]. 如果不输入广告大小，则上载的广告或广告标记的维度将自动输入为只读。 请注意，如果维度不在标准显示中，则不会保存显示广告，例如301x250，而不是300x250广告大小。

>[!IMPORTANT]
>
> 在宽度和高度字段中声明的广告大小将与传入的竞价请求匹配。 如果广告的维度与声明的广告大小不匹配，则可能会遇到投放问题。

### [!UICONTROL Pixel]

用于放置的所有现有事件跟踪像素都会自动附加。 You can detach existing pixels and create new pixels as needed, based on your tracking needs for the individual ad.

以下设置适用于您创建或编辑的每个像素。

**[!UICONTROL Integration Event]:** 触发像素的事件。 对于此广告类型，请使用 *[!UICONTROL Impression]* 或 *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** 像素是否为 *[!UICONTROL IMG URL]* （1x1像素图像文件）， *[!UICONTROL HTML]*&#x200B;或 *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** The URL of the pixel image, in the appropriate format for the specified [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** 像素名称。 使用有助于您轻松识别像素的名称。

**[!UICONTROL Pixel Provider]:** 像素提供程序： *[!UICONTROL None]*, *[!UICONTROL Nielsen]*&#x200B;或 *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [About Ad Management](ad-about.md)
>* [创建单个广告](ad-create.md)
>* [列出与广告关联的版面](ad-list-placements.md)
>* [广告规范](ad-specs.md)
>* [Advertising Cloud DSP宏](/help/dsp/campaign-management/macros.md)

