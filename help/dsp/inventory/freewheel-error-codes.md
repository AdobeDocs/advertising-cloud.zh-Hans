---
title: 的错误代码 [!DNL FreeWheel] 广告提交
description: 引用为广告提交返回的错误代码 [!DNL FreeWheel].
feature: DSP Private Inventory, DSP Deal IDs
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 2%

---

# 的错误代码 [!DNL FreeWheel] 广告提交

失败广告提交的错误消息可能来自Advertising DSP或 [!DNL FreeWheel]. 错误消息显示在 [!UICONTROL API Response] 列 [[!UICONTROL Freewheel Status] 对话框](freewheel-check-status.md).

## Advertising DSP内部错误

| 错误消息 | 描述 | 后续步骤 |
|--- |--- |--- |
| [!DNL Awaiting status response from [!DNL FreeWheel]] | [!DNL FreeWheel] 尚未答复提交是成功还是失败。 | 在10分钟内再次检查状态。 |
| [!DNL The submitted ad does not have a clock number assigned.] | [!DNL FreeWheel] 不接受未分配时钟号的英国广告。 | 为广告分配一个时钟号，然后重新提交该广告。 |
| [!DNL The ad you are attempting to submit has not yet finished transcoding. Please wait ten minutes then try again.] | 在您尝试提交广告时，转码器未完成广告转码。 | 等待10分钟，然后重新提交广告。 |
| [!DNL The deal id you input is not setup as a guaranteed feed. Please submit guaranteed deals only.] | 提交的交易不是作为程序化保证交易而设置的。 [!DNL FreeWheel] 仅接受有保证的交易。 | 将交易ID设置为程序化保证交易。 广告会自动提交到 [!DNL FreeWheel] 在交易ID工作流程结束时，保存程序化保证的默认放置时，您会看到以下信息： |
| [!DNL Invalid external_deal_id:] \&lt;deal_id> | 提交的交易ID不存在或在Adobe结束时不处于活动状态。 | 确保交易处于活动状态，然后重新提交广告。 |
| [!DNL \[public_id=]\&lt;deal>]不存在 | 提交的交易ID在上不存在 [!DNL FreeWheel] 结束。 | 联系您的 [!DNL FreeWheel] 代表来确认交易ID。 |
| [!DNL Ad with identifier] \&lt;*广告名称*\> [!DNL was not found.] | 提交的广告键不存在或在Adobe结束时处于非活动状态。 | 找到正确的广告键，然后重新提交该广告。 |
| [!DNL Pending Submission] | 提交仍在待处理。 | 刷新页面。 |

{style=&quot;table-layout:auto&quot;}

## [!DNL Freewheel] API错误

| 代码 | 含义 | 描述 | 后续步骤 |
|--- |--- |--- |--- |
| 401 | 未授权 | 访问凭据不正确、缺失或无效。 | 联系您的 [!DNL Adobe] 客户团队。 |
| 403 | 禁止 | 服务器理解请求，但拒绝授权。 | 联系您的 [!DNL Adobe] 客户团队。 |
| 404 | 未找到 | 您请求的资源不可用。 如果在PUT操作中未找到创作ID，则返回404。 | 联系您的 [!DNL Adobe] 客户团队。 |
| 405 | 不允许的方法 | 使用该资源不支持的请求方法对资源发出请求(例如，使用方法上的GET要求POST发送数据，或使用只读资源上的PUT)。 | 联系您的 [!DNL Adobe] 客户团队。 |
| 408 | 请求超时 | 处理此请求时出现超时。 超时通常由对特定资源的独占访问的并发请求引起。 | 在收到此状态时重新提交请求。 如果问题仍然存在，请联系 [!DNL Adobe] 客户团队。 |
| 422 | 不可处理的实体 | 资源无效。 当请求正文无效或创建/更新的资源无效（例如，如果未找到交易ID）时，会发生此错误。 请参阅 [FreeWheel API 422错误](#freewheel-422-errors) 以了解更多信息。 | 联系您的 [!DNL Adobe] 客户团队。 |
| 500 | 内部服务器错误 | API系统错误。 | 联系您的 [!DNL Adobe] 客户团队。 |

{style=&quot;table-layout:auto&quot;}

## [!DNL Freewheel] API 422错误 {#freewheel-422-errors}

| 代码 | HTTP代码 | 描述 |
|--- |--- |--- |
| DATA_UNMARSHALL_FAILURE | 422 | 请求数据的json格式无效。 有关详细信息，请查看错误消息。 |
| DATA_VALIDATION_FAILURE | 422 | 请求数据缺少必填字段或数据类型无效。 有关详细信息，请查看错误消息。 |
| DATA_DEAL_INVALID | 422 | 交易配置不正确或不存在。 有关详细信息，请查看错误消息。 |
| DATA_DEAL_GET_失败 | 422 | 未找到交易，或其配置存在问题。 有关详细信息，请查看错误消息。 |
| DATA_CREATIVE_INGEST_FAILURE | 422 | 创作URL无效。 有关详细信息，请查看错误消息。 |
| DATA_CREATIVE_LINK_FAILURE | 422 | 该创意未与交易的广告单元节点关联。 有关详细信息，请查看错误消息。 |
| DATA_CREATIVE_UPDATE_FAILURE | 422 | 创意未更新。 有关详细信息，请查看错误消息。 |
| DATA_DSP_GET_失败 | 422 | DSP在系统中不存在。 |
| DATA_CREATIVE_UNLINK_FAILURE | 422 | 该创作元素未与广告单位取消关联。 |
| DATA_CREATIVE_DELETE_失败 | 422 | 该创意未被删除。 |
| DATA_CREATIVE_DETECTION_FAILURE | 422 | 未检测到URL。 |
| DATA_ENTITY_NOT_FOUND | 422 | 创意不存在。 |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [在中设置程序化保证交易概述 [!DNL Freewheel]](/help/dsp/inventory/freewheel-overview.md)
>* [在交易ID收件箱中接受交易](deal-id-inbox-accept.md)
>* [为程序化保证交易提交广告 [!DNL Freewheel]](/help/dsp/inventory/freewheel-submit.md)
>* [检查广告的状态 [!DNL FreeWheel] 程序化保证交易](/help/dsp/inventory/freewheel-check-status.md)

