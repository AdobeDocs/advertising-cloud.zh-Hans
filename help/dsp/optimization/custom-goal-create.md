---
title: 创建自定义目标
description: 创建自定义目标
feature: DSP Optimization
exl-id: 440ded21-92d3-41ad-839f-ebc8376aa932
source-git-commit: 8aea9eb1358e23a5b25e0353ced80c1550fa0057
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 0%

---

# 创建自定义目标

您可以将自定义目标创建为 *目标* 在Advertising Cloud Search。

要创建自定义目标，Advertising Cloud DSP帐户必须关联到 [!DNL Search] 帐户中具有相同的Adobe Experience Cloud组织ID [!DNL Search] 客户端设置。 如果您的DSP帐户未关联到 [!DNL Search] 帐户，联系 [!DNL Adobe] 客户团队。

>[!TIP]
>
>请参阅 [创建自定义目标的最佳实践](custom-goal-best-practices.md) 以获取有关如何配置自定义目标的提示。

1. 登录Advertising Cloud Search（美国公司） [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) 或（所有其他国家/地区的公司） [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com).
1. 确保您要包含在目标中的量度已被跟踪，在产品中可用，并包含显示名称：
   1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Transaction Properties]**.
   1. 找到量度，并确保 **[!UICONTROL Show in UI and Reports]** 为量度启用。
   1. 如果量度在 **[!UICONTROL Display Name]** 列中，单击单元格，输入显示名称，然后单击 **[!UICONTROL Apply].**
1. 将自定义目标创建为 *目标*:
   1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Optimization] >[!UICONTROL Objectives]**.
   1. 在工具栏中，单击 **[!UICONTROL Create objective].**
   1. 输入目标设置：
      1. 在 **[!UICONTROL Change Objective Name]** 字段，输入目标名称。

         目标名称将显示在 [!UICONTROL Custom Goals] 列表。

      1. 将资产与目标关联：

         >[!NOTE]
         >
         > 默认情况下，为广告商跟踪的所有交易属性都会列在 [!UICONTROL Available Properties] 列表。

         * 要导入包含属性及其权重的CSV文件，请单击 **[!UICONTROL Import]** 并找到要导入的文件。

            广告商必须已存在导入的资产；这些名字不区分大小写。

            导入的属性将替换指定的任何现有属性。

         * 要手动指定具有默认权重(1)的第一个属性，请从为广告商跟踪的所有交易属性列表中进行选择。

         * 要手动添加其默认权重为(1)的属性，请单击 **[!UICONTROL +]** .

            >[!TIP]
            >
            > 要在列表中搜索属性，请在属性名称中的任意位置输入字符串。

         * 要手动添加多个属性，请单击 **[!UICONTROL Add Multiple Properties].** 对于要添加的每个资产，单击 [!UICONTROL Available Properties] 列，并将其拖入 [!UICONTROL Added Properties] 列。 添加完资产后，单击 **[!UICONTROL Add]**.

            >[!TIP]
            >
            >* 要在列表中搜索属性，请在输入字段的属性名称的任意位置输入字符串。
            >* 要过滤列表以排除报表中排除的属性，请选择选项 **[!UICONTROL Hide properties excluded from reports].**


         * （当目标包含多个属性时）要更改某个属性相对于目标中其他属性的权重，请在 **[!UICONTROL Weight]** 字段。
      1. 在设置的底部，单击 **[!UICONTROL Save]**.


创建目标后，当优化目标为“ ”时，您可以将其分配给Advertising Cloud DSP包作为自定义目标[!UICONTROL Highest ROAS - Custom Goal]&quot;或&quot;[!UICONTROL Lowest CPA - Custom Goal].&quot;

>[!TIP]
>
>要获得最佳性能，自定义目标（目标）中的组合量度每天必须至少进行十次转化。 如果不支持，最佳做法是向目标中添加其他支持事件（交易属性），例如产品页面或应用程序启动。 请参阅 [构建自定义目标的最佳实践](custom-goal-best-practices.md) 以了解准则。

>[!MORELIKETHIS]
>
>* [关于自定义目标](custom-goal-about.md)
>* [构建自定义目标的最佳实践](custom-goal-best-practices.md)
>* [优化目标及其使用方法](optimization-goals.md)
>* [包设置](/help/dsp/campaign-management/packages/package-settings.md)
> * [DSP如何优化您的营销活动](optimization-how-dsp-optimizes-campaigns.md)

