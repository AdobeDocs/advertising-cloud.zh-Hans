---
title: 前置广告设置
description: 请参阅前置广告的可用广告设置的描述。
feature: Ads
exl-id: 638d5a3d-3dff-40b6-a3ba-7ab3f08282b9
source-git-commit: e2ee41c7e3e195f062ad1cc67080ed913d6d3d06
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 前置广告设置

## [!UICONTROL Upload or Select Creative]

*仅新广告*

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

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （只读）您创建的广告类型，与广告可附加到的版面类型相对应。

**[!UICONTROL Ad Name]:** 广告名称。默认情况下，会使用资产标题，但您可以更改名称。

>[!TIP]
>
> 在[!UICONTROL Ads]视图和报表中，使用在将广告附加到版面时容易找到的名称。 例如，描述设备类型和一些关键属性(例如“假日产品预览”：30秒前置”)。

**[!UICONTROL Width]|  [!UICONTROL Ad Unit Width]:** （仅限标准和可跳过的前置广告）整个广告单元的宽度。此选项可能会被锁定，具体取决于您选择的广告单元类型。

**[!UICONTROL Height]|  [!UICONTROL Ad Unit Height]:** （仅限标准和可跳过的前置广告）整个广告单元的高度。此选项可能会被锁定，具体取决于您选择的广告单元类型。

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

**[!UICONTROL Wmode]:** （仅限交互式前置）窗口模式： *[!UICONTROL window]*、  *[!UICONTROL transparent]*&#x200B;或 *[!UICONTROL opaque]*。

**[!UICONTROL Video Format]:** （仅限交互式前置广告）潜在库存的广告播放器格式： *[!UICONTROL VPAID]* 或 *[!UICONTROL VPAID & VAST]*。可视性始终针对VPAID进行测量，但VPAID和VAST包含的库存不允许可视性测量。 如果可视性量度对您的营销活动很重要，请牢记这一点。

**[!UICONTROL Clock Number]**:(仅交互式前置广告；仅在英国使用；仅供具有权限的用户使用)用于确保广播正确广告的唯一标识符。如果此设置不适用，请将其留空。

### [!UICONTROL Companion]

*仅DSP提供的广告*

您可以选择在广告中最多附加三个伴随横幅。 最佳做法是尽可能附加伴随横幅。

>[!NOTE]
>
> 并非所有发布者都允许附带横幅。 允许伴随横幅的发布者不保证伴随横幅的展示次数。
> 来自第三方广告标签的伴随横幅可能无法始终预览。

**\[复选框\]:** 包含广告中指定的伴随横幅。禁用此复选框时，将不包含伴随横幅。

**\[横幅大小\]:** 伴随横幅大小： *[!UICONTROL 300x600 (Skyscraper)]*; *[!UICONTROL 300x250 (Medium Rectangle)]*，这是最常见的广告大小，并推荐用于所有广告； *[!UICONTROL 300x60 (Small Banner)]*;或， *[!UICONTROL 728x90 (Leaderboard)]*&#x200B;这是较不常见的广告大小。

**\[来源\]:** 您是在上传您自己的伴侣横幅资产，还是使用第三方标记。

**资产：** （仅限Raw资产）伴随横幅资产。单击&#x200B;**[!UICONTROL Browse]**&#x200B;并在设备或网络上找到文件，然后单击&#x200B;**[!UICONTROL Upload]**。

**广告标记]:[!UICONTROL **（仅使用VAST标记的广告）指向第三方配套横幅源的URL。

**[!UICONTROL Final Ad Tag]:** （仅使用VAST标记的广告）指向第三方配套横幅源的URL，且必要的Advertising Cloud DSP [跟踪](/help/dsp/campaign-management/macros.md) 宏（如果适用）。

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

### [!UICONTROL Pixel]

用于放置的所有现有事件跟踪像素都会自动附加。 您可以根据跟踪需求分离现有像素并根据需要创建新像素。

以下设置适用于您创建或编辑的每个像素。

**[!UICONTROL Integration Event]:** 触发像素的事件。对于此广告类型，请使用在&#x200B;*[!UICONTROL Impression]*&#x200B;或&#x200B;*[!UICONTROL Click-through]*&#x200B;上触发的像素。

**[!UICONTROL Pixel Type]:** 像素是(1x1 *[!UICONTROL IMG URL]* 像素图像文件)、 *[!UICONTROL HTML]*&#x200B;还是 *[!UICONTROL JavaScript URL]*。

**[!UICONTROL Pixel URL or Code]:** 像素图像的URL，采用指定的相应格式 [!UICONTROL Pixel Type]。

**[!UICONTROL Pixel Name]:** 像素名称。使用有助于您轻松识别像素的名称。

**[!UICONTROL Pixel Provider]:** 像素提供程序： *[!UICONTROL None]*、  *[!UICONTROL Nielsen]*&#x200B;或 *[!UICONTROL Comscore]*。

>[!MORELIKETHIS]
>
>* [关于广告管理](ad-about.md)
>* [创建广告](ad-create.md)
>* [列出与广告关联的版面](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [可用广告类型](ad-types.md)
>* [广告规范](/help/dsp/assets/ad-specs.pdf)
>* [设计叠加图的最佳实践](/help/dsp/campaign-management/ads/ad-best-practices-overlays.md)
>* [Advertising Cloud DSP宏](/help/dsp/campaign-management/macros.md)

