---
title: 创建可重用受众
description: 了解如何创建由受众区段和其他已保存受众组成的可重复使用受众。
feature: DSP Audiences
exl-id: 48e3dc4c-6e2d-452c-8d69-7e6211d808e0
source-git-commit: 37e5a4fbb7e2ccda77ab0afd49054ec4d1dabf76
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---

# 创建可重用受众

<!-- "Saved audience" is used in UI (where?), but "saved" is a state, not a type. "Reusable audience" sounds better in a description. "Audience template" isn't right, either, since it implies you can edit it on the fly to create a new, different audience. Some other term? -->

您可以保存和管理可重复使用的受众，这些受众是受众区段组，甚至是其他已保存的受众，您可以将这些受众用作多个版面的目标或排除项。

1. 在主菜单中，单击 **[!UICONTROL Audiences]>[!UICONTROL All Audiences]**.

1. 在数据表上方，单击 **[!UICONTROL Create]**.

1. 输入唯一 [!UICONTROL Audience Name].

1. （可选）取消选择选项以 **[!UICONTROL Share with all advertisers in my account]**.

   当您共享受众时，该受众将作为目标提供，或者对帐户中的所有广告商不包含该受众。 但是，受众中的各个区段仅适用于共享了区段的用户。 例如，如果您与未映射到该区段的广告商共享包含Adobe Analytics区段的受众 [!DNL Analytics] 帐户，则该区段将不会在该广告商的受众中预览。 只有该广告商可用的区段才会在受众中进行预览。

1. 单击 **[!UICONTROL Save]**.

1. 构建受众：

   >[!NOTE]
   >
   >在构建受众时，请详细 [受众大小数据](audience-about.md) 在右侧面板中更新

   * 要使用 [[!UICONTROL Third Party Segments], [!UICONTROL First Party Segments], [!UICONTROL Adobe Segments], [!UICONTROL Custom Segments]和 [!UICONTROL Saved Audiences] 选项卡](audience-settings.md)，请执行以下操作。

      * 要添加第一个区段，请在左侧面板中找到该区段，然后选中区段名称旁边的复选框。

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




1. 单击 **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [关于受众管理](audience-about.md)
>* [受众设置](audience-settings.md)
>* [受众区段逻辑的语法](audience-segment-logic-syntax.md)
>* [可用的第三方数据提供商](third-party-data-providers.md)
>* [创建和实施自定义区段](custom-segment-create.md)
>* [创建和实施 [!UICONTROL CCPA Opt-Out-of-Sale] 区段](ccpa-opt-out-segment-create.md)
>* [版面设置](/help/dsp/campaign-management/placements/placement-settings.md)

