---
title: 显示广告设置
description: 请参阅展示广告的可用广告设置的描述。
feature: Ads
exl-id: ae88dfab-0b0c-42ab-9135-422b20a4b6cd
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 0%

---

# 显示广告设置

以下设置适用于标准显示广告。 您也可以为展示广告提供点击播放视频广告，但我们不建议这样做，因为支持这些广告的发布者不多。

## [!UICONTROL Ad Options]

### 基本

**[!UICONTROL Ad Type]:** （只读）您创建的广告类型，与广告可附加到的版面类型相对应。默认为&#x200B;*[!UICONTROL Display]*。

**[!UICONTROL Ad Name]:** 广告名称。默认情况下，会使用资产标题，但您可以更改名称。

>[!TIP]
>
> 在[!UICONTROL Ads]视图和报表中，使用在将广告附加到版面时容易找到的名称。 例如，描述设备类型和一些关键属性(例如“假日产品预览”：300x250游戏机”)。

**\[广告源\]**:是Advertising Cloud DSP提供广告(*[!UICONTROL Adobe served]*)，还是您使用的是第三方广告服务器(*[!UICONTROL 3rd party]*)。

**[!UICONTROL This is an expandable Banner]:** （仅限第三方广告）指示广告是可扩展的横幅广告。相关的扩展设置可确定要购买的库存，因此请确保它们反映广告行为。

**[!UICONTROL Expansion Method]:** （仅限第三方可扩展的横幅广告）横幅是在上面展开还 *[!UICONTROL Click]* 是 *[!UICONTROL Rollover]*&#x200B;展开。

**[!UICONTROL Expansion Directions]:** （仅限第三方可扩展的横幅广告）广告展开的方向： *[!UICONTROL Up]*、  *[!UICONTROL Down]*、  *[!UICONTROL Left]*&#x200B;或 *[!UICONTROL Right]*。

**[!UICONTROL Certified Vendors]:** （仅限第三方可扩展的横幅广告）广告可用的认证供应商： *[!UICONTROL DCM]* ([!DNL Google DoubleClick for Advertisers])、 *[!UICONTROL Flashtalking]*、 *[!UICONTROL Sizmek]*&#x200B;或 *[!UICONTROL Jivox]*。

**[!UICONTROL Display Code]:** （仅限第三方广告）第三方创意资产的URL。任何[timestamp]和[[timestamp]]参数都将替换为实际值。

**[!UICONTROL Final Display Code]:** （仅限第三方广告）第三方创意资产的URL，并且已发送必要的Advertising Cloud DSP [跟踪](/help/dsp/campaign-management/macros.md) 宏（如果适用）。

**[!UICONTROL Creative type]:** (仅限Adobe投放的广告)资产是 *[!UICONTROL Image]* 资产 *[!UICONTROL HTML5]* 还是

**[!UICONTROL Asset]|  [!UICONTROL HTML5 Asset]:** (仅限Adobe投放的广告)要上传的图像文件或压缩的HTML5资产，具体取决于创作类型。单击&#x200B;**[!UICONTROL Browse]**&#x200B;并在设备或网络上找到文件，然后单击&#x200B;**[!UICONTROL Upload]**&#x200B;或&#x200B;**[!UICONTROL Upload Image]**。

**[!UICONTROL Ad Size]:** 广告的宽度和高度。它必须是[支持的标准显示广告大小](/help/dsp/assets/ad-specs.pdf)。 您可以在上传广告之前手动输入广告大小或输入[!UICONTROL Display Code]。 如果不输入广告大小，则上载的广告或广告标记的维度将自动输入为只读。 请注意，如果维度不在标准显示中，则不会保存显示广告，例如301x250，而不是300x250广告大小。

>[!IMPORTANT]
>
> 在宽度和高度字段中声明的广告大小将与传入的竞价请求匹配。 如果广告的维度与声明的广告大小不匹配，则可能会遇到投放问题。

**[!UICONTROL Click URL]:** (仅限Adobe投放的广告)查看者单击广告后将登陆的URL。

**[!UICONTROL Final Click URL]:** (仅Adobe投放的广告；只读)具有必 [!UICONTROL Click URL] 要的Advertising Cloud DSP [跟踪](/help/dsp/campaign-management/macros.md) 宏（如果适用）。

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
>* [列出与广告关联的版面](ad-list-placements.md)
>* [可用广告类型](ad-types.md)
>* [广告规范](/help/dsp/assets/ad-specs.pdf)
>* [Advertising Cloud DSP宏](/help/dsp/campaign-management/macros.md)

