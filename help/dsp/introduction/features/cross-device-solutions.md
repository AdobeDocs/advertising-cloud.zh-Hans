---
title: 跨设备解决方案
description: 进一步了解跨设备功能。
feature: DSP Introduction
exl-id: 29f8ec41-35a6-4a29-a638-82a2929a8fe6
source-git-commit: e0713f3717a684fb5ef2808d7de769424b8972d2
workflow-type: tm+mt
source-wordcount: '1110'
ht-degree: 0%

---

# 跨设备解决方案

Advertising Cloud DSP集成 [!DNL LiveRamp] 和 [!DNL Adobe Device Co-op] 允许您将受众扩展到用户的所有已知设备，而不仅仅是品牌跟踪的设备。 这些集成还提供跨所有设备的频率上限和归因测量。

使用受支持的基于人员的设备图时，您可以：

* 跨渠道和设备匹配受众，以向人员和家庭（而不是设备）投放广告。
* 通过了解和限制个人的频度来平衡和暴露。
* 测试跨渠道或设备展示受众与转化受众的策略。

## 每个设备图的优势

* [!DNL Adobe Device Co-op]:
   * 提供参与Adobe广告商的确定性和可能性数据的选择加入池
   * 提供由桌面和移动Web访客提供支持的强大Cookie ID连接
   * 包括主要来自美国和加拿大的数据
   * 无使用费

* [!DNL LiveRamp] 设备图：
   * 提供确定性数据池，包括离线客户数据
   * 在Cookie ID和移动设备ID之间提供均匀的覆盖范围
   * 包括主要来自美国的数据
   * 免费进行频度上限和归因测量
   * 延长展示次数(仅通过使用 [!DNL LiveRamp] 设备图，而不是目标受众区段内的设备图)

      费率会反映在您的帐户费率卡上。

## 基于人员的频率管理

基于人员的频率管理允许您在人员级别指定频率上限，而不是设备级别，以便真正控制媒体曝光。

### 激活基于人员的频率管理

* **营销活动：** 创建新营销活动时，您可以指定 [!UICONTROL Cross-Device Level] 设置。 启用“[!UICONTROL Same Device]&quot; -> &quot;[!UICONTROL People]，然后选择一个设备图。 指定的设备图既可用于位置级别的跨设备定位，也可用于营销策划、包和位置级别的基于人员的频率管理。 频率上限适用于人员的所有已知设备。

有关更多信息，请参阅 [营销活动设置](/help/dsp/campaign-management/campaigns/campaign-settings.md).

保存营销活动后，便无法更改其 [!UICONTROL Cross Device Level] 设置。

* **包：**  您可以选择在资源包级别设置附加频率上限。 DSP将遵循营销活动层级中最严格的频率上限。

* **版面：** 您可以选择在放置级别设置附加频率上限。 DSP将遵循营销活动层级中最严格的频率上限。

## 基于人员的定位

通过基于人员的定位，您可以在桌面和移动设备上找到客户。

### 激活基于人员的定位

* **营销活动：** 创建新营销活动时，您可以指定 [!UICONTROL Cross-Device Level] 设置。 启用“[!UICONTROL Same Device]&quot; -> &quot;[!UICONTROL People]，然后选择一个设备图。 指定的设备图用于在放置级别跨设备定位和基于人员的频率管理。

有关更多信息，请参阅 [营销活动设置](/help/dsp/campaign-management/campaigns/campaign-settings.md).

* **版面：** 在具有指定设备图的营销活动中为版面选择受众目标时， [!UICONTROL Cross-Device Targeting] 选项允许您扩展定位到人员所有已知设备（根据促销活动设置中指定的设备图），甚至是不在指定区段的设备。

### 设置基于人员的定位报表

您可以在自定义报表中包含以下量度：

* **延长展示次数：** (在 [!UICONTROL Build Your Report] 部分 [!UICONTROL Metrics] > [!UICONTROL Std. Metrics])利用设备图（在原始受众区段中未找到）交付的增量展示次数量。 此量度还用于计算与使用第三方设备图相关的适用费用。

   要确定某个时段内的延长展示次数的成本，请运行一个包含 [!UICONTROL Extended Impressions] 列，然后将扩展展示次数总数乘以0.00035美元(0.35/1000展示次数)。

   综合成本亦计入综合 [!UICONTROL Billable Other Net Spend] 列（下） [!UICONTROL Metrics] > [!UICONTROL Spend])，但该量度也包含您可能添加的其他促销活动费用。

* **设备图：** (在 [!UICONTROL Build Your Report] 部分 [!UICONTROL Dimensions] > [!UICONTROL Campaign])特定促销活动、包或版面的选定设备图。

## 基于人员的归因测量

*仅具有Advertising Cloud转化跟踪的广告商*

通过基于人员的归因，您可以将发生在媒体曝光设备以外的设备上的转化归因。 基于人员的归因测量可在DSP、Advertising Cloud Search和Advertising Cloud Creative中提供，供在其网站上实施了Advertising Cloud转化像素的广告商使用。

### 启用基于人员的归因测量

如果要激活跨设备归因测量，请联系您的 [!DNL Adobe] 客户经理。 对于 [!DNL Adobe Device Co-op] 帐户，您需要提供您的已签名 [!DNL Adobe Device Co-op] 合同和Experience Cloud [!DNL Organization ID] (以前称为 [!DNL IMS org ID])。

要查看广告商帐户是否配置为使用设备图进行归因测量，请执行以下操作：

1. 在主菜单中，单击 **[!UICONTROL Settings]>[!UICONTROL Advertiser]**.
1. 将光标悬停在广告商行上并单击 **[!UICONTROL Edit]**.
1. 在 [!UICONTROL Integrations] 广告商设置的部分，查看 [!UICONTROL Cross-Device Attribution] 设置处于活动状态。

   对于活动集成，会显示设备图。

### 设置跨设备转化归因的转化报表

#### 转化报表设置

启用设备图进行归因测量后， [!UICONTROL Conversion] 报表包含 [!UICONTROL Cross-Device Breakout] 设置，以便您为每个转化量度最多包含三个单独的列，包括：

* &lt;*转化*>[!UICONTROL (tp)]:包括总转化（总人员），其中包括相同设备转化和跨设备转化（如果适用）。 在报表中， &quot;[!UICONTROL (tp)]“ ”会附加到转化路径中的转化量度名称、规则类型和转化类型(例如“响应(le)(tl)(tp)”)。

* &lt;*转化*>[!UICONTROL (sd)]:（可选）仅包括转化路径中仅跟踪了单个设备的转化。 在报表中， &quot;[!UICONTROL (sd)]“ ”会附加到转化路径中的转化量度名称、规则类型和转化类型(例如“响应(le)(tl)(sd)”)。

* &lt;*转化*>[!UICONTROL (xd)]:（可选）仅包括转化路径中跟踪了多个设备的转化。 在报表中， &quot;[!UICONTROL (xd)]“ ”会附加到转化路径中的转化量度名称、规则类型和转化类型(例如“响应(le)(tl)(xd)”)。

#### 如何解释转化报表

如果您对跨设备转化总数的百分比([!UICONTROL (xd)]/[!UICONTROL (tl)])从高到低，您将了解什么因素促成了高于平均的跨设备转化。 您可以使用此信息来告知您的创意或定位策略，以便将消息传递和渠道投资与用户行为相匹配。

* 包 — 查看哪些包促成的总转化最多，以及哪些包在跨设备转化中的百分比较高。 这有助于您了解在何处集中支出。

* 版面 — 比较版面效果和归因（例如，移动Web广告可能会在桌面上促进转化）。 如果没有设备图进行归因，您可能会错过移动Web版面对桌面转化的影响，或者如果大多数用户在桌面而不是移动Web上进行转化，则该图版可能会被掩盖。

* 广告 — 发现哪些广告可提高转化率，并量化它们在Web浏览器和移动设备应用程序环境中的价值和影响。

* 网站 — 跨网站优化，而不是手动完全排除网站。 如果网站驱动跨设备转化，则可以查看发生此行为的设备。

* 交易 — 通过验证哪些库存交易提供了跨设备转化，然后确定是否应扩大目标以在这些交易中包含更多设备和渠道，来改进手动优化。

>[!MORELIKETHIS]
>
>* [报表设置](/help/dsp/reports/report-settings.md)
>* [营销活动设置](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [包设置](/help/dsp/campaign-management/packages/package-settings.md)
>* [版面设置](/help/dsp/campaign-management/placements/placement-settings.md)

