---
title: 显示广告设置
description: 请参阅展示广告的可用广告设置的描述。
feature: DSP Ads
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 0%

---

# 显示广告设置

以下设置适用于标准显示广告。

## [!UICONTROL Ad Options]

### 基本

**[!UICONTROL Ad Type]:** （只读）您创建的广告类型，与广告可附加到的版面类型相对应。 默认为 *[!UICONTROL Display]*.

**[!UICONTROL Ad Name]:** 广告名称。 默认情况下，会使用资产标题，但您可以更改名称。

>[!TIP]
>
> 在 [!UICONTROL Ads] 视图和报表中。 例如，描述设备类型和一些关键属性(例如“假日产品预览”：300x250游戏机”)。

**\[广告源\]**:（只读） *[!UICONTROL 3rd party]*.

**[!UICONTROL This is an expandable Banner]:** （仅限第三方广告）指示广告是可扩展的横幅广告。 相关的扩展设置可确定要购买的库存，因此请确保它们反映广告行为。

**[!UICONTROL Expansion Method]:** （仅限第三方可扩展的横幅广告）横幅是否在 *[!UICONTROL Click]* 或 *[!UICONTROL Rollover]*.

**[!UICONTROL Expansion Directions]:** （仅限第三方可扩展的横幅广告）广告展开的方向： *[!UICONTROL Up]*, *[!UICONTROL Down]*, *[!UICONTROL Left]*&#x200B;或 *[!UICONTROL Right]*.

**[!UICONTROL Certified Vendors]:** （仅限第三方可扩展横幅广告）广告可用的认证供应商： *[!UICONTROL DCM]* ([!DNL Google DoubleClick for Advertisers])、 *[!UICONTROL Flashtalking]*, *[!UICONTROL Sizmek]*&#x200B;或 *[!UICONTROL Jivox]*.

**[!UICONTROL Display Code]:** （仅限第三方广告）第三方创意资产的URL。 任意 [timestamp] 和[[timestamp]]参数将被实际值替换。

**[!UICONTROL Final Display Code]:** （仅限第三方广告）第三方创意资产的URL，并且必要 [Advertising DSP跟踪宏](/help/dsp/campaign-management/macros.md) 插入（如果适用）。

**[!UICONTROL Ad Size]:** 广告的宽度和高度。 它必须是 [支持的标准显示广告大小](ad-specs.md). 您可以在上传广告之前手动输入广告大小或输入 [!UICONTROL Display Code]. 如果不输入广告大小，则上载的广告或广告标记的维度将自动输入为只读。 请注意，如果维度不在标准显示中，则不会保存显示广告，例如301x250，而不是300x250广告大小。

>[!IMPORTANT]
>
> 在宽度和高度字段中声明的广告大小将与传入的竞价请求匹配。 如果广告的维度与声明的广告大小不匹配，则可能会遇到投放问题。

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
>* [列出与广告关联的版面](ad-list-placements.md)
>* [广告规范](ad-specs.md)
>* [DSP宏](/help/dsp/campaign-management/macros.md)

