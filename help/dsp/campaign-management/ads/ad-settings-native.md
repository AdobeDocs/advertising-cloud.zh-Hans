---
title: 本机显示广告设置
description: 请参阅对本机显示广告的可用广告设置的描述。
feature: DSP Ads
exl-id: 3ae59e63-ae64-41b2-8734-3df2da020c7c
source-git-commit: bcece4bfec6f8a765cced3ee230fd8cbf3055b7b
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---

# 本机显示广告设置

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （只读）您创建的广告类型，与广告可附加到的版面类型相对应。

**[!UICONTROL Ad Name]:** 广告名称。 默认使用广告类型，但您可以更改名称。

>[!TIP]
>
> 在 [!UICONTROL Ads] 视图和报表中。 For example, describe the unit type and some key attributes (such as Holiday Product Preview: 15sec Native”).

**[!UICONTROL Native Creative]:** 1200x627图像，可最大限度地提供移动设备库存。 单击 **[!UICONTROL Browse]** 并在您的设备或网络上找到文件，然后单击 **[!UICONTROL Upload]**.

**[!UICONTROL Title]:** An eye-catching title to engage viewers.

**[!UICONTROL Description]:** 广告的正文。 The maximum length is 100 characters.

**[!UICONTROL Landing Page]:** 查看者单击广告后登陆的URL。

**[!UICONTROL Final Landing Page]:** 的 [!UICONTROL Landing Page] 具有必需 [Advertising Cloud DSP跟踪宏](/help/dsp/campaign-management/macros.md) 插入（如果适用）。

**[!UICONTROL Sponsored By (Advertiser Name)]:** 广告的广告商。

**[!UICONTROL Call to Action]:** （可选）您希望查看者在看到此广告后执行的步骤。

**[!UICONTROL Advertiser Logo]:** （可选）要包含在广告中的1:1比率徽标，以获得更多品牌认可。 单击 **[!UICONTROL Browse]** 并在您的设备或网络上找到文件，然后单击 **[!UICONTROL Upload]**.

### [!UICONTROL Pixel]

All existing event tracking pixels for the placement are automatically attached. You can detach existing pixels and create new pixels as needed, based on your tracking needs for the individual ad.

The following settings apply to each pixel that you create or edit.

**[!UICONTROL Integration Event]:** The event that triggers the pixel to fire. 对于此广告类型，请使用 *[!UICONTROL Impression]* 或 *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** 像素是否为 *[!UICONTROL IMG URL]* （1x1像素图像文件）， *[!UICONTROL HTML]*&#x200B;或 *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** The URL of the pixel image, in the appropriate format for the specified [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** The pixel name. 使用有助于您轻松识别像素的名称。

**[!UICONTROL Pixel Provider]:** 像素提供程序： *[!UICONTROL None]*, *[!UICONTROL Nielsen]*&#x200B;或 *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [关于广告管理](ad-about.md)
>* [创建单个广告](ad-create.md)
>* [List the Placements Associated with an Ad](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [广告规范](ad-specs.md)
>* [Advertising Cloud DSP Macros](/help/dsp/campaign-management/macros.md)

