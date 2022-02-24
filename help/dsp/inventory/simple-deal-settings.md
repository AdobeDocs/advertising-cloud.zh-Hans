---
title: '"[!UICONTROL Simple Ad Serving] 交易设置”'
description: 了解 [!UICONTROL Simple Ad Serving] 交易。
feature: DSP Simple Ad Serving
source-git-commit: 2c94b6c02b4e24878639dd9edbc0455e1751f679
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 0%

---

# [!UICONTROL Simple Ad Serving] 交易设置

## 新建 [!UICONTROL Simple Ad Serving] 交易

### [!UICONTROL Select Ad Source]

| 参数 | 描述 |
|-----------|-------------|
| **[!UICONTROL Serving Type]** | 此交易的媒体类型： *[!UICONTROL Video],* *[!UICONTROL Display],* 或 *[!UICONTROL Audio].* |
| **[!UICONTROL Publisher Site Served On]** | 销售此库存的发布者的名称。 通过在名称中至少输入前两个字符来搜索发布者。 要添加未列出的发布者，请与 [!DNL Adobe] 客户团队。 |
| **[!UICONTROL Advertiser]** | 帐户中可访问此交易的单个广告商。 另外，选择可用交易的促销活动和（可选）包。 |
| **[!UICONTROL Media Quality Assessment?]** | （某些用户）允许广告在其他DSP上运行以进行第三方验证。 <!-- Who can select this? It's disabled for me. Need to see if there are additional fields when this is enabled. --> |
| **[!UICONTROL Ad Source]** | 唯一的选项是 *[!UICONTROL Site Serve (Event Pixels)]*. |
| **[!UICONTROL Ad Creation]** | （仅限新交易）是否：<ul><li>*[!UICONTROL Create New]:* 为此交易创建广告。</li><li>*[!UICONTROL Select Ads]:* 用于此交易的现有广告。</li></ul> |
| **[!UICONTROL Ad Type]** | 此交易的广告类型。 如果您要为交易创建新广告，请根据请求包括广告大小或持续时间。 可用选项因介质类型而异。 |

{style=&quot;table-layout:auto&quot;}

### [!UICONTROL Select Ad(s)]

（当您使用现有广告时）要包含在交易中的广告。 选中要包含的每个广告旁边的复选框。

### [!UICONTROL Select & Upload [Media Type]]

（仅限新广告）用于创建新广告的屏幕 [第一方广告](/help/dsp/campaign-management/ads/ad-create.md) 或 [第三方广告](/help/dsp/campaign-management/ads/ad-create-third-party.md).

### [!UICONTROL Feed Details]

| 参数 | 描述 |
|-----------|-------------|
| **[!UICONTROL Media CPM]** | 每千次展示次数成本(CPM)，反映在合同的费率卡中。 联系您的 [!DNL Adobe] 帐户团队获取此值。 <br><br>还指定交易的货币。 所有用户都可以选择USD，或者，如果SSP支持其他货币，则选择DSP帐户的货币。 |
| **[!UICONTROL Third Party Billed Fees]** | （可选）要作为不可计费成本和交易币种进行跟踪的静态第三方费用。<br><br>所有用户都可以选择USD，或者，如果SSP支持其他货币，则选择DSP帐户的货币。 **注意：** 计费费用反映在 [!UICONTROL Net CPM] 量度。 |
| **[!UICONTROL Third Party Fee Description]** | （可选）第三方费用的描述。 |
| **[!UICONTROL Flight Dates]** | 使用此交易的流量的开始和结束日期。 投放日期必须包含在营销活动投放日期中。 广告标记仅在指定的投放期间返回响应。<br><br> 创建持续时间为一年的单独简单广告服务促销活动并在其中构建跟踪像素的最佳实践。 |
| **[!UICONTROL Impressions]** | （可选）使用此交易预计要运行的预计展示次数。 此值仅用于跟踪目的，用于在满足交付目标时标记；发布者可控制实际的广告投放。 最佳做法是输入大量展示次数，以在DSP中保持标记的活动状态，以便在需要时可以续订或延长标记。 |
| **[!UICONTROL Deal Name]** | 交易名。 输入名称，或选择 *[!UICONTROL Auto Generate Deal Name]* 以便DSP根据交易详细信息生成名称。<br><br>自动生成的名称示例： `Campaign-desktop_video_preroll_15-24Kitchen-$10_USD-jdoe-SAS` |
| **[!UICONTROL Attached Ads]** | （只读）交易中包含的广告。 要编辑广告，请单击广告名称。 要从交易中删除广告，请单击 **[!UICONTROL X]** 广告名称旁边。 |

{style=&quot;table-layout:auto&quot;}

<!-- 
## Existing Simple Ad Serving Deals

Changes aren't applied retroactively.
-->

<!-- completely different settings layout, so need a separate section for them -->

<!-- From Abhinav: Editable fields are Name, Start & End date, Impressions & CPM. Changes are not applied retroactively.

But I see:

| Parameter | Description |
|-----------|-------------|

| **[!UICONTROL Are you using Deal ID?] | (Read-only) Whether the deal was set up as a [!UICONTROL Deal ID] (*[!DNL Yes]*)  or a [!UICONTROL Simple Ad Serving] deal (*[!DNL No]*). |
| **[!UICONTROL Inventory Type] | (Read-only) The inventory type for the deal. |
| **[!UICONTROL Feed Name] | The name of the [!UICONTROL Simple Ad Serving] deal. |
| **[!UICONTROL Publisher Ad Server] | (Read-only)  |
| **[!UICONTROL Publisher maximum ad length] | The maximum length of the ad, per the publisher. |
| **[!UICONTROL Publisher minimum ad length] | The minimum length of the ad, per the publisher. |
| **[!UICONTROL Fill Type] | (Read-only)  |
| **[!UICONTROL Contracted CPM] | This field is required if billing through TubeMogul, but enter your CPM in this field to track your actual spend. |
| **[!UICONTROL 3rd party technology CPM] | (Optional)  |
| **[!UICONTROL Planned Flight Dates] | The beginning and end dates for the deal flight. These dates don't control ad delivery but are used to track delivery pacing. **THIS IS CONTRARY TO WHAT THE NEW DEAL SETTINGS ABOVE, FROM ABHINAV, SAY**> |
| **[!UICONTROL Target Impressions] | (Optional) The estimated number of impressions you expect to run using this deal. This value is used for tracking purposes only and to flag when delivery goals are met; the publisher controls actual ad delivery. The best practice is to enter a high number of impressions to keep the tag active within DSP so it can be renewed or extended if needed. |
 -->

>[!MORELIKETHIS]
>
>* [关于 [!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [创建 [!UICONTROL Simple Ad Serving] 交易](simple-deal-create.md)
>* [查看事件跟踪像素 [!UICONTROL Simple Ad Serving] 交易](simple-deal-show-pixels.md)

