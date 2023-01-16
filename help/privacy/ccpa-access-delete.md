---
title: Adobe对《加州消费者隐私法案》的广告支持：消费者数据访问和删除支持
description: 了解支持的数据请求类型、必需的设置和字段值，以及使用旧版产品ID和返回的数据字段的API访问请求示例。
feature: CCPA
exl-id: 1330da6c-a944-4bb5-8539-488d97f56175
source-git-commit: 17482b831c5db7ef6c211f87b2e408443180746e
workflow-type: tm+mt
source-wordcount: '1076'
ht-degree: 0%

---

# Adobe对《加州消费者隐私法案》的广告支持：消费者数据访问和删除支持

*对于 [!DNL Adobe Advertising Search];Adobe广告DSP;Adobe广告创意；和Adobe广告DCO*

>[!IMPORTANT]
>
>本文档的内容不是法律建议，也不会代替法律建议。 请咨询您的法律顾问，以获取有关《加州消费者隐私法案》的建议。

《加州消费者隐私法案》(CCPA)是加利福尼亚州的新隐私法，于2020年1月1日生效。 CCPA为加利福尼亚州居民提供了有关其个人信息的新权利，并对在加利福尼亚州开展业务的某些实体强加了数据保护责任。 CCPA为消费者提供了访问和删除其个人信息的权利，以及选择退出某些有资格“向第三方出售”个人信息的活动的权利。

作为企业，您将决定Adobe Experience Cloud代表您处理和存储的个人数据。

作为您的服务提供商，Adobe广告为您的企业提供支持，以履行CCPA规定的适用于Adobe广告产品和服务使用的义务，包括管理访问和删除个人信息的请求以及管理选择退出出售个人信息的请求。

本文档介绍如何 [!DNL Advertising Search];广告创意；Advertising DSP(Demand Side Platform);和 [!DNL Advertising DCO]  — 作为服务提供商 — 支持消费者使用Adobe访问和删除个人信息的权利 [!DNL Experience Platform Privacy Service API] 和 [!DNL Privacy Service UI].

有关Advertising DSP如何支持消费者选择退出出售个人信息的权利的信息，请参阅 [Adobe对《加州消费者隐私法案》的广告支持：消费者选择退出支持](/help/privacy/ccpa-opt-out-of-sale.md).

有关CCPA的Adobe隐私服务的更多信息，请参阅 [Adobe隐私中心](https://www.adobe.com/privacy/ccpa.html).

## 支持的Adobe广告数据请求类型

Adobe Experience Platform为企业提供了完成以下任务的功能：

* 在 [!DNL Search], [!DNL Creative], [!DNL DSP]或 [!DNL DCO].
* 删除中存储的Cookie级数据 [!DNL Search], [!DNL Creative], [!DNL DSP]或 [!DNL DCO] 对于使用浏览器的消费者；或删除存储在 [!DNL DSP] 适用于在移动设备上使用应用程序的消费者。
* 检查一个或多个现有请求的状态。

## 发送Adobe广告请求所需的设置

要请求从Adobe广告中访问和删除消费者个人信息，您将需要：

1. 部署JavaScript库以检索和删除客户的Cookie。 同一个图书馆， `AdobePrivacy.js`，用于所有Adobe Experience Cloud解决方案。

   >[!IMPORTANT]
   >
   >对某些Experience Cloud解决方案的请求不需要JavaScript库，但Adobe广告请求需要JavaScript库。

   您应该在网页上部署库，客户可以从中提交访问和删除请求，例如您公司的隐私门户。 库可帮助您检索AdobeCookie(命名空间ID: `gsurferID`)，以便您能够通过提交这些身份，作为访问和删除请求的一部分 [!DNL Adobe Experience Platform Privacy Service API].

   当客户要求删除个人数据时，库还会从客户的浏览器中删除客户的Cookie。

   >[!NOTE]
   >
   >删除个人数据与选择退出不同，退出后会阻止使用受众区段的最终用户进行定位。 但是，当消费者要求从 [!DNL Creative], [!DNL DSP]或 [!DNL DCO]，该库还会向Adobe广告发送请求，以选择退出客户区段定位。 对于具有 [!DNL Search]，我们建议您为客户提供一个指向 [https://www.adobe.com/privacy/opt-out.html#customeruse](https://www.adobe.com/privacy/opt-out.html#customeruse)，其中说明了如何选择退出受众区段定位。

1. 识别您的Experience Cloud组织ID，并确保它已关联到您的Adobe广告帐户。

   Experience Cloud组织ID是由24个字符组成的字母数字字符串，其后附加有“@AdobeOrg”。 大多数Experience Cloud客户都分配了组织ID。 如果您的营销团队或内部Adobe系统管理员不知道您的组织ID，或者不确定是否已配置，请通过gdprsupport@adobe.com联系Adobe客户关怀团队。 您需要组织ID才能使用 `imsOrgID` 命名空间。

   >[!IMPORTANT]
   >
   >联系贵公司的Adobe广告代表，以确认贵组织的所有Adobe广告帐户(包括 [!DNL DSP] 帐户或广告商， [!DNL Search] 帐户和 [!DNL Creative] 或 [!DNL DCO] 帐户 — 已关联到您的Experience Cloud组织ID。

1. 使用 [Adobe Experience Platform Privacy Service API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) （对于自动请求）或 [Privacy ServiceUI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html) （对于临时请求）代表消费者向Adobe广告提交访问和删除个人信息的请求，并检查现有请求的状态。

   适用于具有移动设备应用程序与客户交互并通过 [!DNL DSP]，您将需要下载隐私就绪的移动SDK才能进行Experience Cloud。 Mobile SDK允许企业设置选择退出状态标记，检索消费者的设备ID(命名空间ID: `deviceID`)，并向Privacy ServiceAPI提交请求。 您的移动设备应用程序将需要SDK版本4.15.0或更高版本。

   在您提交消费者访问请求时，Privacy ServiceAPI会根据指定的Cookie或设备ID返回消费者的信息，然后您必须将该信息返回给消费者。

   在您提交消费者删除请求时，Cookie ID或设备ID以及与Cookie关联的所有成本、点击和收入数据都会从服务器中删除。

   >[!NOTE]
   如果您的企业具有多个Experience Cloud组织ID，则必须为每个IP发送单独的API请求。 但是，您可以向多个Adobe广告子解决方案([!DNL Search], [!DNL Creative], [!DNL DSP]和 [!DNL DCO])，每个子解决方案具有一个帐户。

要从Adobe广告获得支持，所有这些步骤都是必需的。 有关使用Adobe Experience Platform Privacy Service执行这些任务和其他相关任务以及在何处查找所需项目的更多信息，请参阅 [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Adobe广告JSON请求中的必填字段值

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*您的Experience Cloud组织ID*>

&quot;users&quot;:

* `"key":` &lt;*通常是客户的名称*>

* `"action":` e `**access**` 或 `**delete**`

* `"user IDs":`

   * `"namespace": **411**` （表示adcloud cookie空间）

   * `"value":` &lt;*实际客户的cookie ID值，检索自`AdobePrivacy.js`*>

* `"include": **adCloud**` (即适用于请求的Adobe产品)

* `"regulation": **ccpa**` （即适用于该请求的隐私法规）

## 消费者使用从AdobePrivacy.js检索到的Adobe广告用户ID提交的请求示例

```
{
"companyContexts":[
      {
         "namespace":"imsOrgID",
         "value":"5AB13068374019BC@AdobeOrg"
      }
   ],
   "users": [
{
 "key": "John Doe",
 "action":["access"],
  "userIDs":[
      {
         "namespace":"411",
         "value":"Wqersioejr-wdg",
         "type":"namespaceId",
         "deletedClientSide":false
      }
   ]
}
],
"include":[
      "adCloud"
   ],
    "regulation":"ccpa"
}
}
```

## 为访问请求返回的数据字段

以下是Adobe广告的个人信息访问响应示例。

```
{
    "jobId":"12345AD43E",
    "action":"access",
    "product":"adCloud",
    "status":"complete",
    "results":{
        "userIDs":[
            {
                "namespace":"411",
                "userID":" Wqersioejr-wdg "
            }
        ],
        "receiptData":{
            "impressionCount":"100",
            "clickCount":5,
            "geo":[
                "United States of America",
                "San Francisco CA"
            ],
            "profile":[
                {
                    "pixelid":"111",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                },
                {
                    "pixelid":"123",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                }
            ],
            "matchingSegments":[
                {
                    "segmentName":"AP4 - Art/Culture - In-Market",
                    "segmentID":"kV1mPa2aqPNWKSNtf325",
                    "serviceProvider":"Adobe"
                },
                {
                    "segmentName":"EMEA - UK - Health Food Buyers",
                    "segmentID":"eP2oJ2UPsfsDVDhvlGewx",
                    "serviceProvider":"BlueKai"
                }
            ]
        }
    }
}
```
