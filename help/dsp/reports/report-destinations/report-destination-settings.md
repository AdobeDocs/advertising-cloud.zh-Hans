---
title: 报表目标设置
description: 按目标类型查看报表目标所需的详细信息。
feature: DSP Custom Reports
source-git-commit: ff14691fd2b6fa56c303dca3ac0e4c897c322f72
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---


# 报表目标设置

非电子邮件报表目标所需的详细信息因目标类型而异。

>[!NOTE]
>
> 您还可以将自定义报表交付给电子邮件收件人，收件人不需要保存的报表目标。 您可以在报表设置中指定电子邮件收件人，而不是保存的目标。

## [!UICONTROL S3]

**[!UICONTROL Name]:** 用于帮助您识别目标的名称。

**[!UICONTROL S3 Bucket URL]:** 上文件夹的完整路径 [!DNL Amazon Simple Storage Service] (S3)将报表上传到的存储段。 示例： `s3://adcloud_account/reports`

**[!UICONTROL Access Key ID]:** 对([!DNL Amazon S3])存储段(提供者 [!DNL Amazon])。

**[!UICONTROL Secret Access Key]:** 对([!DNL Amazon S3])存储段(提供者 [!DNL Amazon])。

## [!UICONTROL FTP]

**[!UICONTROL Name]:** 用于帮助您识别目标的名称。

**[!UICONTROL Server]:** 服务器的主机名。

**[!UICONTROL Port]:** 要在服务器上使用的端口号。 默认值为 *[!UICONTROL 21]*.

**[!UICONTROL Username]:** 要登录到服务器的用户名。

**[!UICONTROL Password]:** 登录到服务器的密码。

**[!UICONTROL Path (Optional)]:** 将文件上传到的服务器路径。

## [!UICONTROL SFTP]

**[!UICONTROL Name]:** 用于帮助您识别目标的名称。

**[!UICONTROL Server]:** 服务器的主机名。

**[!UICONTROL Port]:** 要在服务器上使用的端口号。 默认值为 *[!UICONTROL 21]*.

**[!UICONTROL Username]:** 要登录到服务器的用户名。

**[!UICONTROL Password]:** 登录到服务器的密码。

**[!UICONTROL Path (Optional)]:** 将文件上传到的服务器路径。

## [!UICONTROL FTP SSL]

**[!UICONTROL Name]:** 用于帮助您识别目标的名称。

**[!UICONTROL Server]:** 服务器的主机名。

**[!UICONTROL Port]:** 要在服务器上使用的端口号。 默认值为 *[!UICONTROL 21]*.

**[!UICONTROL Username]:** 要登录到服务器的用户名。

**[!UICONTROL Password]:** 登录到服务器的密码。

**[!UICONTROL Path (Optional)]:** 将文件上传到的服务器路径。

>[!MORELIKETHIS]
>
>* [关于 [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [创建 [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-create.md)
>* [编辑 [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-edit.md)
>* [删除 [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-delete.md)

