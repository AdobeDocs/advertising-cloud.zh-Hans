---
title: 在Adobe Target中配置Adobe广告的A/B测试
description: 了解如何在 [!DNL Target] 用于您的DSP和 [!DNL Search] 广告。
exl-id: 97055645-4b2f-4795-830d-9ce89ae2ad15
source-git-commit: 17482b831c5db7ef6c211f87b2e408443180746e
workflow-type: tm+mt
source-wordcount: '1647'
ht-degree: 0%

---

# 在Adobe Target中配置A/B测试以用于Advertising DSP和 [!DNL Advertising Search] 广告

<!-- Add [!UICONTROL and [!DNL tags throughout as needed. -->

<!-- Break into sub-files, or just leave as one? -->

*仅使用Advertising DSP的广告商*

Adobe广告和Adobe Target使营销人员能够更轻松地跨付费媒体和网站消息传送提供个性化且连接的体验。 通过在产品之间共享信号，您可以：

* 通过将客户的广告曝光量从DSP促销活动关联到其网站上体验，降低网站落后率。

* 通过使用Adobe Audience Manager曝光数据和点击式Target受众通过广告消息传递镜像现场体验来建立A/B测试。

* 通过Adobe Analytics中的简单可视化图表，测量统一消息传送对现场目标提升的影响 [!DNL Target].

有关设置点进和显示跟踪、在DSP和 [!DNL Target] 并设置A/B测试活动，然后 [!DNL Analytics] Analysis Workspace查看测试数据。

如果您有其他问题，请联系adcloud_support@adobe.com。

## 先决条件

此用例需要以下产品和集成：

* [!DNL Target]

* [[!DNL Analytics] （广告）](/help/integrations/analytics/overview.md) 集成<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] 表示 [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) 集成

* Audience Manager（仅用于显示到达测试）

## 步骤1:设置点进框架 {#click-through-framework}

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

![点进框架](/help/integrations/assets/target-ct-framework.png)

当您向点进URL添加DSP宏（用户单击广告并进入登陆页面时显示的URL）时，DSP会通过在点进URL中包含 ```${TM_PLACEMENT_ID}``` 中。 此宏会捕获字母数字放置键，而不是数字放置ID。

![附加到登陆页面URL的点进URL](/help/integrations/assets/target-ct-url.jpg)

### (仅限DSP)将DSP宏添加到点进URL中

<!-- If we ever write instructions for ads on other ad servers (such as Sizmek ads in DCO), then work that into the following section. -->

在Flash谈话或Google Campaign Manager 360中，手动更新每个广告的点进URL，以包含捕获AMO ID变量所需的宏。 AMO ID变量用于将点击数据发送到Adobe Analytics和共享用于A/B测试的放置键。 有关说明，请参阅以下页面：

* [附加 [!DNL Analytics for Advertising] 宏 [!DNL Flashtalking] 广告标记](/help/integrations/analytics/macros-flashtalking.md)

* [附加 [!DNL Analytics for Advertising] 宏 [!DNL Google Campaign Manager 360] 广告标记](/help/integrations/analytics/macros-google-campaign-manager.md)

请联系您的DSP客户团队和广告解决方案组(aac-advertising-solutions-group@adobe.com)以检索所需的版面密钥并完成设置，并确保每个点进URL都填充了版面密钥。

## 步骤2:使用Audience Manager设置显示到达框架 {#view-through-framework}

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

![显示到达框架](/help/integrations/assets/targetr-vt-framework.png)

通过在广告标签和版面设置中添加Audience Manager展示事件像素，您可以创建测试区段，以发掘更多的浏览测试机会。

1. 在广告标签和DSP位置设置中实施Audience Manager展示事件像素。

   有关说明，请参阅[从Advertising DSP Campaigns中收集媒体曝光数据](/help/integrations/audience-manager/media-data-integration/collect.md).&quot;

   确保添加 [DSP宏](/help/dsp/campaign-management/macros.md) 捕获您希望展示事件像素要传递的所有数据，包括 `${TM_PLACEMENT_ID_NUM}` ，用于数字版面ID。

   >[!NOTE]
   >
   >点击跟踪URL包括 `${TM_PLACEMENT_ID}` 字母数字位置键的宏，而不是 `${TM_PLACEMENT_ID_NUM}` ，用于数字版面ID。

1. 从DSP展示数据配置Audience Manager区段：

   1. 转到 **Audience Manager** > **受众数据** > **信号**，然后选择 **搜索** 选项卡。

   1. 输入 **键** 和 **值** 用于确定用户分组到哪个级别的信号。 使用 [受支持键](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html?lang=en) ，其值对应于您添加到Audience Manager展示事件像素的宏。

      例如，要对特定版面的用户进行分组，请使用 `d_placement` 键。 对于值，请使用DSP宏捕获的实际数字放置ID(例如上面屏幕截图中的2501853) `${TM_PLACEMENT_ID_NUM}`. <!-- Explain where to find the placement ID, other than in a custom report. -->

      如果“总计数”字段显示键值对的用户计数，这表示像素放置正确且数据正在流动，则可以继续下一步。
   ![搜索信号](/help/integrations/assets/target-am-signals.png)

1. [创建基于规则的特征](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) 用于在Audience Manager中创建区段。

   1. 命名特征，以便在测试活动中轻松识别该特征。 将特征存储在您喜欢的任何文件夹中。

   1. 从 **数据源** 下拉菜单，选择 **Ad Cloud**.

   1. 在表达式生成器中，添加 ```d_event``` 和 ```imp``` 在 **值** 字段，选择 **添加规则**，然后保存特征。

   ![基于规则的特征的屏幕截图](/help/integrations/assets/target-am-trait.png)

1. 在Audience Manager中设置测试区段：

   1. 在页面顶部，转到 **受众数据** > **特征** 和搜索完整特征名称。 选中特征名称旁边的复选框，然后单击 **创建区段**.

   1. 命名区段，选择 `Ad Cloud` 作为 **数据源**，然后保存区段。

      Audience Manager会自动将区段拆分为控制组（接收标准登陆页面体验）和测试组（接收个性化上门体验）。
   ![测试区段的屏幕截图](/help/integrations/assets/target-am-segment.png)

## 步骤3:在Target中设置“A/B测试”活动

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

以下说明重点介绍了与DSP用例相关的信息。 有关完整说明，请参阅[创建A/B测试](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html)”

1. [登录Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. 从 **活动** 列表，单击 **创建活动** > **A/B测试**.

   ![创建A/B测试活动](/help/integrations/assets/target-create-ab.png)

1. 在 **输入活动URL***字段，输入测试的登陆页面URL。

   ![输入Activity URL字段](/help/integrations/assets/target-create-ab-url.png)

   >[!NOTE]
   >
   >您可以使用多个URL来测试浏览网站条目。 有关更多信息，请参阅[多页面活动](https://experienceleague.adobe.com/docs/target/using/experiences/vec/multipage-activity.html).&quot; 您可以通过创建 [网站登录报表](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/integrations/ad-cloud/create-advertising-cloud-site-entry-reports.html) 中。

1. 在 **目标** 字段，输入测试的成功量度。

   >[!NOTE]
   >
   >确保 [!DNL Analytics] 在中作为数据源启用 [!DNL Target]，并且选择了正确的报表包。

1. 设置 **优先级** to `High` 或 `999` 以防止测试区段中的用户收到错误的网站体验时发生冲突。

1. 在 **报表设置**，选择 **公司名称** 和 **报表包** 已连接到您的DSP帐户。

   有关其他报表提示，请参阅[报表最佳实践和疑难解答](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html).&quot;

1. 在 **日期范围** 字段中，输入相应测试的开始和结束日期。

1. 向活动添加受众：

   1. 选择 [您之前在Audience Manager中创建的用于测试显示到达受众的区段](#view-through-framework).

      ![向活动添加受众](/help/integrations/assets/target-create-ab-audiences.png)

   1. 选择 **网站页面** > **登陆页面** > **查询**，然后在 **值** 字段来使用点进受众的Target查询字符串参数。

      ![目标点击受众的屏幕截图](/help/integrations/assets/target-click-audience.jpg)

1. 对于 **流量分配方法**，选择 **手动（默认）** 并分割受众50/50。

1. 保存活动。

1. 使用 [!DNL Target] [可视化体验编辑器](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) 更改A/B测试登陆页面模板。

   * 体验A:不要编辑，因为它是没有个性化的默认/控制登陆页面体验。

   * 体验B:使用 [!DNL Target] 用户界面，以根据测试中包含的资产（如标题、副本、按钮位置和创作元素）自定义登陆页面模板。
   >[!NOTE]
   >
   >例如，创意测试的创意测试用例，请联系您的客户团队。

## 步骤4:设置您的 [!DNL Analytics for Target] Analysis Workspace [!DNL Analytics]

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

[!DNL Analytics for Target] (A4T)是一种跨解决方案的集成，允许广告商创建 [!DNL Target] 活动基于 [!DNL Analytics] 转化量度和受众区段，然后使用 [!DNL Analytics] 作为报表源。 该活动的所有报表和分段均基于 [!DNL Analytics] 数据收集。

有关 [!DNL Analytics for Target]，包括实施说明的链接，请参阅“[Adobe Analytics作为Adobe Target报表源(A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)&quot;

### 设置 [!DNL Analytics for Target] 面板

在Analysis Workspace中，配置 [!DNL Analytics for Target panel] 分析 [!DNL Target] 活动和体验。 请记住以下有关您的报告的重要指针和信息。

#### 量度

* 在工作区中创建一个面板，该面板专用于运行测试的Adobe广告促销活动、包或版面。 使用概要可视化图表，在与Target测试性能相同的报表中显示Adobe广告量度。

* 优先使用网站上的量度（如访问次数和转化次数）来衡量性能。

* 了解来自Adobe广告的聚合媒体量度（例如展示次数、点击次数和成本）无法与Target量度相匹配。

#### Dimension

以下维度与 [!DNL Analytics for Target]:

* **Target活动**:A/B测试的名称

* **定位体验**:活动中使用的登陆页面体验的名称

* **Target活动** > **体验**:同一行中的活动名称和体验名称

### Analytics疑难解答 [!DNL Target] 数据

在Analysis Workspace中，如果您发现活动和体验数据很少或没有填充，请执行以下操作：

* 确认Target和Analytics都使用了相同的补充数据ID(SDID)。 您可以使用 [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html) 登陆页面（营销活动将用户引导至此页面）。

[Debugger中的补充数据ID(SDID)值](/help/integrations/assets/target-troubleshooting-sdid.png)

* 在同一登陆页面上，验证a)Adobe调试器中解决方案>目标下显示的主机名与b) [!DNL Target] （位于“目标和设置”>“报表设置”下）。

   [!DNL Analytics For Target] 需要 [!DNL Analytics] 跟踪服务器在从 [!DNL Target] 到 [!DNL Modstats] Analytics的数据收集服务器。&lt;! — 只是“到Analytics？”>

[Debugger中的主机名值Adobe](/help/integrations/assets/target-troubleshooting-hostname.png)

[Target中的跟踪服务器值](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## 进一步阅读

* [将Target与Analytics集成](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html) — 说明如何在Analysis Workspace中设置Target报表。
* [A/B测试概述](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html)  — 描述可用于DSP广告的A/B测试活动。
* [体验和选件](https://experienceleague.adobe.com/docs/target/using/experiences/experiences.html)  — 说明 [!DNL Target] 用于确定DSP测试用户所接触到的现场内容的工具。
* [信号、特征和区段](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html)  — 定义一些可帮助进行DSP查看测试的Audience Manager工具。
* [用于广告的Analytics概述](/help/integrations/analytics/overview.md)  — 引入了Analytics for Advertising，它允许您跟踪Analytics实例中的点进和显示到达网站的交互。

<!-- 
>[!MORELIKETHIS]
>
>* 
-->
