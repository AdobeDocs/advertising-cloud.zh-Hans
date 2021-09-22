---
title: 创建和实施CCPA选择退出销售区段
description: 了解如何创建和实施区段以跟踪用户ID，使其免受消费者选择退出销售请求的影响。
feature: CCPA, DSP Segments
exl-id: aebe0c5b-382f-4e4a-b145-c32f32d216ca
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 0%

---

# 创建和实施CCPA选择退出销售区段

您可以根据《加州消费者隐私法案》(CCPA)创建一个区段，以跟踪网站上消费者选择退出销售请求中的用户ID。 用户将无限期地保留在CCPA选择退出销售区段中。

实施区段像素标记后，Advertising Cloud将开始代表广告商收集一个ID池。

>[!NOTE]
>
>* 有关如何使用Adobe Experience Platform Privacy Service API将CCPA选择退出销售请求传达到Advertising Cloud的信息，请参阅[https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html)。
>* 要跟踪出于与跟踪CCPA选择退出销售事件无关的目的访问网页的用户，以及从桌面、移动设备和CTV设备显示广告的用户，请创建[自定义区段](/help/dsp/audiences/custom-segment-create.md)。


1. 创建区段：

   1. 在主菜单中，单击&#x200B;**受众>区段**。

   1. 在数据表上方，单击&#x200B;**[!UICONTROL Create]**。

   1. 输入唯一的&#x200B;**[!UICONTROL Segment Name]**。

      推荐的区段名称：&quot;&lt;*您的广告商名称*> - CCPA Opt Out Of Sale&quot;（例如&quot;Acme - CCPA Opt Of Sale&quot;）

   1. 对于[!UICONTROL Segment Type]，选择&#x200B;**[!UICONTROL CCPA Opt-out of sale]**。

   1. 单击 **[!UICONTROL Save]**.

1. 复制并实施像素标记以跟踪区段：

   1. 返回到&#x200B;**[!UICONTROL Audiences]>[!UICONTROL Segments]**。

   1. 在区段行中，将光标悬停在新区段上，然后单击&#x200B;**[!UICONTROL Get pixel]**。

   1. 将图像像素（从`<img src="https://rtd-tm.everesttech.net"`开始）复制到网页，以收集桌面访客和移动设备访客的用户ID。

   1. 向广告商或网站联系人提供标记以供部署，使用公司用于跟踪CCPA选择退出销售请求的机制（例如使用同意管理平台）。

      广告商的IT部门或其他组可能需要安排或告知标记部署。

      实施像素后，Advertising Cloud将开始代表广告商收集一个ID池。

      尽管实施选项和逻辑取决于广告商，但以下是广告商如何触发像素的示例：

      1. 消费者登陆广告商的主页。
      1. 消费者在广告商的“CCPA选择退出销售”按钮上找到并单击该按钮。
      1. 向消费者提供广告商与其工作的服务提供商列表。
      1. 消费者会选中相应框以选择退出向Adobe Advertising Cloud出售数据。

         此操作会触发像素，并在指定的“[!UICONTROL CCPA Opt-out of sale]”区段内收集消费者的Cookie ID。

>[!MORELIKETHIS]
>
>* [Adobe Advertising Cloud对《加州消费者隐私法案》的支持：消费者选择退出支持](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html)
>* [关于 [!UICONTROL CCPA Opt-out-of-Sale] 区段和报表](ccpa-opt-out-about.md)
>* [检索消费者选择退出销售报表](ccpa-opt-out-segment-report-retrieve.md)
>* [创建和实施自定义区段](custom-segment-create.md)
>* [关于受众管理](audience-about.md)

