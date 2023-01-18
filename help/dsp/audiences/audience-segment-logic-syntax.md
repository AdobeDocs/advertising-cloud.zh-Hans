---
title: 受众区段逻辑的语法
description: 引用可用于定义受众区段逻辑的语法。
feature: DSP Audiences
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# 受众区段逻辑的语法

在创建可重用受众时，您可以使用字母数字区段ID（键）和以下语法手动定义区段逻辑：

* ()指示一组
* `||` 表示 [!DNL OR] <!-- || escaped with backticks so Jenkins doesn't think it's a Markdown table -->
* &amp; [!DNL AND]
* ! 表示 [!DNL NOT] （排除）

>[!NOTE]
>
>* 除非前面有！，否则将包含所有指定的区段组 （不包括这些规则）。
>* 您可以 [查找受众的区段ID](reusable-audience-clipboard.md) 从 [!UICONTROL Audiences] > [!UICONTROL All audiences].


例如，以下逻辑：

```
(X5vUk1cNvZxvBJ3jMjTt) || (sfvXrmQkk77PL5OtHpLH) && !(SMWSjTZFiy9hR1bKm1vw || x08UReA0IcP9HAJdcGVe)
```

均值（英语简单）

```
[!DNL INCLUDE] Segment ID X5vUk1cNvZxvBJ3jMjTt [!DNL OR] INCLUDE Segment ID sfvXrmQkk77PL5OtHpLH [!DNL AND EXCLUDE] (Segment ID SMWSjTZFiy9hR1bKm1vw AND Segment ID x08UReA0IcP9HAJdcGVe)
```

>[!NOTE]
>
>在版面设置中，您可以将保存的受众用作明确定位的受众，或用作要从定位中排除的单独受众。 确保区段逻辑反映您使用受众的目的。

>[!MORELIKETHIS]
>
>* [将可重复使用受众的区段键复制到剪贴板](reusable-audience-clipboard.md)
>* [关于受众管理](audience-about.md)
>* [创建可重用受众](reusable-audience-create.md)
>* [受众设置](audience-settings.md)
>* [可用的第三方数据提供商](third-party-data-providers.md)

