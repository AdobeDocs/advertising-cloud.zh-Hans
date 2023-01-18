---
title: 创建和实施CCPA选择退出销售区段
description: 了解如何创建和实施区段以跟踪用户ID，使其免受消费者选择退出销售请求的影响。
feature: CCPA, DSP Segments
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---

# 创建和实施CCPA选择退出销售区段

您可以根据《加州消费者隐私法案》(CCPA)创建一个区段，以跟踪网站上消费者选择退出销售请求中的用户ID。 用户将无限期地保留在CCPA选择退出销售区段中。

实施区段像素标记后，Adobe广告将开始代表广告商收集一个ID池。

>[!NOTE]
>
>* 有关如何使用Adobe Experience Platform Privacy Service API传达CCPA选择退出销售请求以Adobe广告的信息，请参阅 [https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ccpa-opt-out-of-sale.html](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ccpa-opt-out-of-sale.html).
>* 要跟踪出于与跟踪CCPA选择退出销售事件无关的目的访问网页的用户，以及从桌面、移动设备和CTV设备接触广告的用户，请创建 [自定义区段](/help/dsp/audiences/custom-segment-create.md).


1. 创建区段：

   1. 在主菜单中，单击 **受众>区段**.

   1. 在数据表上方，单击 **[!UICONTROL Create]**.

   1. 输入唯一 **[!UICONTROL Segment Name]**.

      推荐的区段名称：&quot;&lt;*您的广告商名称*> - CCPA Opt Out Of Sale”（例如“Acme - CCPA Opt Out Of Sale”）

   1. 对于 [!UICONTROL Segment Type]，选择 **[!UICONTROL CCPA Opt-out of sale]**.

   1. 单击 **[!UICONTROL Save]**.

1. 复制并实施像素标记以跟踪区段：

   1. 返回 **[!UICONTROL Audiences]>[!UICONTROL Segments]**.

   1. 在区段行中，将光标悬停在新区段上并单击 **[!UICONTROL Get pixel]**.

   1. 复制图像像素(从 `<img src="https://rtd-tm.everesttech.net"`)收集桌面访客和移动设备访客的用户ID到网页。

   1. 向广告商或网站联系人提供标记以供部署，使用公司用于跟踪CCPA选择退出销售请求的机制（例如使用同意管理平台）。

      广告商的IT部门或其他组可能需要安排或告知标记部署。

      实施像素后，Adobe广告将开始代表广告商收集一个ID池。

      尽管实施选项和逻辑取决于广告商，但以下是广告商如何触发像素的示例：

      1. 消费者登陆广告商的主页。
      1. 消费者在广告商的“CCPA选择退出销售”按钮上找到并单击该按钮。
      1. 向消费者提供广告商与其工作的服务提供商列表。
      1. 消费者会选中相应框以选择退出向Adobe广告销售数据。

         此操作会触发像素，并在指定的“”中收集消费者的Cookie ID[!UICONTROL CCPA Opt-out of sale]“区段”。

>[!MORELIKETHIS]
>
>* [Adobe对《加州消费者隐私法案》的广告支持：消费者选择退出支持](/help/privacy/ccpa-opt-out-of-sale.md)
>* [关于 [!UICONTROL CCPA Opt-out-of-Sale] 区段和报表](ccpa-opt-out-about.md)
>* [检索消费者选择退出销售报表](ccpa-opt-out-segment-report-retrieve.md)
>* [创建和实施自定义区段](custom-segment-create.md)
>* [关于受众管理](audience-about.md)

