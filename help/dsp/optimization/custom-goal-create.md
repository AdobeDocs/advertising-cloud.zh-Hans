---
title: 创建自定义目标
description: 创建自定义目标
feature: Optimization
exl-id: 440ded21-92d3-41ad-839f-ebc8376aa932
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 创建自定义目标

>[!TIP]
>
>有关如何配置自定义目标的提示，请参阅创建自定义目标的[最佳实践](custom-goal-best-practices.md)。

1. 登录Advertising Cloud Search（美国公司）[`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com)或（所有其他国家/地区的公司）[`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com)。
1. 确保您要包含在目标中的量度已被跟踪，在产品中可用，并包含显示名称：
   1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Transaction Properties]**。
   1. 找到量度，并确保为该量度启用了&#x200B;**[!UICONTROL Show in UI and Reports]**。
   1. 如果量度在&#x200B;**[!UICONTROL Display Name]**&#x200B;列中没有值，请单击单元格，输入显示名称，然后单击&#x200B;**[!UICONTROL Apply]。**
1. 将自定义目标创建为&#x200B;*objective*:
   1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]> [!UICONTROL Optimization] >[!UICONTROL Objectives]**。
   1. 在工具栏中，单击&#x200B;**[!UICONTROL Create objective]。**
   1. 输入目标设置：
      1. 在&#x200B;**[!UICONTROL Change Objective Name]**&#x200B;字段中，输入目标名称。

         目标名称将显示在Advertising Cloud DSP包设置的[!UICONTROL Custom Goals]列表中。

      1. 将资产与目标关联：

         >[!NOTE]
         >
         > 默认情况下，为广告商跟踪的所有事务属性都会列在[!UICONTROL Available Properties]列表中。

         * 要导入包含属性及其权重的CSV文件，请单击&#x200B;**[!UICONTROL Import]**，然后找到要导入的文件。

            广告商必须已存在导入的资产；这些名字不区分大小写。

            导入的属性将替换指定的任何现有属性。

         * 要手动指定具有默认权重(1)的第一个属性，请从为广告商跟踪的所有交易属性列表中选择。

         * 要手动添加其默认权重为(1)的属性，请单击&#x200B;**[!UICONTROL +]** 。

            >[!TIP]
            >
            > 要在列表中搜索属性，请在属性名称中的任意位置输入字符串。

         * 要手动添加多个属性，请单击&#x200B;**[!UICONTROL Add Multiple Properties]。** 对于要添加的每个资产，单击列中的资产 [!UICONTROL Available Properties] 名称，然后将其拖动到 [!UICONTROL Added Properties] 列中。添加完资产后，单击&#x200B;**[!UICONTROL Add]**。

            >[!TIP]
            >
            >* 要在列表中搜索属性，请在输入字段的属性名称的任意位置输入字符串。
            >* 要过滤列表以排除报表中排除的属性，请选择选项&#x200B;**[!UICONTROL Hide properties excluded from reports]。**


         * （当目标包含多个属性时）要更改属性相对于目标中其他属性的权重，请在&#x200B;**[!UICONTROL Weight]**&#x200B;字段中输入值。
      1. 在设置的底部，单击&#x200B;**[!UICONTROL Save]**。


创建目标后，当优化目标为“[!UICONTROL Highest ROAS - Custom Goal]”或“[!UICONTROL Lowest CPA - Custom Goal]”时，可以将其分配给Advertising Cloud DSP包作为自定义目标。

>[!TIP]
>
>要优化<!-- optimum? Or optimization won't happen at all w/out it? -->性能，自定义目标（目标）中的组合量度每天必须至少进行10次转化。 如果不支持，最佳做法是向目标中添加其他支持事件（交易属性），例如产品页面或应用程序启动。 有关准则，请参阅[构建自定义目标的最佳实践](custom-goal-best-practices.md)。

>[!MORELIKETHIS]
>
>* [关于自定义目标](custom-goal-about.md)
>* [构建自定义目标的最佳实践](custom-goal-best-practices.md)
>* [优化目标及其使用方法](optimization-goals.md)
>* [包设置](/help/dsp/campaign-management/packages/package-settings.md)
> * [DSP如何优化您的营销活动](optimization-how-dsp-optimizes-campaigns.md)

