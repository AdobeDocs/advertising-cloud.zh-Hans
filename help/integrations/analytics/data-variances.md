---
title: 之间的预期数据差异 [!DNL Analytics] 和Adobe广告
description: 之间的预期数据差异 [!DNL Analytics] 和Adobe广告
feature: Integration with Adobe Analytics
exl-id: 34685e04-d4f9-4e27-b83e-b56164244b2b
source-git-commit: ad4ab8b9b0a4b5b1cc4aab540900363d2fe671c2
workflow-type: tm+mt
source-wordcount: '3278'
ht-degree: 0%

---

# 之间的预期数据差异 [!DNL Analytics] 和Adobe广告

*仅具有Adobe广告与Adobe Analytics集成的广告商*

具有 [!DNL Analytics for Advertising] <!-- (A4AdC) --> 集成通过Adobe广告和Adobe Analytics跟踪付费广告。 当您通过多个系统跟踪媒体、营销活动和渠道时，来自不同系统的相同数据集很少会完全匹配。 本文档介绍您应如何期望通过Adobe广告传输的媒体数据与跟踪媒体的不同系统中的数据进行比较 [!DNL Analytics].

>[!NOTE]
>
>本文档重点介绍了AdobeAdvertising和Analytics，但许多关键点也可以转移到其他跟踪解决方案。

## 相似报表中的归因差异

### 可能不同的回顾窗口和归因模型

的 [!DNL Analytics for Advertising] 集成使用两个变量（eVar或rVars \[保留的eVars]\）来捕获 [EF ID和AMO ID](ids.md). 这些变量配置了单个回顾窗口（点进次数和显示到达次数归因的时间）和归因模型。 除非另有指定，否则变量会配置为与Adobe广告中默认的广告商级别点击回顾窗口和归因模型相匹配。

但是，回顾窗口和归因模型可以在Analytics（通过eVar）和Adobe广告中进行配置。 此外，在Adobe广告中，归因模型不仅可以在广告商级别（用于竞价优化）进行配置，还可以在单个数据视图和报表中（仅用于报告目的）进行配置。 例如，组织可能倾向于使用均匀分配归因模型进行优化，但将最近联系归因用于Advertising DSP或 [!DNL Advertising Search]. 更改归因模型会更改归因转化的数量。

如果在一个产品中修改了报表回顾窗口或归因模型，而在另一个产品中未修改，则每个系统的相同报表将显示不同的数据：

* **不同回顾时间范围导致的差异示例：**

   假设Adobe广告有60天的点击回顾窗口和 [!DNL Analytics] 具有30天的回顾窗口。 假设用户通过Adobe广告跟踪的广告访问网站，离开，然后在第45天返回并转化。 Adobe广告会将转化归因于初次访问，因为转化发生在60天的回顾窗口内。 [!DNL Analytics]但是，无法将转化归因于初始访问，因为转化发生在30天回顾窗口过期之后。 在此示例中，Adobe广告报告的转化次数高于 [!DNL Analytics] 会。

   ![在Adobe广告中归因但未归因的转化示例 [!DNL Analytics]](/help/integrations/assets/a4adc-lookback-example.png)

* **不同归因模型导致差异的示例：**

   假设用户在转化前与三个不同的Adobe广告交互，并以收入作为转化类型。 如果Adobe广告报表使用偶数分布模型进行归因，则它将在所有广告中平均分配收入。 如果 [!DNL Analytics] 但是，会使用最近联系归因模型，然后它会将收入归因于最后一个广告。 在以下示例中，Adobe广告将捕获的30美元收入归因于三个广告中的每个广告，即使是10美元，而 [!DNL Analytics] 将所有30美元的收入归因于用户看到的最后一个广告。 当您比较来自Adobe广告和 [!DNL Analytics]，您可能会看到归因差异的影响。

   ![不同Adobe应占收益广告及 [!DNL Analytics] 基于不同的归因模型](/help/integrations/assets/a4adc-attribution-example.png)

>[!IMPORTANT]
>
>最佳做法是在Adobe广告和 [!DNL Analytics]. 使用 [!DNL Adobe] 帐户团队以确定当前设置并保持配置同步。

这些相同概念适用于使用不同回顾窗口或归因模型的任何其他类似渠道。

#### 用于显示到达跟踪的不同回顾窗口 {#impression-lookback}

在Adobe广告中，归因基于点击次数和展示次数，您可以针对点击次数和展示次数配置不同的回顾窗口。 在 [!DNL Analytics]但是，归因基于点进次数和显示到达次数，并且您没有选项为点进次数和显示到达设置不同的归因窗口；跟踪每次开始的网站。 展示可能会在显示到达的同一天或多天前发生，这可能会影响归因窗口在每个系统中的开始位置。

通常，大多数直通式转化发生得非常快，以至于两个系统都归因点数。 但是，某些转化可能会在Adobe广告展示回顾窗口之外，但在 [!DNL Analytics] 回顾窗口；此类转化归因于 [!DNL Analytics] 但不能给Adobe广告留下印象。

在以下示例中，假设访客在第1天获得了一则广告，在第2天执行了一次浏览访问（即，访问了广告的登陆页面，而之前未点击广告），然后在第45天进行了转换。 在这种情况下，Adobe广告将在第1天至第14天（使用14天的回顾时间）跟踪用户， [!DNL Analytics] 将跟踪从第2天到第61天（使用60天回顾）的用户，并且第45天的转化将归因到内的广告 [!DNL Analytics] 但不在Adobe广告中。

![中显示到达转化归因的示例 [!DNL Analytics] 但不Adobe广告](/help/integrations/assets/a4adc-viewthrough-example.png)

导致差异的另一个原因是，在Adobe广告中，您可以为显示到达转化分配一个自定义 *显示到达权重* 相对于归因于基于点击的转化的权重。 默认的显示到达权重为40%，这意味着显示到达转化将被计为基于点击的转化值的40%。 [!DNL Analytics] 不提供此类显示到达转化的权重。 例如，捕获的100美元收入订单 [!DNL Analytics] 如果您使用默认的显示到达权重（差额为60美元），则在Adobe广告中将折现为40美元。

在比较Adobe广告和 [!DNL Analytics] 报表。

#### 可用的归因模型

| Adobe广告归因 | [!DNL Analytics] 归因 | eVar/rVar分配 |
|--- |--- |--- |
| [!UICONTROL Last Event] | [!UICONTROL Last Touch] | [!UICONTROL Most Recent] |
| [!UICONTROL First Event] | [!UICONTROL First Touch] | [!UICONTROL Original Value] |
| [!UICONTROL Weight First Event More] | n/a | n/a |
| [!UICONTROL Even Distribution] | [!UICONTROL Linear] | [!UICONTROL Linear]<br><br>不要使用* |
| [!UICONTROL Weight Last Event More] | n/a | n/a |
| [!UICONTROL U-Shaped] | [!UICONTROL U-Shaped] | n/a |
| n/a | [!UICONTROL J-Shaped] | n/a |
| n/a | [!UICONTROL Inverse-J] | n/a |
| n/a | [!UICONTROL Custom] | n/a |
| n/a | [!UICONTROL Participation] | n/a |
| n/a | [!UICONTROL Algorithmic] | n/a |

>[!NOTE]
>
>对于线性分配， [!DNL Analytics] 在单次访问中对所有eVar值均等地归因成功事件，因此在“访问”eVar过期时使用线性分配。 但是，对于广告而言，使用线性归因会导致分配不是真正的线性分配，并且会导致报告不理想。 例如，如果访客在三次单独访问中转化之前与三个广告交互，则只有在上次访问中看到的广告会归因于转化，而不是全部三个广告。
>
>此外，将转化分配切换到“线性”或从“线性”切换到“线性”会阻止显示历史数据，这可能会导致报表中数据陈述错误。 例如，线性分配可能会将收入划分为多个不同的eVar值。 如果将分配更改为“最近”，则100%的收入会与最近的单个值关联。 这种关联可能会导致您得出错误的结论。
>
>为防止混淆， [!DNL Analytics] 使历史数据在报表界面中不可用。 如果您将eVar更改回初始分配设置，则可以查看历史数据，不过您不应仅为了访问历史数据而更改eVar分配设置。 Adobe建议，在您要为已记录的eVar应用新的分配设置时，应使用新的eVar，而不是更改已具有大量历史数据的数据的分配设置。

查看 [!DNL Analytics] 归因模型及其定义 [https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html).

如果您已登录 [!DNL Search]，您可以在
[https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm](https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm).

#### Adobe广告中的事件日期归因

在Adobe广告中，您可以按关联的点击日期/事件日期（点击或展示事件的日期）或交易日期（转化日期）报告转化数据。 中不存在点击/事件日期报告的概念 [!DNL Analytics];跟踪的所有转化 [!DNL Analytics] 按交易日期报告。 因此，在Adobe广告和 [!DNL Analytics]. 例如，假设某位用户在1月1日点击了一则广告，并在1月5日进行了转化。 如果您在Adobe广告中按事件日期查看转化数据，则转化将在1月1日发生点击时报告。 在 [!DNL Analytics]，则会在1月5日报告相同的转换。

![归因于不同日期的转化示例](/help/integrations/assets/a4adc-conversions-based-on.png)

## 归因于 [!DNL Analytics Marketing Channels]

[[!DNL Analytics Marketing Channels] 报告](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html) 允许您配置规则，以便根据点击信息的不同方面来识别不同的营销渠道。 您可以跟踪Adobe广告跟踪的渠道([!UICONTROL Display Click Through], [!UICONTROL Display View Through]和 [!UICONTROL Paid Search])作为 [!DNL Marketing Channels] 使用 `ef_id` 查询字符串参数来标识渠道。 <!-- Move most of the above text to "Marketing Channels" chapter once it's created, and add link here. --> 但是，即使 [!DNL Marketing Channels] 报表可以跟踪Adobe广告渠道，因此数据可能因多种原因与Adobe广告报表不匹配。 有关更多信息，请参阅以下部分。

>[!NOTE]
>
> 以下核心概念还适用于涉及未在Adobe广告中跟踪的促销活动(例如 [`campaign`](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/campaign.html) 变量(也称为“跟踪代码”Dimension或“eVar0”)和自定义eVar跟踪。

### 中可能不同的归因模型 [!DNL Marketing Channels]

最多 [!DNL Marketing Channels] 报表的配置 [!UICONTROL Last Touch] 归因，其中检测到的最后一个营销渠道分配了100%的转化值。 对 [!DNL Marketing Channels] 报表和Adobe广告报表将导致归因转化中出现差异。

### 中可能不同的回顾窗口 [!DNL Marketing Channels]

的回顾窗口 [!DNL Marketing Channels] 可以自定义。 在Adobe广告中，可以配置点击回顾窗口，但固定的60天窗口很常见。 如果这两种产品使用不同的回顾窗口，您可能会发现数据差异。

### 中的不同渠道归因 [!DNL Marketing Channels]

Adobe广告报表仅捕获通过Adobe广告(通过付费搜索 [!DNL Advertising Search] 广告和显示)，而 [!DNL Marketing Channels] 报表可以跟踪所有数字渠道。 这可能会导致将转化归因到的渠道不一致。

例如，付费搜索和免费搜索渠道通常具有共生关系，其中每个渠道可相互协助。 的 [!DNL Marketing Channels] 报表会将一些转化归因到“Adobe广告”不会执行的免费搜索，因为它不会跟踪免费搜索。

另外，还可以考虑查看展示广告、点击付费搜索广告、点击电子邮件内部，然后下30美元订单的客户。 即使Adobe广告和 [!DNL Marketing Channels] 这两种方法都使用最近联系归因模型，则转化仍会以不同的方式归因到每个属性。 Adobe广告无权访问 [!UICONTROL Email] 渠道，因此它将对转化的付费搜索进行计数。 [!DNL Marketing Channels]但是，具有所有三个渠道的访问权限，因此将 [!UICONTROL Email] 中。

![Adobe广告中与 [!DNL Analytics Marketing Channels]](/help/integrations/assets/a4adc-channel-example.png)

有关量度可能不同原因的更多说明，请参阅[渠道数据为何会因Adobe广告和 [!DNL Marketing Channels]](marketing-channels/mc-data-variances.md).&quot;

## Adobe Analytics中的数据差异 [!DNL Paid Search Detection]

的 [旧版 [!DNL Paid Search Detection]](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/paid-search-detection.html) 功能 [!DNL Analytics] 允许公司 [定义用于跟踪付费和免费搜索流量的规则](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/t-paid-search-detection.html) 对于指定的搜索引擎。 的 [!DNL Paid Search Detection] 规则使用查询字符串和反向链接域来识别付费和免费搜索流量。 的 [!DNL Paid Search Detection] 报表是 [查找方法](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/finding-methods.html) 报表，在发生指定事件（如购物车结账）或访问结束时过期。

下面是用于创建 [!DNL Paid Search Detection] 规则集：

![中付费搜索检测规则集的示例 [!DNL Analytics]](/help/integrations/assets/a4adc-paid-search-detection.png)

结果 [!DNL Paid Search Detection] 报表包括 [!UICONTROL Paid Search Engine], [!UICONTROL Paid Search Keywords], [!UICONTROL Natural Search Engine]和 [!UICONTROL Natural Search Keywords] 报表。

请注意 [!DNL Paid Search Detection] 报表：

* 的 [!UICONTROL Paid Search Keywords] 和 [!UICONTROL Natural Search Keywords] 报表显示由引荐URL标识的搜索查询，而不是用户竞价的关键词。 Adobe广告和 [!DNL Analytics] 报表显示实际的关键词，因此不希望这些关键词与 [!DNL Paid Search Detection] 关键词报表。

* 当 [!DNL Paid Search Detection] 最初创建了该功能，最初的搜索查询（用户在搜索引擎的搜索栏中输入的字符串）更容易通过反向链接URL向广告商提供。 如今，搜索引擎在很大程度上模糊了搜索查询以及 [!DNL Paid Search Detection] 关键字报表的值有限，因为大多数查询数据都在“未指定”下。

   使用 [!DNL Analytics for Advertising]，广告商仍可在 [!DNL Analytics]. 反向链接域通知引擎报告是哪个搜索引擎驱动了流量。 由于广告商特定的帐户信息未绑定到反向链接域，因此所有流量都将列在搜索引擎下。 在同一搜索引擎中具有多个帐户的广告商应参考Adobe广告或 [!DNL Analytics] 报表。

### 为何配置 [!DNL Paid Search Detection]?

的 [!DNL Paid Search Detection] 利用报表，可识别 [[!DNL Analytics Marketing Channels] 报告](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html). 将付费搜索流量与免费搜索流量分开是了解免费搜索为整个营销生态系统带来价值的绝佳途径。

## 点进数据验证 [!DNL Analytics for Advertising] {#data-validation}

对于您的集成，您应验证点进数据，以确保网站上的所有页面均正确跟踪点进次数。

在 [!DNL Analytics]，最简单的验证方法之一 [!DNL Analytics for Advertising] 跟踪是使用“点击到AMO ID实例”计算量度比较点击次数与实例，该计算量度的计算方式如下：

```Clicks to AMO ID Instances = (AMO ID Instances / AMO Clicks)```

[!UICONTROL AMO ID Instances] 表示AMO ID(`s_kwcid` 参数)。 每次点击广告时， `s_kwcid` 参数添加到登陆页面URL。 数量 [!UICONTROL AMO ID Instances]，因此，与点击次数类似，可根据实际广告点击进行验证。 我们通常会看到 [!DNL Search] 和30%的匹配率 [!DNL DSP] 流量（过滤为仅包含点进） [!UICONTROL AMO ID Instances])。 搜索和显示之间的预期差异可以通过预期流量行为来解释。 搜索会捕获意图，因此，用户通常打算单击其查询中的搜索结果。 但是，如果用户看到展示或在线视频广告，则更有可能无意中点击该广告，然后从网站跳出或放弃在跟踪页面活动之前加载的新窗口。

在Adobe广告报表中，您同样可以使用“[!UICONTROL ef_id_instances]“量度”而不是 [!UICONTROL AMO ID Instances]:

```Clicks to [!UICONTROL EF ID Instances] = (ef_id_instances / Clicks)```

虽然您应该期望AMO ID与EF ID之间的匹配率较高，但不希望出现100%的对等性，因为AMO ID和EF ID会从根本上跟踪不同的数据，这种差异可能会导致总数略有差异 [!UICONTROL AMO ID Instances] 和 [!UICONTROL EF ID Instances]. 如果总计 [!UICONTROL AMO ID Instances] in [!DNL Analytics] 不同 [!UICONTROL EF ID Instances] 但是，在Adobe广告中，联系您的 [!DNL Adobe] 客户团队寻求帮助。

有关AMO ID和EF ID的更多信息，请参阅 [AdobeAnalytics使用的广告ID](ids.md).

以下是用于跟踪实例点击量的工作区示例。

![跟踪实例点击量的工作区示例](/help/integrations/assets/a4adc-clicks-to-instances-example.png)

## 比较中的数据集 [!DNL Analytics for Advertising] 与Adobe广告相比

的 [AMO ID](ids.md) （s_kwcid查询字符串参数） [!DNL Analytics]和 [EF ID](ids.md) 用于在Adobe广告中进行报告。 由于它们是不同的值，因此可能有一个值已损坏或未添加到登陆页面。

例如，假设我们拥有以下登陆页面：

`www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id`

其中EF ID为“`test_ef_id`“”和AMO ID为“`test_amo_id`.&quot;

如果发生站点端重定向，则URL可能会如下所示：

`www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id#redirectAnchorTag`

其中EF ID为“`test_ef_id`“”和AMO ID为“`test_amo_id#redirectAnchorTag`.&quot;

在此示例中，添加锚点标记会向AMO ID中添加意外字符，从而导致Analytics无法识别值。 此AMO ID不会进行分类，因此与其关联的转化将位于“[!UICONTROL unspecified]&quot;或&quot;[!UICONTROL none]&quot; [!DNL Analytics] 报表。

幸运的是，尽管此类问题很常见，但通常不会导致高比例的差异。 但是，如果您发现 [!DNL Analytics] 和EF ID(位于Adobe广告中)，请联系您的 [!DNL Adobe] 客户团队寻求帮助。

## 其他量度注意事项

### 点击次数与访问次数之差 {#clicks-vs-visits}

它们看起来很相似，但点击次数和访问次数代表不同的数据：

* **单击：** [!DNL DSP] 或者，当访客点击发布者网站上的广告时，搜索引擎会记录一次点击。

* **访问：** [!DNL Analytics] 定义 [访问](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html) 作为用户的一系列页面查看，根据若干条件（如30分钟的非活动状态）之一结束。

根据定义，单击一次可导致多次访问。

请考虑以下示例：用户1和用户2均通过单击Adobe广告访问网站。 用户1查看了四个页面，然后离开当天，因此初始点击会导致一次访问。 用户2次浏览两页，离开45分钟午餐，返回，再浏览两页，然后离开；在这种情况下，初始点击会导致两次访问。

![点击次数与访问次数之间差异的示例](/help/integrations/assets/a4adc-visits-example.png)

### 点进次数和点进次数之差

<!-- Rob to let me know if we should remove this and add more info. to the section on AMO Instances etc. -->

点进次数和点进次数是两个不同的量度：

* **单击：** [!DNL DSP] 或者，当访客点击发布者网站上的广告时，搜索引擎会记录一次点击。

* **点进次数：** [!DNL Analytics] 当访客登陆目标网站、登陆页面加载和 [!DNL Analytics] 页面底部的请求会将数据发送到 [!DNL Analytics].

点击次数和点进次数可能因意外广告点击而有很大差异。 我们发现，展示广告的大多数点击都是意外点击，这些意外访客在登陆页面加载前点击了“返回”按钮，因此 [!DNL Analytics] 无法记录点进。 对于意外点击更有可能发生的广告，例如移动广告、视频广告和填充屏幕且必须在用户查看页面之前关闭的广告，尤其如此。

由于带宽较低或处理能力较强，在移动设备上加载的网站也不太可能产生点进次数，这会导致登陆页面加载所需的时间较长。 50%至70%的点击不会产生点进次数的情况并不罕见。 在移动设备环境中，差异可能高达90%，因为浏览器速度较慢，并且用户在浏览页面或尝试关闭广告时意外点击广告的可能性较高。

点击数据也可能会记录在无法使用当前跟踪机制记录点进次数（例如进入或从移动设备应用程序进行点击）的环境中，或者广告商仅为其部署了一种跟踪方法（例如，使用“显示到达JavaScript”方法时，阻止第三方Cookie的浏览器将跟踪点进次数，但不会跟踪点进次数）的环境中。 Adobe建议同时部署点击URL跟踪和显示到达JavaScript跟踪方法的一个关键原因是，要最大限度地覆盖可跟踪的点进。

### 将Adobe广告流量量度用于非Adobe广告Dimension

Adobe广告为Analytics提供 [特定于广告的流量量度以及DSP和[!DNL [!DNL Search]]](advertising-cloud-metrics-in-analytics.md). 提供Adobe广告的量度仅适用于指定的Adobe广告维度，并且数据不适用于 [!DNL Analytics].

例如，如果您查看 [!UICONTROL AMO Clicks] 和 [!UICONTROL AMO Cost] “按帐户划分的量度”(即“Adobe广告”维度)，您将看到总计 [!UICONTROL AMO Clicks] 和 [!UICONTROL AMO Cost] 帐户。

![使用Adobe广告维度的报表中Adobe广告量度的示例](/help/integrations/assets/a4adc-traffic-supported-dimension.png)

但是，如果您查看 [!UICONTROL AMO Clicks] 和 [!UICONTROL AMO Cost] 量度（如页面维度）(Adobe广告不为其提供数据)，然后 [!UICONTROL AMO Clicks] 和 [!UICONTROL AMO Cost] 对于每个页面，将为零(0)。

![使用不支持的维度在报表中Adobe广告量度的示例](/help/integrations/assets/a4adc-traffic-unsupported-dimension.png)

### 使用 [!UICONTROL AMO ID Instances] 取代非Adobe广告Dimension的点击量

因为你不能 [!UICONTROL AMO Clicks] 对于网站维度，您可能希望找到与点击量等效的维度。 您可能倾向于使用访问作为替代，但它们不是最佳选项，因为每个访客可能有多次访问。 (请参阅“[点击次数与访问次数之差](#clicks-vs-visits).&quot; 我们建议您改为使用 [!UICONTROL AMO ID Instances]，捕获AMO ID的次数。 While [!UICONTROL AMO ID Instances] 不匹配 [!UICONTROL AMO Clicks] 的确，它们是测量网站上点击流量的最佳选项。 有关更多信息，请参阅[的数据验证 [!DNL Analytics for Advertising]](#data-validation).&quot;

![示例 [!UICONTROL AMO ID Instances] 而不是 [!UICONTROL AMO Clicks] 对于不支持的维度](/help/integrations/assets/a4adc-amo-id-instances.png)

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* [Adobe使用的广告ID [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Adobe广告量度在Analysis Workspace中](/help/integrations/analytics/advertising-cloud-metrics-in-analytics.md)
>* [[!DNL Analytics] Adobe广告中的数据](/help/integrations/analytics/analytics-data-in-advertising-cloud.md)
>* [为何Adobe广告和 [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)

