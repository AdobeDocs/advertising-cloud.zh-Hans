---
title: 创建多个第三方广告
description: 了解如何一次创建多个第三方广告。
feature: DSP Ads
exl-id: 83d35d27-1ab6-4fcf-877f-650a2dc6975a
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# 创建多个第三方广告

您一次最多可以创建500个第三方广告，方法是上传指向第三方广告服务器上托管的创意资产的标记。 您可以包含广告的跟踪像素。<!-- The bulksheet template for other ad servers says you can include 200. Which is it: 200 or 500? -->

您可以上传[!DNL DoubleClick]和[!DNL Flashtalking]标签表，或使用提供的模板手动填充的文件。

要创建单个第三方广告，请参阅[创建广告](ad-create.md)。

>[!TIP]
>
> 最佳实践是使用使用HTTPS安全提供的第三方广告。 使用HTTPS提供的URL以“https”开头。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Campaigns]**。

1. 单击将包含广告的营销活动的名称。

1. 在数据表上方，单击&#x200B;**[!UICONTROL Create]**。 在菜单的“广告类型”部分，单击&#x200B;**[!UICONTROL Bulk upload ads]**。

1. 选择广告托管在的广告服务器：*[!UICONTROL DoubleClick]*、*[!UICONTROL Flashtalking]*&#x200B;或&#x200B;*[!UICONTROL Other]*。

1. （[!DNL DoubleClick]和[!DNL Flashtalking]广告）选择要用于每个视频资产和每个显示资产的标记类型。 可用选项因广告服务器而异。

1. （除[!DNL DoubleClick]和[!DNL Flashtalking]之外的所有广告服务器上的广告）单击&#x200B;**[!UICONTROL Download this template]**&#x200B;以下载[!DNL Microsoft Excel]电子表格(XLSX)格式的模板，您可以使用广告数据填充该模板并在本地保存。 所需的列包括[!UICONTROL Ad Name]、[!UICONTROL VAST/VPAID URL or Ad Tag]和[!UICONTROL Ad Types]。

1. 单击&#x200B;**[!UICONTROL Upload]**&#x200B;并从设备或网络中选择.xlsx或.xls格式的文件。

   对于[!DNL DoubleClick]和[!DNL Flashtalking]广告，请从广告服务器上载未编辑的标签表。 对于其他广告服务器，请使用您在步骤3中下载的模板。

1. 上传完成后，单击&#x200B;**[!UICONTROL Start Building Ads]**。

1. 查看每个广告的详细信息和状态：

   1. 根据对上传标记的验证检查，查看每个广告的状态。
   1. （可选）对每个广告执行以下任意操作：
      * 要预览广告，请在广告行中单击![play](/help/dsp/assets/play.png)。
      * 要编辑广告详细信息，请单击![编辑](/help/dsp/assets/edit.png)，编辑详细信息，然后单击&#x200B;**保存**。
      * 要删除广告，请单击广告行中的&#x200B;**[!UICONTROL X]**。

1. 单击&#x200B;**[!UICONTROL Create *N *Ad(s)]**。

1. 执行以下操作之一：

   * 单击 **[!UICONTROL Done]**.

   * (如果广告被拒绝；（可选）要编辑广告记录并重新提交广告以供审核，请执行以下操作：
      1. 单击广告名称。
      1. 编辑广告设置。
      1. 单击 **[!UICONTROL Save & submit for review]**.

>[!MORELIKETHIS]
>
>* [关于广告管理](ad-about.md)
>* [创建广告](ad-create.md)
>* [可用广告类型](ad-types.md)
>* [广告规范](/help/dsp/assets/ad-specs.pdf)

