---
title: 关于Advertising Cloud DSP中的广告管理
description: 了解广告管理。
feature: Ads
exl-id: 72c8bbef-d09c-4cf4-994d-99578d043d39
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 0%

---

# 关于Advertising Cloud DSP中的广告管理

<!-- add "The Ads View (Dashboard?)" section -->

Advertising Cloud DSP提供了两种提供广告的方法：

* 当您将自己的资产（例如显示横幅、视频资产、音频文件或URL）直接上传到DSP时，Advertising Cloud DSP将免费提供您的广告。 对于DSP提供的资产，您可以访问其他功能，如叠加。

* 如果您使用第三方广告服务器（如Google、Flashtalking或Sizmek），则可以单独或批量将第三方广告服务标签上传到DSP。 批量上传功能要求您a)上传DoubleClick和Flashtalking标签表，或b)下载模板，将您的标签输入到模板中，然后重新上传模板。<!-- need a list of all supported third-party ad servers; see file in future-tbd folder -->

设置广告后，您需要将每个广告附加到版面，其中包括将控制营销活动投放方式的定位参数（如地域、受众、设备和库存定位）。 您可以将单个广告附加到一个或多个版面。

## 可用广告类型

* 音频
* 连接的电视
* 显示
* 移动设备
* 本机
* 前置广告

有关这些广告类型的更多信息，请参阅[可用广告类型](ad-types.md)和完整的[广告规范](/help/dsp/assets/ad-specs.pdf)。

## 特殊广告功能

以下功能仅适用于DSP提供的广告。

### 伴随横幅

伴随横幅与[前置广告](ad-settings-pre-roll.md)或（与某些发布者一起）[音频广告](ad-settings-audio.md)一起提供，有助于加强品牌和消息关联。

>[!NOTE]
>
>* 并非所有发布者都允许附带横幅。 允许伴随横幅的发布者不保证伴随横幅的展示次数。
>* 来自第三方广告标签的伴随横幅可能无法始终预览。


您可以上传自己的伴侣横幅资产，或从经认证的第三方广告服务合作伙伴上传第三方iFrame或脚本横幅标记。

### 叠加

叠加图有助于在整个视频中实现持续品牌化，并且可以推动更多点击。 叠加功能适用于[交互式前置广告](ad-settings-pre-roll.md)和[交互式和点按播放格式](ad-settings-mobile.md)的移动广告。

请参阅[设计叠加的最佳实践](/help/dsp/campaign-management/ads/ad-best-practices-overlays.md)

### Teaser

Teaser是一幅吸引眼球的图像，它鼓励查看者播放广告。 Teaser仅适用于移动设备点按播放广告格式。

## Advertising Cloud DSP广告批准

创建广告时，Advertising Cloud DSP会针对敏感类别对其进行审核，单击URL功能并预览渲染。

最初，您会在[!UICONTROL Status]列中看到一个红色圆点。 审核过程通常需要24-48小时。 但是，损坏的广告可能具有超过48小时的待决状态，因此您有时间在广告被拒绝之前修复错误。 被拒绝的广告包括拒绝的原因。

当DSP批准广告时，“状态”列中将显示一个绿色圆点。

![列中的批准指 [!UICONTROL Status] 示器](/help/dsp/assets/ad-approval-status.png)

>[!NOTE]
>
>仅当DSP和SSP都批准了创作元素时，才会提供您的广告。 每个SSP都有自己的批准要求和流程。

>[!MORELIKETHIS]
>
>* [创建广告](ad-create.md)
>* [创建多个第三方广告](ad-create-third-party.md)
>* [可用广告类型](ad-types.md)
>* [广告规范](/help/dsp/assets/ad-specs.pdf)

