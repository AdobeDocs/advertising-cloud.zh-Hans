---
title: 本机显示广告设置
description: 请参阅对本机显示广告的可用广告设置的描述。
feature: DSP Ads
exl-id: 3ae59e63-ae64-41b2-8734-3df2da020c7c
source-git-commit: 68af6b1846a37689dce0ca13a05cc1611b1f35a9
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
> 在 [!UICONTROL Ads] 视图和报表中。 例如，描述设备类型和一些关键属性(例如“假日产品预览”：15秒本机”)。

**[!UICONTROL Native Creative]:** 1200x627图像，可最大限度地提供移动设备库存。 单击 **[!UICONTROL Browse]** 并在您的设备或网络上找到文件，然后单击 **[!UICONTROL Upload]**.

**[!UICONTROL Title]:** 一个吸引观众眼球的标题。

**[!UICONTROL Description]:** 广告的正文。 最大长度为100个字符。

**[!UICONTROL Landing Page]:** 查看者单击广告后登陆的URL。

**[!UICONTROL Final Landing Page]:** 的 [!UICONTROL Landing Page] 具有必需 [Advertising Cloud DSP跟踪宏](/help/dsp/campaign-management/macros.md) 插入（如果适用）。

**[!UICONTROL Sponsored By (Advertiser Name)]:** 广告的广告商。

**[!UICONTROL Call to Action]:** （可选）您希望查看者在看到此广告后执行的步骤。

**[!UICONTROL Advertiser Logo]:** （可选）要包含在广告中的1:1比率徽标，以获得更多品牌认可。 单击 **[!UICONTROL Browse]** 并在您的设备或网络上找到文件，然后单击 **[!UICONTROL Upload]**.

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
>* [广告规范](/help/dsp/assets/ad-specs.pdf)
>* [Advertising Cloud DSP宏](/help/dsp/campaign-management/macros.md)

