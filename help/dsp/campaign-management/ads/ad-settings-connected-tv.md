---
title: 连接的电视广告设置
description: 请参阅连接的电视广告的可用广告设置描述。
feature: DSP Ads
exl-id: 4daae9e4-27eb-4496-9186-f33aebd8daae
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 0%

---

# 连接的电视广告设置

## [!UICONTROL Upload or Select Creative]

*仅新广告*

**[!UICONTROL Upload Audio]:** 将原始资产上传到DSP。选择此选项时，请执行以下操作：

1. 单击&#x200B;**[!UICONTROL Choose File]**&#x200B;并在设备或网络上找到文件。
1. 输入文件标题，该标题将在[!UICONTROL Ads]视图和报告中使用。
1. 单击 **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Audio]:** 在帐户中以正确的格式选择任何之前上传的创作元素。

**[!UICONTROL Advanced: VAST Tag URL]:** （某些广告类型）要输入包含创意资产和跟踪像素的第三方VAST标记，请执行以下操作：

1. 单击![](/help/dsp/assets/compressed.png)旁边的箭头。**[!UICONTROL Advanced: VAST Tag URL]**
1. 在&#x200B;**[!UICONTROL URL]**&#x200B;字段中，输入VAST标记URL。
1. 为文件输入&#x200B;**[!UICONTROL Title]**，该文件将用在“广告”视图和报表中。

>[!TIP]
>
> 要检查VAST标记的有效性，请将其粘贴到浏览器中，然后点击&#x200B;**[!UICONTROL Enter]**&#x200B;键。 如果标记有效，您将在顶部附近看到一个包含`<VAST>`的XML文件。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （只读）您创建的广告类型，与广告可附加到的版面类型相对应。

**[!UICONTROL Ad Name]:** 广告名称。默认情况下，会使用资产标题，但您可以更改名称。

>[!TIP]
>
> 在[!UICONTROL Ads]视图和报表中，使用在将广告附加到版面时容易找到的名称。 例如，描述设备类型和一些关键属性(例如“假日产品预览”：30秒CTV”)。

**[!UICONTROL Width | Ad Unit Width]:** 整个广告单元的宽度。此选项可能会被锁定，具体取决于您选择的广告单元类型。

**[!UICONTROL Height | Ad Unit Height]:** 整个广告单元的高度。此选项可能会被锁定，具体取决于您选择的广告单元类型。

**[!UICONTROL Player X]:** 广告单元的X坐标。保留默认设置。

**[!UICONTROL Player Y]:** 广告单元的Y坐标。保留默认设置。

**[!UICONTROL Player Width]:** 整个广告单元的宽度。此选项可能会被锁定，具体取决于您选择的广告单元类型。

与&#x200B;**[!UICONTROL Width]**&#x200B;字段相同。

**[!UICONTROL Player Height]:** 整个广告单元的高度。此选项可能会被锁定，具体取决于您选择的广告单元类型。

与&#x200B;**[!UICONTROL Height]**&#x200B;字段相同。

**[!UICONTROL Show Controls]:** 广告的视频控件应包含的位置： *[!UICONTROL Under]*、  *[!UICONTROL Over]*、 *[!UICONTROL Bottom]*&#x200B;或( *[!UICONTROL None]* 默认)。

**[!UICONTROL Preserve Aspect Ratio]:** 是保留视频的宽度和高度比例(*[!UICONTROL Yes]*)，还是拉伸视频以填充可用空间(*[!UICONTROL No]*)。

**[!UICONTROL Click URL]:** (仅限Adobe投放的广告)查看者单击广告后将登陆的URL。

**[!UICONTROL Final Click URL]:** (仅Adobe投放的广告；只读)具有必 [!UICONTROL Click URL] 要的Advertising Cloud DSP [跟踪](/help/dsp/campaign-management/macros.md) 宏（如果适用）。

**[!UICONTROL VAST Tag]:** (仅使用VAST标记的广告；只读)作为广告源输入的第三方VAST标记。

**[!UICONTROL Final VAST Tag]:** (仅使用VAST标记的广告；只读)您作为广告源输入的第三方VAST标记，且必要的Advertising Cloud DSP跟 [踪宏(](/help/dsp/campaign-management/macros.md) 如果适用)。

**[!UICONTROL Clock Number]**:(仅在英国使用；仅供具有权限的用户使用)用于确保广播正确广告的唯一标识符。如果此设置不适用，请将其留空。

### [!UICONTROL Pixel]

用于放置的所有现有事件跟踪像素都会自动附加。 您可以根据跟踪需求分离现有像素并根据需要创建新像素。

以下设置适用于您创建或编辑的每个像素。

**[!UICONTROL Integration Event]:** 触发像素的事件。对于此广告类型，请使用在&#x200B;*[!UICONTROL Impression]*&#x200B;或&#x200B;*[!UICONTROL Click-through]*&#x200B;上触发的像素。

**[!UICONTROL Pixel Type]:** 像素是(1x1 *[!UICONTROL IMG URL]* 像素图像文件)、 *[!UICONTROL HTML]*&#x200B;还是 *[!UICONTROL JavaScript URL]*。

**[!UICONTROL Pixel URL or Code]:** 像素图像的URL，采用指定“像素类型”的相应格式。

**[!UICONTROL Pixel Name]:** 像素名称。使用有助于您轻松识别像素的名称。

**[!UICONTROL Pixel Provider]:** 像素提供程序： *[!UICONTROL None]*、  *[!UICONTROL Nielsen]*&#x200B;或 *[!UICONTROL Comscore]*。

>[!MORELIKETHIS]
>
>* [关于广告管理](ad-about.md)
>* [创建广告](ad-create.md)
>* [列出与广告关联的版面](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [可用广告类型](ad-types.md)
>* [广告规范](/help/dsp/assets/ad-specs.pdf)
>* [Advertising Cloud DSP宏](/help/dsp/campaign-management/macros.md)

