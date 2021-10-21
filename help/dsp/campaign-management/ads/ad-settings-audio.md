---
title: 音频广告设置
description: 请参阅音频广告的可用广告设置的描述。
feature: DSP Ads
exl-id: 746b6f40-ff59-4bbe-bfc0-3579d4461e4a
source-git-commit: e0713f3717a684fb5ef2808d7de769424b8972d2
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 0%

---

# 音频广告设置

## [!UICONTROL Upload or Select Creative]

*仅新广告*

**[!UICONTROL Upload Audio]:** 将原始资产上传到DSP。 选择此选项时，请执行以下操作：

1. 单击 **[!UICONTROL Choose File]** 并在设备或网络上找到文件。
1. 输入文件的标题，该标题将在 [!UICONTROL Ads] 查看和报表。
1. 单击 **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Audio]:** 选择帐户中任何以正确格式上传的创作元素。

**[!UICONTROL Advanced: VAST Tag URL]:** 要输入包含创意资产和跟踪像素的第三方VAST标记，请执行以下操作：

1. 单击 ![箭头](/help/dsp/assets/compressed.png) 下一页 **[!UICONTROL Advanced: VAST Tag URL]**.
1. 在 **[!UICONTROL URL]** 字段中，输入VAST标记URL。
1. 输入 **[!UICONTROL Title]** ，将在 [!UICONTROL Ads] 查看和报表。

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

**[!UICONTROL Click URL]:** (使用原始资产且仅带有显示横幅的广告；（可选）查看者点击与您的广告一起显示的横幅时将登陆的URL。

**[!UICONTROL Final Click URL]:** (使用原始资产且仅带有显示横幅的广告；只读) [!UICONTROL Click URL] 必要 [Advertising Cloud DSP跟踪宏](/help/dsp/campaign-management/macros.md) 插入（如果适用）。

**[!UICONTROL VAST Tag]:** （仅使用VAST标记的广告）第三方广告源的URL。 确保VAST标记仅包含音频媒体文件。

**[!UICONTROL Final VAST Tag]:** （仅使用VAST标记的广告）第三方广告源的URL，其中必需 [Advertising Cloud DSP跟踪宏](/help/dsp/campaign-management/macros.md) 插入（如果适用）。

**[!UICONTROL Select Rate]:** （仅限具有权限的用户）通过Adobe计费的预协商费率，或您已协商并将通过供应商计费的费率之一。 要添加费率，请联系您的 [!DNL Adobe] 客户经理。

### [!UICONTROL Companion]

*仅DSP提供的广告*

您可以选择在广告中最多附加三个伴随横幅。 最佳做法是尽可能附加伴随横幅。

>[!NOTE]
>
>* 并非所有发布者都允许附带横幅。 允许伴随横幅的发布者不保证伴随横幅的展示次数。
>* 来自第三方广告标签的伴随横幅可能无法始终预览。


**\[复选框\]:** 包含广告中指定的伴随横幅。 禁用此复选框时，将不包含伴随横幅。

**\[横幅大小\]:** 伴随横幅大小： *[!UICONTROL 300x250]* (用于 [!DNL iHeartRadio], [!DNL Spotify], [!DNL SoundCloud]和 [!DNL TuneIn])、 *[!UICONTROL 640x640]* (用于 [!DNL Spotify), or *1024x1024]*(用于 [!DNL SoundCloud])。

**\[源\]:** 伴随横幅资产的来源：

* *[!UICONTROL Upload My Own Asset]:* 上传您自己的资产。
* *[!UICONTROL Use a Third Party Tag]:* 从经认证的第三方广告服务合作伙伴输入iFrame或脚本标记。

如果要跟踪第三方伴随横幅展示次数，请使用第三方标记。

**[!UICONTROL Asset]:** （仅限原始资产）GIF、JPG或PNG格式的伴随横幅资产。 单击 **[!UICONTROL Browse]** 并在您的设备或网络上找到文件，然后单击 **[!UICONTROL Upload]**.

**[!UICONTROL Click URL]:** （仅限原始资产）查看者单击广告的配套横幅时将登陆的URL。 它可以包含使用第三方点击跟踪像素的点击重定向。

**[!UICONTROL Final Click URL]:** (仅限原始资产；只读)具有必需 [Advertising Cloud DSP跟踪宏](/help/dsp/campaign-management/macros.md) 插入（如果适用）。

**[!UICONTROL Ad Tag]:** （仅使用第三方广告标记的广告）第三方配套横幅源的iFrame或脚本横幅标记。 它必须来自经认证的第三方广告服务合作伙伴。

**[!UICONTROL Final Ad Tag]:** （仅使用第三方广告标签的广告） [Advertising Cloud DSP跟踪宏](/help/dsp/campaign-management/macros.md) 插入（如果适用）。

### 像素

用于放置的所有现有事件跟踪像素都会自动附加。 您可以根据跟踪需求分离现有像素并根据需要创建新像素。

以下设置适用于您创建或编辑的每个像素。

**[!UICONTROL Integration Event]:** 触发像素的事件。 对于此广告类型，请使用 *[!UICONTROL Impression]* 或 *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** 像素是否为 *[!UICONTROL IMG UR]L* （1x1像素图像文件）， *[!UICONTROL HTML]*&#x200B;或 *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** 像素图像的URL，采用指定“像素类型”的相应格式。

**[!UICONTROL Pixel Name]:** 像素名称。 使用有助于您轻松识别像素的名称。

**[!UICONTROL Pixel Provider]:** 像素提供程序： *[!UICONTROL None]*, *[!UICONTROL Nielsen]*&#x200B;或 *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [关于广告管理](ad-about.md)
>* [创建广告](ad-create.md)
>* [列出与广告关联的版面](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [可用广告类型](ad-types.md)
>* [广告规范](/help/dsp/assets/ad-specs.pdf)
>* [Advertising Cloud DSP宏](/help/dsp/campaign-management/macros.md)

