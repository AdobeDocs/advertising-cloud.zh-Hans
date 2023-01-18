---
title: 编辑可重用受众
description: 了解如何编辑可重复使用的受众。
feature: DSP Audiences
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# 编辑可重用受众

在您编辑在任何版面或其他可重复使用受众中使用的受众时，所做的更改会立即应用于这些版面和受众。<!-- verify -->

1. 在主菜单中，单击 **[!UICONTROL Audiences]>[!UICONTROL All audiences]**.

1. 将光标悬停在受众行上并单击 **[!UICONTROL Edit]**.

1. 通过以下任一方式编辑受众设置：

   >[!NOTE]
   >
   >如果您编辑受众区段逻辑，请详细 [受众大小数据](audience-about.md) 在右侧面板中更新。

   * （可选）要编辑 **[!UICONTROL Audience Name]** 单击 ![编辑](/help/dsp/assets/edit.png) 在受众名称旁边，输入唯一的受众名称，然后单击 **[!UICONTROL Apply]**.

   * （可选）要使用 [[!UICONTROL Third Party Segments], [!UICONTROL First Party Segments], [!UICONTROL Adobe Segments], [!UICONTROL Custom Segments]和 [!UICONTROL Saved Audiences] 选项卡](audience-settings.md)，请执行以下操作。

      * 要将区段添加到现有区段组，请执行以下操作：
      1. 单击右侧面板中的区段组。

      1. （可选）将组逻辑更改为 *[!UICONTROL Include Any]*, *[!UICONTROL Include All]*&#x200B;或 *[!UICONTROL Exclude All]*，根据需要。

         *[!UICONTROL Exclude All]* 不适用于第一个区段组。 对于仅包含排除项的受众，将此受众构建为 *[!UICONTROL Include Any]* 然后，在版面中，从“排除的受众”菜单中选择该受众。

      1. 在左侧面板中找到新区段，然后选中区段名称旁边的复选框。

         区段组会自动更新为新区段。
   * 要添加新区段组，请执行以下操作：

      1. 单击 **[!UICONTROL + New Group]** 中。

      1. （可选）将上一组和新组之间的逻辑更改为 *[!UICONTROL And]* 或 *[!UICONTROL Or]*，根据需要。

      1. 在左侧面板中找到新组的区段，并选中区段名称旁边的复选框。

      1. （可选）将组逻辑更改为 *[!UICONTROL Include Any]*, *[!UICONTROL Include All]*&#x200B;或 *[!UICONTROL Exclude All]*，根据需要。
   * 要使用现有受众的区段逻辑，请执行以下操作：

      1. 通过以下任一方式从现有受众复制区段逻辑：

         * 在“所有受众”视图中，将光标悬停在受众行上，然后单击 **[!UICONTROL More]>[!UICONTROL Copy to Clipboard]**.

         * 在现有受众的设置中，在区段逻辑面板顶部，单击 **[!UICONTROL More]>[!UICONTROL Copy to Clipboard]**.

         * 在文本编辑器中，使用字母数字区段ID和 [布尔语法](audience-segment-logic-syntax.md)，然后将其复制到剪贴板。
      1. 单击 **[!UICONTROL paste in an audience rule to begin building]**，将现有区段逻辑粘贴到输入字段中，然后单击 **[!UICONTROL Apply]**.

         >[!NOTE]
         >
         >如果受众已包含任何区段逻辑，则在新区段逻辑中粘贴将覆盖现有逻辑。





1. 单击 **[!UICONTROL Save]**.

1. 在确认消息中，单击 **[!UICONTROL Continue]**.

>[!MORELIKETHIS]
>
>* [关于受众管理](audience-about.md)
>* [创建可重用受众](reusable-audience-create.md)
>* [复制可重用受众](reusable-audience-duplicate.md)
>* [查看有关可重用受众的详细信息](reusable-audience-view-details.md)
>* [共享可重用受众](reusable-audience-share.md)
>* [导出可重复使用的受众](reusable-audience-export.md)
>* [将可重复使用受众的区段键复制到剪贴板](reusable-audience-clipboard.md)
>* [删除可重用受众](reusable-audience-delete.md)
>* [受众设置](audience-settings.md)
>* [受众区段逻辑的语法](audience-segment-logic-syntax.md)
>* [可用的第三方数据提供商](third-party-data-providers.md)

