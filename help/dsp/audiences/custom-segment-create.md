---
title: 创建和实施自定义区段
description: 了解如何创建和实施自定义区段，以跟踪展示给广告的用户或访问您网页的用户。
feature: DSP Segments
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---

# 创建和实施自定义区段

您可以通过创建和实施自定义DSP区段来收集您自己的第一方受众数据。 您可以使用该区段来跟踪a)从桌面、移动设备和CTV设备显示广告的用户以及b)访问特定网页的用户。 您可以稍后使用其他广告重新定位区段中的用户，或阻止区段中的用户接收其他广告。

>[!NOTE]
>
>要根据《加州消费者隐私法案》(CCPA)的规定，从您网站上的消费者选择退出销售请求中跟踪用户ID，请创建 [CCPA选择退出销售区段](ccpa-opt-out-segment-create.md).

1. 创建区段：

   1. 在主菜单中，单击 **[!UICONTROL Audiences]>[!UICONTROL Segments]**.

   1. 在数据表上方，单击 **[!UICONTROL Create]**.

   1. 输入唯一 **[!UICONTROL Segment Name]**.

   1. 对于 **[!UICONTROL Segment Type]**，选择 *[!UICONTROL Custom]*.

   1. 输入 **[!UICONTROL Segment Window]**，用户的cookie在区段中停留的天数。

      默认窗口为45天。 输入一(1)到365之间的值。

   1. 单击 **[!UICONTROL Save]**.

1. 根据需要复制并实施标记以跟踪区段：

   1. 返回 **[!UICONTROL Audiences]>[!UICONTROL Segments]**.

   2. 将光标悬停在区段行上并单击 **[!UICONTROL Get Pixel]**.

      * 要跟踪网页的桌面和移动设备访客，请执行以下操作：

         1. 复制标记为“[!UICONTROL Desktop or mobile websites].&quot;

         1. 向广告商或网站联系人提供标记以进行部署。

            广告商的IT部门或其他组可能需要安排或告知标记部署。
      * 要跟踪在桌面、移动设备或CTV设备上显示到广告单元的用户，请执行以下操作：

         1. 复制标记为“[!UICONTROL Desktop or mobile ads].&quot;


1. 将标记添加到 [!UICONTROL Pixel] 选项卡 [!UICONTROL Event Pixels] 部分 [[!UICONTROL Tracking] 每个相关版面的设置](/help/dsp/campaign-management/placements/placement-settings.md#placement-tracking).

实施跟踪标记后，您可以在受众目标或排除项中将该区段用于任何版面。

>[!TIP]
>
>在跟踪用户时，跟踪区段大小。

>[!MORELIKETHIS]
>
>* [关于受众管理](audience-about.md)
>* [编辑区段信息](segment-edit.md)
>* [删除区段](segment-delete.md)
>* [查看区段的跟踪像素](segment-view-pixels.md)
>* [共享或停止共享区段](segment-share.md)
>* [创建和实施 [!UICONTROL CCPA Opt-Out-of-Sale] 区段](ccpa-opt-out-segment-create.md)
>* [创建可重用受众](reusable-audience-create.md)
>* [可用的第三方数据提供商](third-party-data-providers.md)
>* [版面设置](/help/dsp/campaign-management/placements/placement-settings.md)

