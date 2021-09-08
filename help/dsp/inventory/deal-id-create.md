---
title: 手动创建交易ID详细信息
description: 了解如何手动输入交易ID的详细信息。
feature: Private Inventory, Deal IDs
exl-id: cd9763a7-99d4-4881-9df9-b4e24c55be0f
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 手动创建交易ID详细信息

1. 在主菜单中，单击&#x200B;**[!UICONTROL Inventory]> [!UICONTROL Deals]。**

1. 在数据表上方，单击&#x200B;**[!UICONTROL Create]**，然后选择&#x200B;**[!UICONTROL Deal ID]**。

1. 输入[deal settings](deal-id-settings.md):

   1. 在[!UICONTROL Deal ID basics]部分中，指定交易详细信息以及可访问交易的广告商。 对于有保证的交易，您还必须指定计划的投放日期和预计的展示次数，以便仅用于跟踪。

   1. (仅管理员用户；（可选）在[!UICONTROL Technical]部分中，根据需要编辑默认设置。

   1. 单击 **[!UICONTROL Save]**.

1. （仅限保证交易）选择将用于交易的广告，并创建默认的程序化保证(PG)投放。

   默认的PG投放可确保您的交易始终为每个竞价请求返回竞价。 如果您未创建默认的PG版面，则定位该交易的任何版面将不会进行投标，除非它们设置正确。 您应始终创建默认的PG版面。 在[!UICONTROL Placements]视图中，默认PG位置的[!UICONTROL Sub-type]列值为“[!UICONTROL PG Default]”。

   您可以选择在附加版面中将交易用作库存目标，但必须正确设置交易才能进行竞价。

   1. 在[!UICONTROL Ad & Campaign Selection]设置中，选择要用于交易的广告：

      1. 选择广告商、营销活动和广告类型。

      1. 从可用广告列表中，选中将用于交易的每个广告旁边的复选框。

      1. 单击 **[!UICONTROL Apply]**.
   1. 在版面设置屏幕中：

      1. 输入版面名称。

      1. （可选）编辑[版面设置](/help/dsp/campaign-management/placements/placement-settings.md)，包括覆盖默认竞价，该默认竞价会自动填充交易的CPM值；更改日期范围；或附加更多广告。

      该交易会在库存目标部分中自动定位。 所有其他定位选项均不适用。

      1. 单击 **[!UICONTROL Create placement]**.



在创建交易后，您可以将该交易用作多个版面的库存目标。

>[!NOTE]
>
> 您无需将交易标记发送给发布者进行验证。

>[!TIP]
>
>* 在[!UICONTROL Inventory] > [!UICONTROL Deals]视图中， [!UICONTROL Pacing & Budget]列显示交易如何步调到指定的飞行日期和展示目标。
>
>* 如果投放进度缓慢或过于紧张，请联系您的发布者以调整通过交易发送的量。


>[!MORELIKETHIS]
>
>* [手动交易ID设置](deal-id-settings.md)
>* [设置程序化保证交易](programmatic-guaranteed-set-up.md)
>* [为程序化保证交易提交广告 [!DNL FreeWheel]](freewheel-submit.md)
>* [关于程序化保证交易](programmatic-guaranteed-about.md)

