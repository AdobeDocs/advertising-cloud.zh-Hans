---
title: 常见问题解答
description: xx
source-git-commit: ca19836d5918c69161c4d850a65eaff311249225
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 0%

---

# xxx常见问题解答

## 标题

https://adobeadcloud.zendesk.com/agent/tickets/14214默认情况下，Adobe Analytics会报告每个报表中所有捕获的事件。 &quot;[!UICONTROL Unspecified]“事件表示未连接到Advertising Cloud的表单完成事件。 例如，在广告平台报表中，电子邮件促销活动驱动的自然转化或转化将归为“未指定”。

您可以使用过滤器通过通过“包括未指定（无）”选项删除复选标记，从报表中删除未指定事件。 <!-- Not sure if this is in DSP or in Analytics Workspace -->

## 标题

https://adobeadcloud.zendesk.com/agent/tickets/24323将Analytics事件标记放置在与Ad Cloud像素相同的位置，以确保XXX匹配。

## 标题

https://adobeadcloud.zendesk.com/agent/tickets/24323

问：在内部安全审核期间，某些功能被标记为安全问题，在将Ad Cloud集成到现有Adobe Analytics安装中后，我们启用了这些功能。

相关集成位于AdCloud和Adobe Audience Manager之间。 此功能可增加AdCloud和Adobe Audience Manager之间访客ID的匹配率。 它通过向pagead.l.doubleclick.net、star-mini.c10r.facebook.com和pug88000nf.pubmatic.com发送网络请求来确定这些服务是否具有可供利用的访客现有ID。 这些网络请求已被标记为安全风险，并针对所有网站访客发生。

我们的审计员要求我们禁用此功能。 如果我们阻止这些网络请求，会发生什么情况？

答：我们与我们的产品进行了核对，他们提到，相关像素的目的是提高Ad Cloud、特定库存/SSP合作伙伴(对于DSP)和AAM之间的Cookie匹配率。  如果删除了这些像素，客户可能会看到AAC/AAM与库存合作伙伴之间各自像素所对应的匹配率有所降低，但他们不认为匹配率会很大。

对于Ad Cloud搜索，我们确实会看到组织的Experience CloudID已为Mathworks设置，但我们的产品团队没有看到Mathworks设置以在Ad Cloud中激活受众。 您是否使用Audience Manager将受众发送到Ad Cloud搜索？ 如果没有，则删除这些参数对当前工作流将不会产生影响。 AAM客户关怀团队可以帮助移除这些像素（如果您不希望触发这些像素）。

