---
title: 使用 [!DNL Last Event Service] JavaScript库(包含 [!DNL Web SDK]
description: 了解从使用 [!DNL Analytics] [!DNL visitorAPI] 库 [!DNL Experience Platform] [!DNL Web SDK] 库 [!DNL Analytics for Advertising] 实施。
feature: Integration with Adobe Analytics
exl-id: 96537244-1c5c-4d9a-a44e-ba7fcea9381d
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---

# 使用 [!DNL Last Event Service] 包含Adobe Experience Platform的JavaScript库 [!DNL Web SDK]

*仅具有Adobe广告与Adobe Analytics集成的广告商*

如果贵组织使用旧版Adobe Analytics `visitorAPI.js` 用于数据收集的库中，您可以选择使用 [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) 库(`alloy.js`)，它允许您通过 [!DNL Edge Network].

的 [!DNL Analytics for Advertising] [!DNL Last Event Service] JavaScript库会按原样记录显示到达事件和点进事件，并使用补充ID(`SDID`)。 的 [!DNL Web SDK] 但是，库不提供 [!DNL stitch ID]. 使用 [!DNL Web SDK] 表示 [!DNL Analytics for Advertising]，您需要修改1) [!DNL Last Event Service] 标记，并且2 [!DNL Web SDK] `sendEvent` 中，将相应地执行以下操作：

## 步骤1:编辑 [!DNL Last Event Service] 要生成的标记 `[!DNL StitchID]`

在 [!DNL Analytics for Advertising] [!DNL Last Event Service] 标记，添加代码以生成 `[!DNL StitchID]` 使用库中捆绑的随机ID生成器。

**旧版标记：**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id');
</script>
```

**新标记：**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id').generateRandomId();
</script>
```

## 步骤2:使用 [!DNL Web SDK] 发送 [!DNL StitchID] 作为XDM数据 [!DNL Analytics]

在 [!DNL Web SDK] `sendEvent` 命令发送 [!DNL StitchID] to [!DNL Experience Edge] as [!DNL Experience Data Model] (XDM)数据 [!DNL Analytics].<!-- The library will send the StitchID to [!DNL Experience Edge] as `[_adcloud.advertisingStitchID](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/adcloud/stitch.schema.md)`. --> [!DNL Analytics] 将值用作 `SDID`.

**要添加的属性：**

```
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
```

**示例：**

```
<script>
  alloy("sendEvent", {
    "xdm": {
      "commerce": {
        "order": {
                ………
        }
     },
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
    }
  });
</script>
```

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* [适用于的JavaScript代码 [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md)

