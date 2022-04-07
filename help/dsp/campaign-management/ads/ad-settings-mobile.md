---
title: Mobile广告设置
description: 请参阅移动广告的可用广告设置描述。
feature: DSP Ads
exl-id: f67c4ba0-1011-4ad6-bd36-98c312b81b67
source-git-commit: 68af6b1846a37689dce0ca13a05cc1611b1f35a9
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 0%

---

# Mobile广告设置

## [!UICONTROL Insert Ad Tag]

*仅新增移动视频广告格式*

**[!UICONTROL URL]** 或 **[!UICONTROL Ad Tag]**:包含创意资产和跟踪像素的第三方VAST广告标记或广告标记

**[!UICONTROL Ad Title]** 或 **[!UICONTROL Title]**:在 [!UICONTROL Ads] 查看和报表。

>[!TIP]
>
> 要检查VAST标记的有效性，请将其粘贴到浏览器中，然后点击 **[!UICONTROL Enter]** 键。 如果标记有效，您将看到一个包含 `<VAST>` 靠近顶部。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]:Mobile展示广告

**[!UICONTROL Ad Type]:** （只读）您创建的广告类型，与广告可附加到的版面类型相对应。

**[!UICONTROL Ad Name]:** 广告名称。 默认情况下，会使用资产标题，但您可以更改名称。

>[!TIP]
>
> 在将广告附加到版面、广告视图和报表中时，使用易于查找的名称。 例如，描述设备类型和一些关键属性(例如“假日产品预览”：300x250游戏机”)。

**\[广告源\]**:（只读） *[!UICONTROL 3rd party]*.

**[!UICONTROL Display Code]:** 第三方创意资产的URL。 任意 [timestamp] 和[[timestamp]]参数将被实际值替换。

**[!UICONTROL Final Display Code]:** 第三方创意资产的URL，必需 [Advertising Cloud DSP跟踪宏](/help/dsp/campaign-management/macros.md) 插入（如果适用）。

### [!UICONTROL Basic]:视频广告

**[!UICONTROL Ad Type]:** （只读）您创建的广告类型，与广告可附加到的版面类型相对应。

**[!UICONTROL Ad Name]:** 广告名称。 默认情况下，会使用资产标题，但您可以更改名称。

>[!TIP]
>
> 在将广告附加到版面、广告视图和报表中时，使用易于查找的名称。 例如，描述设备类型和一些关键属性(例如“假日产品预览”：30秒电话前置”)。

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]:** 整个广告单元的宽度。 此选项可能会被锁定，具体取决于您选择的广告单元类型。

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]:** 整个广告单元的高度。 此选项可能会被锁定，具体取决于您选择的广告单元类型。

**[!UICONTROL Player X]:** 广告单元的X坐标。 保留默认设置。

**[!UICONTROL Player Y]:** 广告单元的Y坐标。 保留默认设置。

**[!UICONTROL Player Width]:** 整个广告单元的宽度。 此选项可能会被锁定，具体取决于您选择的广告单元类型。

这与 **[!UICONTROL Width]** 字段。

**[!UICONTROL Player Height]:** 整个广告单元的高度。 此选项可能会被锁定，具体取决于您选择的广告单元类型。

这与 **[!UICONTROL Height]** 字段。

**[!UICONTROL Show Controls]:** 广告的视频控件的包含位置： *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]*&#x200B;或 *[!UICONTROL None]* （默认）。

**[!UICONTROL Preserve Aspect Ratio]:** 是否保留视频的宽度和高度比例(*[!UICONTROL Yes]*)或拉伸视频以填充可用空间(*[!UICONTROL No]*)。

**[!UICONTROL Close Button Delay]:** （某些广告类型）关闭按钮外观延迟的秒数。

**[!UICONTROL VAST Tag]:** (仅使用VAST标记的广告；只读)作为创意资产输入的第三方VAST标记。

**[!UICONTROL Final VAST Tag]:** (仅使用VAST标记的广告；只读)您输入的第三方VAST标记作为创意资产，且必要 [Advertising Cloud DSP跟踪宏](/help/dsp/campaign-management/macros.md) 插入（如果适用）。

**[!UICONTROL Wmode]:** （某些广告类型）窗口模式： *[!UICONTROL window]*, *[!UICONTROL transparent]*&#x200B;或 *[!UICONTROL opaque]*.

### [!UICONTROL Pixel]

用于放置的所有现有事件跟踪像素都会自动附加。 您可以根据您对单个广告的跟踪需求，分离现有像素并根据需要创建新像素。

以下设置适用于您创建或编辑的每个像素。

**[!UICONTROL Integration Event]:** 触发像素的事件。 对于此广告类型，请使用 *[!UICONTROL Impression]* 或 *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** 像素是否为 *[!UICONTROL IMG URL]* （1x1像素图像文件）， *[!UICONTROL HTML]*&#x200B;或 *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** 像素图像的URL，格式与指定的 [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** 像素名称。 使用有助于您轻松识别像素的名称。

**[!UICONTROL Pixel Provider]:** 像素提供程序： *[!UICONTROL None]*, *[!UICONTROL Nielsen]*&#x200B;或 *[!UICONTROL Comscore]*.

### [!UICONTROL Sharing]

已弃用

>[!MORELIKETHIS]
>
>* [关于广告管理](ad-about.md)
>* [创建单个广告](ad-create.md)
>* [列出与广告关联的版面](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [广告规范](/help/dsp/assets/ad-specs.pdf)
>* [Advertising Cloud DSP宏](/help/dsp/campaign-management/macros.md)

