---
title: 连接的电视广告设置
description: 请参阅连接的电视广告的可用广告设置描述。
feature: DSP Ads
exl-id: 4daae9e4-27eb-4496-9186-f33aebd8daae
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 0%

---

# 连接的电视广告设置

## [!UICONTROL Insert Ad Tag]

*仅新广告*

**[!UICONTROL URL]**:VAST标记URL。

**[!UICONTROL Title]**:文件的名称，将在广告视图和报表中使用。

>[!TIP]
>
> 要检查VAST标记的有效性，请将其粘贴到浏览器中，然后点击 **[!UICONTROL Enter]** 键。 如果标记有效，您将看到一个包含 `<VAST>` 靠近顶部。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （只读）您创建的广告类型，与广告可附加到的版面类型相对应。

**[!UICONTROL Ad Name]:** 广告名称。 默认情况下，会使用资产标题，但您可以更改名称。

>[!TIP]
>
> 在 [!UICONTROL Ads] 视图和报表中。 例如，描述设备类型和一些关键属性(例如“假日产品预览”：30秒CTV”)。

**[!UICONTROL Width | Ad Unit Width]:** 整个广告单元的宽度。 此选项可能会被锁定，具体取决于您选择的广告单元类型。

**[!UICONTROL Height | Ad Unit Height]:** 整个广告单元的高度。 此选项可能会被锁定，具体取决于您选择的广告单元类型。

**[!UICONTROL Player X]:** 广告单元的X坐标。 保留默认设置。

**[!UICONTROL Player Y]:** 广告单元的Y坐标。 保留默认设置。

**[!UICONTROL Player Width]:** 整个广告单元的宽度。 此选项可能会被锁定，具体取决于您选择的广告单元类型。

这与 **[!UICONTROL Width]** 字段。

**[!UICONTROL Player Height]:** 整个广告单元的高度。 此选项可能会被锁定，具体取决于您选择的广告单元类型。

这与 **[!UICONTROL Height]** 字段。

**[!UICONTROL Show Controls]:** 广告的视频控件的包含位置： *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]*&#x200B;或 *[!UICONTROL None]* （默认）。

**[!UICONTROL Preserve Aspect Ratio]:** 是否保留视频的宽度和高度比例(*[!UICONTROL Yes]*)或拉伸视频以填充可用空间(*[!UICONTROL No]*)。

**[!UICONTROL VAST Tag]:** (仅使用VAST标记的广告；只读)作为广告源输入的第三方VAST标记。

**[!UICONTROL Final VAST Tag]:** (仅使用VAST标记的广告；只读)您作为广告源输入的第三方VAST标记，且 [Advertising DSP跟踪宏](/help/dsp/campaign-management/macros.md) 插入（如果适用）。

**[!UICONTROL Clock Number]**:(仅在英国使用；仅供具有权限的用户使用)用于确保广播正确广告的唯一标识符。 如果此设置不适用，请将其留空。

### [!UICONTROL Pixel]

用于放置的所有现有事件跟踪像素都会自动附加。 您可以根据您对单个广告的跟踪需求，分离现有像素并根据需要创建新像素。

以下设置适用于您创建或编辑的每个像素。

**[!UICONTROL Integration Event]:** 触发像素的事件。 对于此广告类型，请使用 *[!UICONTROL Impression]* 或 *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** 像素是否为 *[!UICONTROL IMG URL]* （1x1像素图像文件）， *[!UICONTROL HTML]*&#x200B;或 *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** 像素图像的URL，采用指定“像素类型”的相应格式。

**[!UICONTROL Pixel Name]:** 像素名称。 使用有助于您轻松识别像素的名称。

**[!UICONTROL Pixel Provider]:** 像素提供程序： *[!UICONTROL None]*, *[!UICONTROL Nielsen]*&#x200B;或 *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [关于广告管理](ad-about.md)
>* [创建单个广告](ad-create.md)
>* [列出与广告关联的版面](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [广告规范](ad-specs.md)
>* [DSP宏](/help/dsp/campaign-management/macros.md)

