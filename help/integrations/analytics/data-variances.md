---
title: ' [!DNL Analytics] 和Advertising Cloud之间的预期数据差异'
description: ' [!DNL Analytics] 和Advertising Cloud之间的预期数据差异'
feature: Integration with Adobe Analytics
exl-id: 34685e04-d4f9-4e27-b83e-b56164244b2b
source-git-commit: 185fc7d79798a0a3a9ad5829b701aeb53a4a47c1
workflow-type: tm+mt
source-wordcount: '3285'
ht-degree: 0%

---

# [!DNL Analytics]和Advertising Cloud之间的预期数据差异

*仅具有Advertising Cloud-Adobe Analytics集成的广告商*

使用[!DNL Analytics for Advertising Cloud] <!-- (A4AdC) -->集成的广告商可通过Advertising Cloud和Adobe Analytics跟踪付费广告。 当您通过多个系统跟踪媒体、营销活动和渠道时，来自不同系统的相同数据集很少会完全匹配。 本文档说明您应如何期望通过Advertising Cloud传输的媒体与在[!DNL Analytics]内跟踪媒体的不同系统中的数据进行比较。

>[!NOTE]
>
>本文档重点介绍了Advertising Cloud和Analytics，但许多关键点也可转移到其他跟踪解决方案。

## 相似报表中的归因差异

### 可能不同的回顾窗口和归因模型

[!DNL Analytics for Advertising Cloud]集成使用两个变量（eVar或rVars \[保留的eVars]\）来捕获[EF ID和AMO ID](ids.md)。 这些变量配置了单个回顾窗口（点进次数和显示到达次数归因的时间）和归因模型。 除非另有指定，否则这些变量将配置为匹配Advertising Cloud中的默认广告商级别点击回顾窗口和归因模型。

但是，回顾窗口和归因模型可在Analytics（通过eVar）和Advertising Cloud中进行配置。 此外，在Advertising Cloud中，归因模型不仅可以在广告商级别（用于竞价优化）进行配置，还可以在单个数据视图和报表中（仅用于报告目的）进行配置。 例如，组织可能倾向于使用偶数分布归因模型进行优化，但将最近联系归因用于Advertising Cloud DSP或[!DNL Search]中的报表。 更改归因模型会更改归因转化的数量。

如果在一个产品中修改了报表回顾窗口或归因模型，而在另一个产品中未修改，则每个系统的相同报表将显示不同的数据：

* **不同回顾时间范围导致的差异示例：**

   假设Advertising Cloud的点击回顾窗口为60天，而[!DNL Analytics]的回顾窗口为30天。 假设用户通过Advertising Cloud跟踪的广告访问网站，离开，然后在第45天返回并转化。 Advertising Cloud会将转化归因于初始访问，因为转化发生在60天的回顾窗口内。 [!DNL Analytics]但是，无法将转化归因于初始访问，因为转化发生在30天回顾窗口过期之后。在此示例中，Advertising Cloud报告的转化次数高于[!DNL Analytics]。

   ![归因于Advertising Cloud但不归因的转化示例  [!DNL Analytics]](/help/integrations/assets/a4adc-lookback-example.png)

* **不同归因模型导致差异的示例：**

   假设用户在转化前与三个不同的Advertising Cloud广告交互，且转化类型为收入。 如果Advertising Cloud报表使用偶数分布模型进行归因，则它将在所有广告中平均分配收入。 但是，如果[!DNL Analytics]使用最近联系归因模型，则会将收入归因于上一个广告。 在以下示例中，Advertising Cloud将捕获的30美元收入中的每一个归因为10美元，而[!DNL Analytics]将所有30美元收入归因于用户看到的最后一个广告。 在比较Advertising Cloud和[!DNL Analytics]中的报表时，您可能会发现归因差异的影响。

   ![归因于Advertising Cloud和基于不 [!DNL Analytics] 同归因模型的不同收入](/help/integrations/assets/a4adc-attribution-example.png)

>[!IMPORTANT]
>
>最佳做法是在Advertising Cloud和[!DNL Analytics]中使用相同的回顾窗口和归因模型。 根据需要与您的Adobe客户经理合作，以标识当前设置并保持配置同步。

这些相同概念适用于使用不同回顾窗口或归因模型的任何其他类似渠道。

#### 用于显示到达跟踪的不同回顾窗口 {#impression-lookback}

在Advertising Cloud中，归因基于点击次数和展示次数，您可以针对点击次数和展示次数配置不同的回顾窗口。 但是，在[!DNL Analytics]中，归因基于点进和显示到达，因此您没有选项为点进和显示到达设置不同的归因窗口；跟踪每次开始的网站。 展示可能会在显示到达的同一天或多天前发生，这可能会影响归因窗口在每个系统中的开始位置。

通常，大多数直通式转化发生得非常快，以至于两个系统都归因点数。 但是，在Advertising Cloud展示回顾窗口之外，但在[!DNL Analytics]回顾窗口内，可能会发生一些转化；此类转化归因于[!DNL Analytics]中的显示到达，但不归因于Advertising Cloud中的展示。

在以下示例中，假设访客在第1天获得了一则广告，在第2天执行了一次浏览访问（即，访问了广告的登陆页面，而之前未点击广告），然后在第45天进行了转换。 在这种情况下，Advertising Cloud将在第1-14天（使用14天回顾窗口）跟踪用户， [!DNL Analytics]将在第2-61天（使用60天回顾窗口）跟踪用户，第45天的转化将在[!DNL Analytics]内归因于广告，但不会在Advertising Cloud内归因于广告。

![在但不在Advertising Cloud中的显示到达转化归因 [!DNL Analytics] 的示例](/help/integrations/assets/a4adc-viewthrough-example.png)

出现差异的另一个原因是，在Advertising Cloud中，您可以为显示到达转化分配一个自定义的&#x200B;*显示到达权重*，该权重与基于点击的转化所应占的权重相关。 默认的显示到达权重为40%，这意味着显示到达转化将被计为基于点击的转化值的40%。 [!DNL Analytics] 不提供此类显示到达转化的权重。因此，例如，如果您使用默认显示到达权重，则在[!DNL Analytics]中捕获的100美元收入订单将在Advertising Cloud中折现为40美元 — 差额为60美元。

在比较Advertising Cloud报表和[!DNL Analytics]报表之间的显示到达转化时，请考虑这些差异。

#### 可用的归因模型

| Advertising Cloud Attribution | [!DNL Analytics] 归因 | eVar/rVar分配 |
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
>对于线性分配，[!DNL Analytics]对单次访问中所有eVar值均等地归因成功事件，因此，在“访问”eVar过期时使用线性分配。 但是，对于广告而言，使用线性归因会导致分配不是真正的线性分配，并且会导致报告不理想。 例如，如果访客在三次单独访问中转化之前与三个广告交互，则只有在上次访问中看到的广告会归因于转化，而不是全部三个广告。
>
>此外，将转化分配切换到“线性”或从“线性”切换到“线性”会阻止显示历史数据，这可能会导致报表中数据陈述错误。 例如，线性分配可能会将收入划分为多个不同的eVar值。 如果将分配更改为“最近”，则100%的收入会与最近的单个值关联。 这种关联可能会导致您得出错误的结论。
>
>为避免混淆，[!DNL Analytics]会使历史数据在报表界面中不可用。 如果您将eVar更改回初始分配设置，则可以查看历史数据，不过您不应仅为了访问历史数据而更改eVar分配设置。 Adobe建议，在您要为已记录的eVar应用新的分配设置时，应使用新的eVar，而不是更改已具有大量历史数据的数据的分配设置。

请在[https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html)中查看[!DNL Analytics]归因模型及其定义的列表。

如果您已登录Advertising Cloud，则可以在
[https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm](https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)。

#### Advertising Cloud中的事件日期归因

在Advertising Cloud中，您可以按关联的点击日期/事件日期（点击或展示事件的日期）或交易日期（转化日期）报告转化数据。 [!DNL Analytics]中不存在点击/事件日期报告的概念；在[!DNL Analytics]中跟踪的所有转化都按交易日期进行报告。 因此，在Advertising Cloud和[!DNL Analytics]中，可能会报告不同日期的相同转化。 例如，假设某位用户在1月1日点击了一则广告，并在1月5日进行了转化。 如果您在Advertising Cloud中按事件日期查看转化数据，则转化将在1月1日发生点击时报告。 在[!DNL Analytics]中，将于1月5日报告相同的转换。

![归因于不同日期的转化示例](/help/integrations/assets/a4adc-conversions-based-on.png)

## [!DNL Analytics Marketing Channels]中的归因

[[!DNL Analytics Marketing Channels] ](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/marketing-channels-admin.html) 报表允许您配置规则，以便根据点击信息的不同方面来识别不同的营销渠道。您可以使用`ef_id`查询字符串参数来识别渠道，从而将Advertising Cloud跟踪的渠道（[!UICONTROL Display Click Through]、[!UICONTROL Display View Through]和[!UICONTROL Paid Search]）跟踪为[!DNL Marketing Channels]。 <!-- Move most of the above text to "Marketing Channels" chapter once it's created, and add link here. --> 但是，即使这些报 [!DNL Marketing Channels] 表可以跟踪Advertising Cloud渠道，但由于多种原因，数据可能与Advertising Cloud报表不匹配。有关更多信息，请参阅以下部分。

>[!NOTE]
>
> 以下核心概念还适用于任何涉及未在Advertising Cloud中跟踪的促销活动的多渠道跟踪，例如[`campaign`](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/campaign.html)变量(也称为“跟踪代码”Dimension或“eVar0”)和自定义eVar跟踪。

### [!DNL Marketing Channels]中可能不同的归因模型

大多数[!DNL Marketing Channels]报表都配置了[!UICONTROL Last Touch]归因，为该归因中检测到的最后一个营销渠道分配了转化值的100%。 对[!DNL Marketing Channels]报表和Advertising Cloud报表使用不同的归因模型将导致归因转化中出现差异。

### [!DNL Marketing Channels]中可能不同的回顾窗口

可以自定义[!DNL Marketing Channels]的回顾窗口。 在Advertising Cloud中，可以配置点击回顾窗口，但固定的60天窗口很常见。 如果这两种产品使用不同的回顾窗口，您可能会发现数据差异。

### [!DNL Marketing Channels]中的不同渠道归因

Advertising Cloud报表仅捕获通过Advertising Cloud流量的付费媒体(Advertising Cloud Search广告的付费搜索和Advertising Cloud DSP广告的显示)，而[!DNL Marketing Channels]报表可跟踪所有数字渠道。 这可能会导致将转化归因到的渠道不一致。

例如，付费搜索和免费搜索渠道通常具有共生关系，其中每个渠道可相互协助。 [!DNL Marketing Channels]报表会将一些转化归因于Advertising Cloud不会进行的免费搜索，因为它不跟踪免费搜索。

另外，还可以考虑查看展示广告、点击付费搜索广告、点击电子邮件内部，然后下30美元订单的客户。 即使Advertising Cloud和[!DNL Marketing Channels]都使用最近联系归因模型，转化仍会以不同的方式归因到每个归因模型。 Advertising Cloud无权访问[!UICONTROL Email]渠道，因此它将对转化进行付费搜索。 [!DNL Marketing Channels]但是，有权访问所有三个渠道，因此该渠道将 [!UICONTROL Email] 归因于转化。

![Advertising Cloud中与  [!DNL Analytics Marketing Channels]](/help/integrations/assets/a4adc-channel-example.png)

有关量度可能不同原因的更多说明，请参阅“[为什么渠道数据在Advertising Cloud和 [!DNL Marketing Channels]](marketing-channels/mc-data-variances.md)之间可能有所不同。”

## Adobe Analytics中的数据差异[!DNL Paid Search Detection]

[!DNL Analytics]中的[旧版 [!DNL Paid Search Detection]](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/paid-search-detection.html)功能允许公司[定义规则以跟踪指定搜索引擎的付费和免费搜索流量](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/t-paid-search-detection.html)。 [!DNL Paid Search Detection]规则使用查询字符串和反向链接域来标识付费和免费搜索流量。 [!DNL Paid Search Detection]报表属于较大的[查找方法](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/finding-methods.html)报表组的一部分，该组报表会在发生指定事件（如购物车结账）或访问结束时过期。

以下是用于创建[!DNL Paid Search Detection]规则集的接口：

![中付费搜索检测规则集的示例  [!DNL Analytics]](/help/integrations/assets/a4adc-paid-search-detection.png)

生成的[!DNL Paid Search Detection]报告包括[!UICONTROL Paid Search Engine]、[!UICONTROL Paid Search Keywords]、[!UICONTROL Natural Search Engine]和[!UICONTROL Natural Search Keywords]报告。

请注意[!DNL Paid Search Detection]报表中数据存在的以下两个限制：

* [!UICONTROL Paid Search Keywords]和[!UICONTROL Natural Search Keywords]报表显示由引荐URL标识的搜索查询，而不是用户竞价的关键词。 Advertising Cloud和[!DNL Analytics]报表显示实际的关键词，因此不希望它们与[!DNL Paid Search Detection]关键词报表保持一致。

* 最初创建[!DNL Paid Search Detection]功能时，广告商可通过反向链接URL更方便地使用原始搜索查询（用户在搜索引擎的搜索栏中输入的字符串）。 如今，搜索引擎在很大程度上会模糊处理搜索查询，而[!DNL Paid Search Detection]关键字报表的值有限，因为大多数查询数据都位于“未指定”下。

   使用[!DNL Analytics for Advertising Cloud]时，广告商仍可以跟踪[!DNL Analytics]中的付费关键词。 反向链接域通知引擎报告是哪个搜索引擎驱动了流量。 由于广告商特定的帐户信息未绑定到反向链接域，因此所有流量都将列在搜索引擎下。 在同一搜索引擎中具有多个帐户的广告商应参考Advertising Cloud或[!DNL Analytics]报表，以获取特定于帐户的报表。

### 为何配置[!DNL Paid Search Detection]?

[!DNL Paid Search Detection]报表允许您识别[[!DNL Analytics Marketing Channels] 报表](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/marketing-channels-admin.html)中的免费搜索流量。 将付费搜索流量与免费搜索流量分开是了解免费搜索为整个营销生态系统带来价值的绝佳途径。

## [!DNL Analytics for Advertising Cloud]的点进数据验证 {#data-validation}

对于您的集成，您应验证点进数据，以确保网站上的所有页面均正确跟踪点进次数。

在[!DNL Analytics]中，验证[!DNL Analytics for Advertising Cloud]跟踪的最简单方法之一是使用“点击AMO ID实例”计算量度比较实例的点击量，该计算量度的计算方式如下：

```Clicks to AMO ID Instances = (AMO ID Instances / AMO Clicks)```

[!UICONTROL AMO ID Instances] 表示在网站上跟踪AMO ID(`s_kwcid` 参数)的次数。每次点击广告时，都会向登陆页面URL中添加`s_kwcid`参数。 因此，[!UICONTROL AMO ID Instances]的数量与点击次数类似，可根据实际广告点击进行验证。 通常，我们会看到[!DNL Search]的匹配率为80%,[!DNL DSP]流量的匹配率为30%（过滤后仅包含点进[!UICONTROL AMO ID Instances]）。 搜索和显示之间的预期差异可以通过预期流量行为来解释。 搜索会捕获意图，因此，用户通常打算单击其查询中的搜索结果。 但是，如果用户看到展示或在线视频广告，则更有可能无意中点击该广告，然后从网站跳出或放弃在跟踪页面活动之前加载的新窗口。

在Advertising Cloud报表中，您也可以类似地使用“[!UICONTROL ef_id_instances]”量度而不是[!UICONTROL AMO ID Instances]来比较点击次数与实例：

```Clicks to [!UICONTROL EF ID Instances] = (ef_id_instances / Clicks)```

虽然您应该期望AMO ID与EF ID之间的匹配率较高，但不希望出现100%奇偶校验，因为AMO ID和EF ID会从根本上跟踪不同的数据，这种差异可能导致总数[!UICONTROL AMO ID Instances]和[!UICONTROL EF ID Instances]中的细微差异。 如果[!DNL Analytics]中的[!UICONTROL AMO ID Instances]总数与Advertising Cloud中的[!UICONTROL EF ID Instances]相差超过1%，请联系您的Adobe客户经理以寻求帮助。

有关AMO ID和EF ID的更多信息，请参阅[Analytics使用的Advertising Cloud ID](ids.md)。

以下是用于跟踪实例点击量的工作区示例。

![跟踪实例点击量的工作区示例](/help/integrations/assets/a4adc-clicks-to-instances-example.png)

## 比较[!DNL Analytics for Advertising Cloud]中的数据集与Advertising Cloud中的数据集

[AMO ID](ids.md)（s_kwcid查询字符串参数）用于在[!DNL Analytics]中报告，而[EF ID](ids.md)用于在Advertising Cloud中报告。 由于它们是不同的值，因此可能有一个值已损坏或未添加到登陆页面。

例如，假设我们拥有以下登陆页面：

`www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id`

其中EF ID为“`test_ef_id`”，AMO ID为“`test_amo_id`”。

如果发生站点端重定向，则URL可能会如下所示：

`www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id#redirectAnchorTag`

其中EF ID为“`test_ef_id`”，AMO ID为“`test_amo_id#redirectAnchorTag`”。

在此示例中，添加锚点标记会向AMO ID中添加意外字符，从而导致Analytics无法识别值。 此AMO ID不会进行分类，因此与其关联的转化将在[!DNL Analytics]报表中位于“[!UICONTROL unspecified]”或“[!UICONTROL none]”下。

幸运的是，尽管此类问题很常见，但通常不会导致高比例的差异。 但是，如果您发现[!DNL Analytics]中的AMO ID与Advertising Cloud中的EF ID之间存在很大差异，请联系您的Adobe客户经理以获取帮助。

## 其他量度注意事项

### 点击次数与访问次数之差 {#clicks-vs-visits}

它们看起来很相似，但点击次数和访问次数代表不同的数据：

* **点击：** [!DNL DSP] 或者，当访客点击发布者网站上的广告时，搜索引擎会记录一次点击。

* **访问：** [!DNL Analytics] 定义一 [](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html) 个用户对一系列页面查看的访问，该查看会根据以下几个条件之一结束，例如30分钟处于不活动状态。

根据定义，单击一次可导致多次访问。

请考虑以下示例：用户1和用户2均通过单击Advertising Cloud广告访问网站。 用户1查看了四个页面，然后离开当天，因此初始点击会导致一次访问。 用户2次浏览两页，离开45分钟午餐，返回，再浏览两页，然后离开；在这种情况下，初始点击会导致两次访问。

![点击次数与访问次数之间差异的示例](/help/integrations/assets/a4adc-visits-example.png)

### 点进次数和点进次数之差

<!-- Rob to let me know if we should remove this and add more info. to the section on AMO Instances etc. -->

点进次数和点进次数是两个不同的量度：

* **点击：** [!DNL DSP] 或者，当访客点击发布者网站上的广告时，搜索引擎会记录一次点击。

* **点进次数：** [!DNL Analytics] 当访客登陆目标网站、加载登陆页面时，会记录一次点进，且位 [!DNL Analytics] 于页面底部的请求会将数据发送至 [!DNL Analytics]。

点击次数和点进次数可能因意外广告点击而有很大差异。 我们发现，展示广告的大多数点击都是意外点击，这些意外访客在登陆页面加载前点击了“返回”按钮，因此[!DNL Analytics]无法记录点进。 对于意外点击更有可能发生的广告，例如移动广告、视频广告和填充屏幕且必须在用户查看页面之前关闭的广告，尤其如此。

由于带宽较低或处理能力较强，在移动设备上加载的网站也不太可能产生点进次数，这会导致登陆页面加载所需的时间较长。 50%至70%的点击不会产生点进次数的情况并不罕见。 在移动设备环境中，差异可能高达90%，因为浏览器速度较慢，并且用户在浏览页面或尝试关闭广告时意外点击广告的可能性较高。

点击数据也可能会记录在无法使用当前跟踪机制记录点进次数（例如进入或从移动设备应用程序进行点击）的环境中，或者广告商仅为其部署了一种跟踪方法（例如，使用直通JavaScript方法时，阻止第三方Cookie的浏览器将跟踪点进次数，但不会跟踪点进次数）的环境中。 Adobe建议同时部署点击URL跟踪和显示JavaScript跟踪方法的一个关键原因是，可跟踪点进次数的覆盖范围最大。

### 将Advertising Cloud流量量度用于非Advertising CloudDimension

Advertising Cloud为DSP和Search提供了[广告特定的流量量度和相关维度。 ](advertising-cloud-metrics-in-analytics.md)Advertising Cloud提供的量度仅适用于指定的Advertising Cloud维度，并且数据不适用于[!DNL Analytics]中的其他维度。

例如，如果您按帐户查看[!UICONTROL AMO Clicks]和[!UICONTROL AMO Cost]量度(这是Advertising Cloud维度)，则将会按帐户查看[!UICONTROL AMO Clicks]和[!UICONTROL AMO Cost]总数。

![使用Advertising Cloud维度的报表中的Advertising Cloud量度示例](/help/integrations/assets/a4adc-traffic-supported-dimension.png)

但是，如果您按页面上的维度（如Page）查看[!UICONTROL AMO Clicks]和[!UICONTROL AMO Cost]量度(Advertising Cloud不为其提供数据)，则每个页面的[!UICONTROL AMO Clicks]和[!UICONTROL AMO Cost]将为零(0)。

![使用不支持的维度的报表中的Advertising Cloud量度示例](/help/integrations/assets/a4adc-traffic-unsupported-dimension.png)

### 使用[!UICONTROL AMO ID Instances]作为非Advertising CloudDimension的点击替代

由于不能将[!UICONTROL AMO Clicks]与现场维度一起使用，因此您可能需要找到与单击次数等效的维度。 您可能倾向于使用访问作为替代，但它们不是最佳选项，因为每个访客可能有多次访问。 (请参阅“[点击量与访问量之差](#clicks-vs-visits)”。 我们建议您改用[!UICONTROL AMO ID Instances]，这是捕获AMO ID的次数。 虽然[!UICONTROL AMO ID Instances]与[!UICONTROL AMO Clicks]不完全匹配，但它们是测量网站上点击流量的最佳选项。 有关更多信息，请参阅“[ [!DNL Analytics for Advertising Cloud]](#data-validation)的数据验证”。

![不支持 [!UICONTROL AMO ID Instances] 的维度 [!UICONTROL AMO Clicks] 的示例而不是](/help/integrations/assets/a4adc-amo-id-instances.png)

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Advertising Cloud ID使用者 [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Advertising Cloud量度在Analysis Workspace中](/help/integrations/analytics/advertising-cloud-metrics-in-analytics.md)
>* [[!DNL Analytics] Advertising Cloud中的数据](/help/integrations/analytics/analytics-data-in-advertising-cloud.md)
>* [为何数据可能因Advertising Cloud和 [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)

