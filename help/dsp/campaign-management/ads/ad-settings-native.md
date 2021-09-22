---
title: 本机广告设置
description: 请参阅对本机广告可用广告设置的描述。
feature: DSP Ads
exl-id: 3ae59e63-ae64-41b2-8734-3df2da020c7c
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# 本机广告设置

## [!UICONTROL Upload or Select Creative]

*仅新增视频（但不显示）广告*

**[!UICONTROL Upload Audio]:** 将原始资产上传到DSP。选择此选项时，请执行以下操作：

1. 单击&#x200B;**[!UICONTROL Choose File]**&#x200B;并在设备或网络上找到文件。
1. 输入文件标题，该标题将在[!UICONTROL Ads]视图和报告中使用。
1. 单击 **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Audio]:** 在帐户中以正确的格式选择任何之前上传的创作元素。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （只读）您创建的广告类型，与广告可附加到的版面类型相对应。

**[!UICONTROL Ad Name]:** 广告名称。默认情况下，会使用广告类型（显示本机）或视频标题（视频格式），但您可以更改名称。

>[!TIP]
>
> 在[!UICONTROL Ads]视图和报表中，使用在将广告附加到版面时容易找到的名称。 例如，描述设备类型和一些关键属性(例如“假日产品预览”：15秒本机”)。

**[!UICONTROL Native Creative]:** 1200x627图像，可最大程度地提高移动设备库存的交付。对于视频广告，这将是在播放本机视频之前显示的图像。 单击&#x200B;**[!UICONTROL Browse]**&#x200B;并在设备或网络上找到文件，然后单击&#x200B;**[!UICONTROL Upload]**。

**[!UICONTROL Title]:** 吸引观看者眼球的标题。

**[!UICONTROL Description]:** 对于视频广告，这是广告的简短摘要。对于展示广告，这是广告的正文。 最大长度为100个字符。

**[!UICONTROL Landing Page]:** 查看者单击广告后将登陆的URL。

**[!UICONTROL Final Landing Page]:** 包含必 [!UICONTROL Landing Page] 要的Advertising Cloud DSP跟 [踪宏](/help/dsp/campaign-management/macros.md) 的URL（如果适用）。

**[!UICONTROL Sponsored By (Advertiser Name)]:** 广告的广告商。

**[!UICONTROL Call to Action]:** （可选）您希望查看者在看到此广告后执行的步骤。

**[!UICONTROL Advertiser Logo]:** （可选）要包含在广告中的1:1比率徽标，以便获得更多品牌认可。单击&#x200B;**[!UICONTROL Browse]**&#x200B;并在设备或网络上找到文件，然后单击&#x200B;**[!UICONTROL Upload]**。

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
>* [Advertising Cloud DSP宏](/help/dsp/campaign-management/macros.md)

