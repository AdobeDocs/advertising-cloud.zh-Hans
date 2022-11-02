---
title: 从Advertising Cloud DSP促销活动中收集点击和展示数据
description: 了解如何使用Audience Manager像素从Advertising Cloud DSP广告中捕获基于Cookie的展示和点击事件
feature: Integration with Adobe Audience Manager
exl-id: eb717148-00ab-428a-97b9-e8396a5c47b0
source-git-commit: 8de057df8bf2b67f20a915e6e711902f11176747
workflow-type: tm+mt
source-wordcount: '1062'
ht-degree: 0%

---

# 从Advertising Cloud DSP促销活动中收集媒体曝光数据

*仅使用Advertising Cloud DSP的广告商*

*仅具有Advertising Cloud-Adobe Audience Manager集成的广告商*

本文档介绍如何标记Advertising Cloud DSP广告，以使用Audience Manager像素捕获基于Cookie的展示和点击事件，以及使用数据所需的其他任务。

事件像素不会捕获在无Cookie环境(如移动设备应用程序和连接的电视(CTV))中发生的事件。

## 步骤1:在Audience Manager中设置数据源 {#set-up-data-source}

在Audience Manager中，创建 [数据源](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html) ，然后单击数据。 包括数据源ID [在每个事件标记中](#implement-dsp-pixels) 以便所有跟踪事件都归因于数据源。

>[!NOTE]
> 可以在单个数据源中收集在多个DSP上运行的广告促销活动的所有展示和点击数据。

## 步骤2:在网页上实施展示和点击事件像素 {#implement-dsp-pixels}

广告商可以为自己的品牌创建和实施事件标记。 如有必要，请联系您的Adobe Audience Manager顾问或 [!DNL Adobe] 客户经理以寻求支持。

>[!NOTE]
>
>如果贵组织使用 [!DNL Analytics] 跟踪，则您可能不需要Audience Manager点击跟踪。 Adobe Analytics会捕获点击信号，并可以将其发送到Audience Manager [服务器端转发](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

### 像素语法

事件像素必须包括以下参数。

**展示次数跟踪像素：**

`[Audience Manager customer domain].demdex.net/event?d_event=imp&d_src=[source id]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

with [可选的其他参数](#parameters) 前缀为 `&`

**点击跟踪像素：**

`[Audience Manager customer domain].demdex.net/event?d_event=click&d_src=[source id]&d_rd=[redirect URL]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

with [可选的其他参数](#parameters) 前缀为 `&`

其中：

* `[Audience Manager customer domain]` 是将展示或单击事件发送到的域名 [!DNL Adobe].

* `[source id]` 是 [数据源](#set-up-data-source) 在中，您将跟踪DSP展示次数并单击数据。

* `[redirect URL]` 是双重编码的重定向URL。 如果您使用在线编码工具(如www.urlencoder.org)，则通过编码器运行字符串并重新编码结果。

* `${TM_CAMPAIGN_ID_NUM}` 是DSP中的数值促销活动ID。 如果要硬编码单个促销活动ID而不是使用DSP宏，请在促销活动设置中找到该ID。

* 每个 [参数](#key-value-pairs) 前缀为 `&` 和的格式 `d_parameter=parameter_id`，其中 `parameter` 将替换为新字段的键值对。 示例： `&d_placement=${TM_PLACEMENT_ID_NUM}`

### 键值对的参数 {#parameters}

**格式：**  `d_parameter=parameter_id`

    其中：
    
    *参数前缀为“&amp;”
    
    *“parameter”将替换为新字段的键值对
    
    示例：&#39;&amp;d_placement=${TM_PLACEMENT_ID_NUM}&#39;

这两种类型的像素可以包含其他参数，如 *键值对* 为其他报表收集特征或提供营销活动元数据（如版面名称或营销活动名称）。 键值对由两个相关元素组成：a *key*，它是定义数据集的常量，以及 *值*，属于集的变量。

在键值对中，值变量可以是硬编码ID，也可以是 *宏*，这是一小块自包含代码，在加载广告标记以用于促销活动和用户跟踪时，会将其动态替换为相应值。 对于与促销活动相关的参数，您可以使用 [DSP宏](/help/dsp/campaign-management/macros.md) 使用单个像素在所有广告中发送促销活动属性，而不是Audience Manager宏，将促销活动属性与相应展示次数或点击数据一起发送到Audience Manager。 插入到事件像素中的DSP宏必须是包含在像素中的键值对的合适值。 例如，对于 `d_placement` 键，您将使用DSP宏 `${TM_PLACEMENT_ID_NUM}` 作为捕获由Advertising Cloud宏生成的版面ID的值。

有关Audience Manager支持展示事件像素的宏列表，请参阅[通过像素调用捕获营销活动展示数据](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html#supported-key-value-pairs).&quot;

有关Audience Manager支持点击事件像素的宏列表，请参阅[通过像素调用捕获营销活动点击数据](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/click-data-pixels.html).&quot;

>[!TIP]
>
>* 最佳实践是包含营销活动、版面、创意（广告）和网站ID，以便您可以使用营销活动属性创建Audience Manager特征。
>* 要创建Audience Optimization报表，需要其他参数。
>* 在键值对中，将这些值替换为 [DSP宏](/help/dsp/campaign-management/macros.md) 这样，您就可以在所有营销活动的所有广告中使用单个像素。 例如，更改 `d_campaign=[%campaignID%]`to `d_campaign=${TM_CAMPAIGN_ID_NUM}` 用于捕获由Advertising Cloud宏生成的促销活动ID。
>* 您可以根据需要使用硬编码值创建自己的参数。 示例： `d_DSP=AdCloud`


展示事件像素的示例：

`http://acme.demdex.net/event?d_event=imp&d_src=1052880&d_site=${TM_SITE_ID_NUM}&d_creative=${TM_AD_ID_NUM}&d_placement=${TM_FEED_ID_NUM}&d_campaign=${TM_CAMPAIGN_ID_NUM}&d_DSP=AdCloud&d_bust=${TM_RANDOM}`

### 添加像素的位置

#### 展示跟踪像素

在 [!DNL DSP] 营销活动。 您可以在以下任意位置执行此操作：

* 在放置级别，默认情况下，该级别会将像素应用于放置中的所有广告。 在位置设置的“跟踪”部分中，将像素添加到 [[!UICONTROL Event pixels] 字段](/help/dsp/campaign-management/placements/placement-settings.md).

* 在广告级别，它覆盖任何置入级别的事件像素。 在广告设置中， [在 [!UICONTROL Pixel] 选项卡](/help/dsp/campaign-management/ads/ad-edit.md).

* （对于第三方广告服务器上的广告）在广告服务器中的广告级别。

#### 点击跟踪像素

在广告服务器中，无论您通常插入广告的点进URL的位置，都应插入点击事件像素（附加编码URL）。

## 步骤3:实施后任务

实施事件标记后，数据将流入Audience Manager数据收集服务器。 在报表中使用数据之前，请先完成以下任务。

### 创建 [!DNL Amazon S3] 存储段和数据源

在您的数据上Audience Manager服务器后，您必须 [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3])存储段，然后是将所有像素数据发送到的数据源。 联系您的Audience Manager顾问或 [客户关怀](https://experienceleague.adobe.com/docs/audience-manager/user-guide/help-and-legal/help-legal-contact.html) 如果您需要支持。

### 创建Audience Manager特征和区段

您的事件数据将作为 [未使用的信号](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/interactive-and-overlap-reports/unused-signals.html). 手动创建 [基于规则的特征](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) ，然后创建 [区段](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segments-purpose.html) 使用这些特征，才能在报表中使用数据。

示例特征，用于填充向DSP中特定创作元素公开的用户级别数据：

1. 将事件标识为 `d_event = imp`.
1. 在DSP促销活动中识别创作ID，然后将其映射到特征，如 `d_creative=[Creative ID]`.

![特征创建屏幕](/help/dsp/assets/aa-trait.png)

>[!MORELIKETHIS]
>
>* [Advertising Cloud DSP宏](/help/dsp/campaign-management/macros.md)
>* [将DSP媒体曝光数据发送到Adobe Audience Manager概述](overview.md)
>* [用例](use-cases.md)

