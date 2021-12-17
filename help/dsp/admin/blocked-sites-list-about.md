---
type: Documentation
cloud: Experience Cloud
solution: Advertising Cloud
product: advertising cloud
title: 关于帐户级别和广告商级别的阻止的网站列表
description: 关于帐户级别和广告商级别的阻止的网站列表
source-git-commit: ac35677ef4832177b7a7e735bbbbf24454371496
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# 关于帐户级别和广告商级别的阻止的网站列表

<!-- Can you just add domains for your acct profile or advertiser to which you have access? It doesn't look like you can remove or edit any existing domains. Or can you with a specific syntax? -->

<!-- For domains, sub-domains,...? Specify what is valid. -->
您可以编辑用于整个Advertising Cloud帐户的阻止的网站列表以及该帐户中各个广告商的其他列表。

阻止的网站列表定义了要为您的版面排除的目标集。 每个列表都可以由顶级网站域和任何级别组成 <!--- verify --> 子域（例如example.com、my.example.com或my.new.example.com）和移动设备应用程序名称(例如???)的子域名<!-- package names/app IDs, the full URL in Google Play/iTunes? Specify what is valid. -->.

广告商级别的列表会覆盖帐户级别的列表。

>[!NOTE]
>
>* 除了Advertising Cloud DSP之外，还会应用帐户级别和广告商级别的阻止网站列表 [全局阻止的站点列表](/help/dsp/introduction/features/brand-safety-media-quality.md)，包括认为对广告不安全的网站。
>* 用户还可以将目标网站添加到任何版面。
>* 阻止的站点列表始终会覆盖目标站点列表。 如果版面同时排除和包含广告的相同目标，则会排除该目标。 <!-- Verify -->


>[!MORELIKETHIS]
<!--
>* [Edit an Account-level or Advertiser-level Blocked Site List](/help/dsp/admin/blocked-sites-list-edit.md)
[Brand Safety and Media Quality](/help/dsp/introduction/features/brand-safety-media-quality.md)
>* [Placement Settings](/help/dsp/campaign-management/placements/placement-settings.md)
-->
