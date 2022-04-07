---
title: 音频广告设置
description: 请参阅音频广告的可用广告设置的描述。
feature: DSP Ads
exl-id: 746b6f40-ff59-4bbe-bfc0-3579d4461e4a
source-git-commit: 68af6b1846a37689dce0ca13a05cc1611b1f35a9
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# 音频广告设置

## [!UICONTROL Insert Ad Tag]

*仅新广告*

**[!UICONTROL URL]**:VAST标记URL。

**[!UICONTROL Title]**:文件的名称，将在 [!UICONTROL Ads] 查看和报表。

>[!TIP]
>
> 要检查VAST标记的有效性，请将其粘贴到浏览器中，然后点击 **[!UICONTROL Enter]** 键。 如果标记有效，您将看到一个包含 `<VAST>` 靠近顶部。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （只读）您创建的广告类型，与广告可附加到的版面类型相对应。 默认为 *[!UICONTROL Audio]*.

**[!UICONTROL Ad Name]:** 广告名称。 默认情况下，会使用资产标题，但您可以更改名称。

>[!TIP]
>
> 在 [!UICONTROL Ads] 视图和报表中。 例如，描述设备类型和一些关键属性(例如“假日产品预览”：30秒音频”)。

**[!UICONTROL Ad Duration]:** 音频文件的长度。 它自动设置为 [!UICONTROL 15] 或 [!UICONTROL 30]，具体取决于所选的广告单位。

根据帐户权限，可能会显示或不显示此字段。

**[!UICONTROL VAST Tag]:** （仅使用VAST标记的广告）第三方广告源的URL。 确保VAST标记仅包含音频媒体文件。

**[!UICONTROL Final VAST Tag]:** （仅使用VAST标记的广告）第三方广告源的URL，其中必需 [Advertising Cloud DSP跟踪宏](/help/dsp/campaign-management/macros.md) 插入（如果适用）。

**[!UICONTROL Select Rate]:** （仅限具有权限的用户）通过Adobe计费的预协商费率，或您已协商并将通过供应商计费的费率之一。 要添加费率，请联系您的 [!DNL Adobe] 客户团队。

### 像素

用于放置的所有现有事件跟踪像素都会自动附加。 您可以根据您对单个广告的跟踪需求，分离现有像素并根据需要创建新像素。

以下设置适用于您创建或编辑的每个像素。

**[!UICONTROL Integration Event]:** 触发像素的事件。 对于此广告类型，请使用 *[!UICONTROL Impression]* 或 *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** 像素是否为 *[!UICONTROL IMG UR]L* （1x1像素图像文件）， *[!UICONTROL HTML]*&#x200B;或 *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** 像素图像的URL，采用指定“像素类型”的相应格式。

**[!UICONTROL Pixel Name]:** 像素名称。 使用有助于您轻松识别像素的名称。

**[!UICONTROL Pixel Provider]:** 像素提供程序： *[!UICONTROL None]*, *[!UICONTROL Nielsen]*&#x200B;或 *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [关于广告管理](ad-about.md)
>* [创建单个广告](ad-create.md)
>* [列出与广告关联的版面](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [广告规范](/help/dsp/assets/ad-specs.pdf)
>* [Advertising Cloud DSP宏](/help/dsp/campaign-management/macros.md)

