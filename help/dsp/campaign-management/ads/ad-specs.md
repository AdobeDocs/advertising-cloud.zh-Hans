---
title: 广告规范
description: 参考常规和特定于发布者的广告规范。
feature: DSP Ads
exl-id: 905dfd9b-e7a3-4eb6-988f-b49d4b282dd2
source-git-commit: b867ace878a0c1e6391476e267c9161e5ecea921
workflow-type: tm+mt
source-wordcount: '841'
ht-degree: 0%

---

# 支持的广告类型的规范

## 视频广告（前置广告和CTV）

### 支持的屏幕

默认情况下，广告在桌面设备、移动设备和连接的电视设备上提供。 设备定位可用于调整投放。

### 支持的第三方广告服务器

您可以使用 [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid]和 [!DNL Sizmek]. 有关受支持供应商的完整列表，请参阅[经认证的广告服务合作伙伴](certified-ad-servers.md).&quot;

### 高清视频资产的要求（必需）

**视频标记类型：** VPAID 2.0 JavaScript或VAST(CTV)。 所有VPAID广告单位都必须遵循 [VPAID 2.0规范](https://iabtechlab.com/wp-content/uploads/2016/04/VPAID_2_0_Final_04-10-2012.pdf) 由互动广告局(IAB)定义。

**视频编解码器：** MP4/H.264

**解决办法：** 720p为1280x720,1920x1080,1080p为1080

**比特率：** 1500-2500 kbps(720p),2500-3500 kbps(1080p)

**H.264配置文件/级别：** 720便士的3.1级高调；备受关注，1080p的4.0级

**视频帧率：** 29.970 fps（通常称为30 fps）（对于NTSC国家/地区），25 fps（对于PAL国家/地区），23.976 fps（通常称为24 fps）（对于影片外观内容）

**视频色彩空间：** 4:2:0 YUV色度子采样

**视频隔行：** 逐行扫描，即非隔行扫描。 无场内运动（混合帧）或隔行。

**领导者（石板）：** 不允许

**音频编解码器：** AAC-LC或HE-AACv1

**音频比特率：** AAC-LC为128-192 kbps，HE-AACv1为64-128 kbps

**音频渠道：** 2声道立体声混合

**音频采样率：** 44.1 kHz或48 kHz，作为每种源材料

**音频级别：** 24个LKFS(+/- 2.0 dB)，按照ATSC A/85;根据欧洲银行R128，欧盟23个LUFS(+/- 1.0)

#### 连接的电视广告的其他发布者要求

* **A+E网络：** 请参阅A+E网络的 [广告规范](/help/dsp/assets/a-e-networks-tve-video-ad-specs.pdf)

* **发现：** 请参阅Discovery的 [广告规范](/help/dsp/assets/discovery-networks-ad-specs.pdf).

* **迪士尼(包括 葫芦网):** 观看迪士尼 [广告规范](https://hulu.disneyadsales.com/ad-products/video-commercial/).

* **HBO Max:** 观看HBO Max的 [广告规范](/help/dsp/assets/hbo-max-ad-specs-2022.xlsx).

* **NBC通用：**

   * [数字视频](https://together.nbcuni.com/nbcu-creative-guidelines/digital-video/)

   * [实时流](https://together.nbcuni.com/nbcu-creative-guidelines/livestream/)

   * [孔雀](https://together.nbcuni.com/nbcu-creative-guidelines/peacock/)

* **派拉蒙：** 参见派拉蒙的 [广告规范](https://www.paramount.com/digital-ads).

## 显示广告

### 支持的屏幕

默认情况下，广告在桌面和移动设备上交付。 设备定位可用于调整投放。

### 支持的文件类型

**图像：** GIF、JPG/JPEG、PNG

**HTML5:** 图像文件类型：GIF、JPG/JPEG、PNG、SVG

### 图像资产要求（必需）

支持通用显示。

**推荐广告大小：** 120x60、160x600、180x150、300x50、300x100、300x1050、300x250、300x600、320x50、320x480、480x60、640x40888x31、728x90、970x250、970x90

**支持的第三方广告服务器：** 您可以使用 [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid]和 [!DNL Sizmek]. 有关受支持供应商的完整列表，请参阅[经认证的广告服务合作伙伴](certified-ad-servers.md).&quot;

## 音频广告

### 支持的屏幕

台式机、移动设备、平板电脑、智能扬声器和连接的电视

### 支持的第三方广告服务器

您可以使用 [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid]和 [!DNL Sizmek]. 有关受支持供应商的完整列表，请参阅[经认证的广告服务合作伙伴](certified-ad-servers.md).&quot;

### 音频资产要求（必需）

**文件类型：** MP3、OGG、AAC

**领导者（石板）：**  不允许

**最大文件大小：** 2MB

**比特率：** 128

**文件长度：** 0-60秒

#### 其他发布者要求

* **[!DNL iHeartRadio]**
   * 长度：5、15、30或60秒
   * 文件类型：MP3
   * 最大文件大小：320 kbps
   * 卷：44.1千赫

* **[!DNL Pandora]**
   * 长度：15或30秒
   * 文件类型：MP4（应用程序内）、MP3（桌面）
   * 最大文件大小：2.2 MB

* **[!DNL SoundCloud]**
   * 长度：6、15或30秒
   * 文件类型：MP3
   * 最大文件大小：5 MB

* **[!DNL Spotify]**
   * 长度：最多30秒
   * 文件类型：OGG
   * 最大文件大小：500MB
   * 卷：RMS标准化为–14;dBFS峰归一化为–0.2 dBFS

* **[!DNL TargetSpot]**
   * 长度：15、30或60秒
   * 文件类型：MP3

* **[!DNL TuneIn]**
   * 长度：10、15或30秒
   * 文件类型：MP3、OGG
   * 卷：44.1千赫

### 伴随横幅广告的要求（可选）

**支持的大小：** 300x250、500x500、640x640、1024x1024

#### 其他发布者要求

* **[!DNL iHeartRadio]:**
   * 文件类型：JPEG、JPG、PNG、GIF、SWF、HTML
   * 最大文件大小：2.2 MB
   * Dimension:300x250

* **[!DNL Pandora]:**
   * 文件类型：JPEG,GIF
   * 最大文件大小：大小：100 KB
   * Dimension:300x250（移动设备或台式机）或500x500（台式机）

* **[!DNL SoundCloud]:**
   * 文件类型：静态JPG, PNG
   * 最大文件大小：低于400 KB
   * Dimension:1024x1024

* **[!DNL Spotify]:**
   * 文件类型：静态JPG, PNG
   * 最大文件大小：200 KB
   * Dimension:300x250

* **[!DNL TuneIn]:**
   * 文件类型：JPEG、JPG、PNG、GIF、HTML
   * 最大文件大小：2 MB
   * Dimension:300x250
 

## 本机显示广告

每个广告可以包含静态图像或移动GIF（电影）。

### 支持的屏幕

默认情况下，广告在桌面和移动设备上交付。 设备定位可用于调整投放。

### 所有本机信息源内格式所需的资产

#### 图像资产

**解决办法：** 最少600x600像素；建议最少1200x627像素

**文件类型：** JPEG（图像广告或视频广告封面图像）、GIF（电影）

**文件大小：** 小于1 MB（图像应不含文本。）

#### 广告商徽标

**解决办法：** 最少80x80像素；建议最少300x300像素

**文件类型：** JPEG或PNG。

**宽高比：**  1x1比率

>[!NOTE]
>
>根据将覆盖图像的图像，在浅色或深色徽标资产之间进行选择。

#### 文本/复制

**标题：** 最多200个字符；推荐25个字符

**题注：** 最多200个字符；建议使用100个字符

**赞助方：** 最多200个字符；推荐30个字符

**行动动员（仅限MoPub）：** 最多15个字符

>[!NOTE]
>
>最终布局由发布者在运行时定义。 如果广告超出了建议的字符数，则某些库存提供商可能无法交付广告，或者发布者或SSP可能会截断文本。

#### 登陆页面URL

包含可选点击跟踪器的点进URL。

点击跟踪器的要求：

* 第三方展示跟踪像素：仅1x1图像URL格式

* 可查看性JavaScript跟踪器：仅支持IAS;仅JS.append格式的1x1图像

* 第三方点击跟踪像素：必须重定向到嵌入在URL中的登陆页面（HTTP 302重定向）

* 不支持具有200个或更多响应的数据管理平台(DMP)点击跟踪器。

>[!MORELIKETHIS]
>
>* [关于广告管理](ad-about.md)
>* [创建单个广告](ad-create.md)
>* [创建多个第三方广告](ad-create-multiple.md)
>* [编辑广告](ad-edit.md)

