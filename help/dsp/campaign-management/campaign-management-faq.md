---
title: 关于Campaign管理的常见问题解答
description: 进一步了解营销活动管理，包括更改的延迟期以及在投放期间进行预算更改时所发生的情况。
feature: Packages, Placements
exl-id: 9034ab2c-b8b0-4759-bc87-5f73857bb062
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---

# 关于Campaign管理的常见问题解答

<!-- Most of this information should be moved into the relevant topics (especially editing topics). -->

## 设置更改的延迟

* 当您更改版面或包设置时，更改何时生效？

   设置更改通常会立即生效，但最长可能需要12小时。

   如果是最后一天交付，请在当天早些时候做出更改，这样DSP就有充足的时间根据更改来重新调整资源包。 例如，如果您从步调调整到前置负载步调，DSP需要重新评估它在整个飞行剩余时间的分配方式。 如果在航班的最后一天，你只剩一个小时才能送货，那就别做这种改变。

## 飞行中的预算更新

* 在对版面进行更改后，DSP需要多长时间才能重新分配资源包预算？

   预算分配基于投放绩效，使用14天的平均值进行评估。 版面的更改仅在导致平均14天绩效变化时，才会导致预算分配发生更改。

   当性能发生更改时，DSP会在下一个预算优化周期(大约在营销活动时区的午夜(00:00)分)内相应地在版面之间重新分配包预算。

* 在从资源包中删除版面并将其添加到其他资源包时，如何重新分配预算？

   版面的整个支出历史记录会附加到该版面，并随之从一个包移动到另一个包。

   从资源包中删除版面时，该资源包将不再具有版面支出的历史记录。 包预算将变为（包预算 — 删除的版面预算）/剩余的时间间隔。 然后，将包预算分配给包中剩余的版面。

   同样，如果您将同一版面添加到其他版面包，则当DSP为新版面包中的所有版面分配预算时，会考虑该版面的支出历史记录。

* 在飞行的最后一天，包裹的步调如何变化？

   在飞行的最后一天，将日期从24小时缩短到23小时，以便不超出包预算。 此外，包的步调填充策略会自动更改为“[!UICONTROL Frontload]”，即使它设置为“[!UICONTROL even]”也是如此。 这意味着65%的每日预算应在东部标准时间上午11:30前交付。

>[!MORELIKETHIS]
>
>* [包设置](/help/dsp/campaign-management/packages/package-settings.md)
>* [版面设置](/help/dsp/campaign-management/placements/placement-settings.md)
>* [设置效果促销活动的最佳实践](/help/dsp/optimization/campaign-best-practices-performance.md)

