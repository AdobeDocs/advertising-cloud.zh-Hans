---
title: 移动设备广告设置
description: 请参阅移动广告的可用广告设置描述。
feature: DSP Ads
exl-id: f67c4ba0-1011-4ad6-bd36-98c312b81b67
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '1335'
ht-degree: 0%

---

# 移动设备广告设置

## [!UICONTROL Upload or Select Creative]

*仅新增移动视频广告格式*

**[!UICONTROL Vertical video]:** (选择时不 [!UICONTROL Custom Transcode] 可用)指示视频为垂直（纵向模式）。

**[!UICONTROL Transcode to]:** (某些用户，具体取决于权限；（可选）当发布者具有特定的创作文件要求时，要包含在VAST标记中的格式。默认情况下，会选择大多数发布者接受的格式。

**[!UICONTROL Custom Transcode]:** (仅测试版用户；选择“垂直视频”时不可用))表示视频使用自定义转码。如果选择此选项，则最多为三个自定义转码版本指定文件格式、视频比特率、缩放和维度。

**[!UICONTROL XTrader]:** （某些用户，取决于权限）指示视频使用一个或多个 [!DNL X_TRADER] 信息源。

**[!UICONTROL Upload Video]:** 将原始资产上传到DSP。选择此选项时，请执行以下操作：

1. 单击&#x200B;**[!UICONTROL Choose File]**&#x200B;并在设备或网络上找到文件。
1. 输入文件标题，该标题将在[!UICONTROL Ads]视图和报告中使用。
1. 单击 **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Video]:** 在帐户中以正确的格式选择任何之前上传的创作元素。

**[!UICONTROL Advanced: VAST Tag URL]:** （某些广告类型）要输入包含创意资产和跟踪像素的第三方VAST标记，请执行以下操作：

1. 单击![](/help/dsp/assets/compressed.png)旁边的箭头。**[!UICONTROL Advanced: VAST Tag URL]**
1. 在&#x200B;**[!UICONTROL URL]**&#x200B;字段中，输入VAST标记URL。
1. 输入文件的&#x200B;**[!UICONTROL Title]**，该文件将用在[!UICONTROL Ads]视图和报告中。

>[!TIP]
>
> 要检查VAST标记的有效性，请将其粘贴到浏览器中，然后点击&#x200B;**[!UICONTROL Enter]**&#x200B;键。 如果标记有效，您将在顶部附近看到一个包含`<VAST>`的XML文件。

**[!UICONTROL Advanced: 3rd party Ad Tag]:** （某些广告类型）要输入包含创意资产和跟踪像素的第三方广告标记，请执行以下操作：

1. 单击![](/help/dsp/assets/compressed.png)旁边的箭头。**[!UICONTROL Advanced: #3rd party Ad Tag]**
1. 输入文件的&#x200B;**[!UICONTROL Ad Title]**，该文件将用在[!UICONTROL Ads]视图和报告中。
1. 在&#x200B;**[!UICONTROL Ad Tag]**&#x200B;字段中，输入广告标记。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]:移动显示广告

**[!UICONTROL Ad Type]:** （只读）您创建的广告类型，与广告可附加到的版面类型相对应。

**[!UICONTROL Ad Name]:** 广告名称。默认情况下，会使用资产标题，但您可以更改名称。

>[!TIP]
>
> 在将广告附加到版面、广告视图和报表中时，使用易于查找的名称。 例如，描述设备类型和一些关键属性(例如“假日产品预览”：300x250游戏机”)。

**\[广告源\]**:是Advertising Cloud DSP提供广告(*[!UICONTROL Adobe served]*)，还是您使用的是第三方广告服务器(*[!UICONTROL 3rd party]*)。

**[!UICONTROL Creative type]:** (仅限Adobe投放的广告)资产是 *[!UICONTROL Image]* 资产 *[!UICONTROL HTML5]* 还是

**[!UICONTROL Asset]|  [!UICONTROL HTML5 Asset]:** (仅限Adobe投放的广告)要上传的图像文件或压缩的HTML5资产，具体取决于创作类型。单击&#x200B;**[!UICONTROL Browse]**&#x200B;并在设备或网络上找到文件，然后单击&#x200B;**[!UICONTROL Upload]**。

**[!UICONTROL Click URL]:** (仅限Adobe投放的广告)查看者单击广告后将登陆的URL。

**[!UICONTROL Final Click URL]:** (仅Adobe投放的广告；只读)具有必要Advertising Cloud DSP跟踪宏的点 [击](/help/dsp/campaign-management/macros.md) URL（如果适用）。

**[!UICONTROL Display Code]:** （仅限第三方广告）第三方创意资产的URL。任何[timestamp]和[[timestamp]]参数都将替换为实际值。

**[!UICONTROL Final Display Code]:** （仅限第三方广告）第三方创意资产的URL，并且已发送必要的Advertising Cloud DSP [跟踪](/help/dsp/campaign-management/macros.md) 宏（如果适用）。

### [!UICONTROL Basic]:视频广告

**[!UICONTROL Ad Type]:** （只读）您创建的广告类型，与广告可附加到的版面类型相对应。

**[!UICONTROL Ad Name]:** 广告名称。默认情况下，会使用资产标题，但您可以更改名称。

>[!TIP]
>
> 在将广告附加到版面、广告视图和报表中时，使用易于查找的名称。 例如，描述设备类型和一些关键属性(例如“假日产品预览”：30秒电话前置”)。

**[!UICONTROL Width]|  [!UICONTROL Ad Unit Width]:** 整个广告单元的宽度。此选项可能会被锁定，具体取决于您选择的广告单元类型。

**[!UICONTROL Height]|  [!UICONTROL Ad Unit Height]:** 整个广告单元的高度。此选项可能会被锁定，具体取决于您选择的广告单元类型。

**[!UICONTROL Player X]:** 广告单元的X坐标。保留默认设置。

**[!UICONTROL Player Y]:** 广告单元的Y坐标。保留默认设置。

**[!UICONTROL Player Width]:** 整个广告单元的宽度。此选项可能会被锁定，具体取决于您选择的广告单元类型。

与&#x200B;**[!UICONTROL Width]**&#x200B;字段相同。

**[!UICONTROL Player Height]:** 整个广告单元的高度。此选项可能会被锁定，具体取决于您选择的广告单元类型。

与&#x200B;**[!UICONTROL Height]**&#x200B;字段相同。

**[!UICONTROL Show Controls]:** 广告的视频控件应包含的位置： *[!UICONTROL Under]*、  *[!UICONTROL Over]*、 *[!UICONTROL Bottom]*&#x200B;或( *[!UICONTROL None]* 默认)。

**[!UICONTROL Preserve Aspect Ratio]:** 是保留视频的宽度和高度比例(*[!UICONTROL Yes]*)，还是拉伸视频以填充可用空间(*[!UICONTROL No]*)。

**[!UICONTROL Close Button Delay]:** （某些广告类型）关闭按钮外观延迟的秒数。

**[!UICONTROL Click URL]:** (仅限Adobe投放的广告)查看者单击广告后将登陆的URL。

**[!UICONTROL Final Click URL]:** (仅Adobe投放的广告；只读)具有必 [!UICONTROL Click URL] 要的Advertising Cloud DSP [跟踪](/help/dsp/campaign-management/macros.md) 宏（如果适用）。

**[!UICONTROL VAST Tag]:** (仅使用VAST标记的广告；只读)作为创意资产输入的第三方VAST标记。

**[!UICONTROL Final VAST Tag]:** (仅使用VAST标记的广告；只读)您作为创意资产输入的第三方VAST标记，且必要的Advertising Cloud DSP跟 [踪宏](/help/dsp/campaign-management/macros.md) （如果适用）。

**[!UICONTROL Wmode]:** （某些广告类型）窗口模式： *[!UICONTROL window]*、  *[!UICONTROL transparent]*&#x200B;或 *[!UICONTROL opaque]*。

### [!UICONTROL Teaser]

*DSP服务广告的移动点播播放格式*

**[!UICONTROL Asset]:** Teaser图像或视频资产：

* 要选择您自己的映像，请单击&#x200B;**[!UICONTROL Choose File],**&#x200B;在设备或网络上找到该文件，然后单击&#x200B;**[!UICONTROL Upload Image]**。

   最佳实践是使用与广告单元具有相同尺寸的图像。

* 要从创作元素中选择图像，请单击&#x200B;**[!UICONTROL Choose Thumbnail]**。

静态图像Teaser的要求：

* 格式：GIF、JPEG、PNG
* 图像大小：300x250
* 文件大小：50KB或更低
* 建议：行动动员、可识别图像、品牌徽标

Video Teaser的要求：

* 文件类型：MOV， MP4
* 文件大小：小于2MB
* 持续时间：7-10秒
* 建议：可识别的图像、面孔、快速剪切

### [!UICONTROL Overlays]

*用于DSP服务广告的交互式前置广告和移动交互式和点按播放格式*

以下设置适用于您创建或编辑的每个叠加。

**[!UICONTROL Asset]:** （仅限Raw资产）叠加图像资产。文件必须为单帧GIF、JPG或PNG格式，并且最大图像大小小于2 MB。 要上传资产，请单击&#x200B;**[!UICONTROL Browse]**&#x200B;并在设备或网络上找到文件，然后单击&#x200B;**[!UICONTROL Upload]**。

>[!TIP]
>
>请参阅[设计叠加的最佳实践](/help/dsp/campaign-management/ads/ad-best-practices-overlays.md)

**[!UICONTROL Click URL]:**  查看者单击广告的叠加图时将登陆的URL。

**[!UICONTROL X]:** 叠加的X坐标。选择叠加图的开始位置，然后输入开始位置的像素数（如从中心10像素）。 最佳做法是使用&#x200B;*From Center*，以防止叠加在发布者网站上随不同播放器大小而移动。

**[!UICONTROL Y]:** 叠加的Y坐标。选择叠加图的开始位置，然后输入开始位置的像素数（如顶部的10像素）。 最佳做法是根据您希望在广告上显示叠加图的位置，指定坐标&#x200B;*[!UICONTROL From Bottom]*&#x200B;或&#x200B;*[!UICONTROL From Top]、*。

**[!UICONTROL Layer]:** 将显示叠加的层。视频和每个叠加将分别位于不同的图层中。

* *[!UICONTROL 2 through 5]:* 在视频之前，但在其他叠加图之后。

* *[!UICONTROL 1]:* 在视频前面。

* *[!UICONTROL 0]:* 在与视频相同的图层中。视频将收缩以填充剩余空间。 不建议使用交互式前置广告。

* *[!UICONTROL -1]:* 在视频后面。

* *[!UICONTROL -2 through -5]:* 在视频后面，但在其他叠加图之前。

* *[!UICONTROL Background]:* 在视频和其他叠加图的后面。叠加图将缩放到视频的全宽和全高，且宽高比将不会保留。

### [!UICONTROL Endcap]

已弃用

### [!UICONTROL Pixel]

用于放置的所有现有事件跟踪像素都会自动附加。 您可以根据跟踪需求分离现有像素并根据需要创建新像素。

以下设置适用于您创建或编辑的每个像素。

**[!UICONTROL Integration Event]:** 触发像素的事件。对于此广告类型，请使用在&#x200B;*[!UICONTROL Impression]*&#x200B;或&#x200B;*[!UICONTROL Click-through]*&#x200B;上触发的像素。

**[!UICONTROL Pixel Type]:** 像素是(1x1 *[!UICONTROL IMG URL]* 像素图像文件)、 *[!UICONTROL HTML]*&#x200B;还是 *[!UICONTROL JavaScript URL]*。

**[!UICONTROL Pixel URL or Code]:** 像素图像的URL，采用指定的相应格式 [!UICONTROL Pixel Type]。

**[!UICONTROL Pixel Name]:** 像素名称。使用有助于您轻松识别像素的名称。

**[!UICONTROL Pixel Provider]:** 像素提供程序： *[!UICONTROL None]*、  *[!UICONTROL Nielsen]*&#x200B;或 *[!UICONTROL Comscore]*。

### [!UICONTROL Sharing]

已弃用

>[!MORELIKETHIS]
>
>* [关于广告管理](ad-about.md)
>* [创建广告](ad-create.md)
>* [列出与广告关联的版面](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [可用广告类型](ad-types.md)
>* [广告规范](/help/dsp/assets/ad-specs.pdf)
>* [设计叠加图的最佳实践](/help/dsp/campaign-management/ads/ad-best-practices-overlays.md)
>* [Advertising Cloud DSP宏](/help/dsp/campaign-management/macros.md)

