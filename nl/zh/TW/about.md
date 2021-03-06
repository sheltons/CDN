---

copyright:
  years: 2017, 2018
lastupdated: "2018-06-28"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# 關於 Content Delivery Network (CDN)

Content Delivery Network (CDN) 是 Edge Server 的集合，分佈在國家/地區或全世界各地。Web 內容是由 Edge Server 所提供，而 Edge Server 位在最接近要求內容之客戶的地理區域中。此技術可讓您的使用者更及時地收到內容，它也為您的客戶提供更好的整體經驗。

## CDN 如何運作？

CDN 透過將 Web 內容快取到全球各地的 Edge Server 來達到其目的。客戶要求 Web 內容時，會將內容要求遞送至地理上最接近該客戶的 Edge Server。透過減少內容必須行進的距離，CDN 可提供最佳化產量、最小化延遲，並提高效能。使用 IBM Cloud Content Delivery Network 搭配 Akamai，內容提供者可以從全球各地實現有效率的要求內容遞送，並且只需要最少的配置。

IBM Cloud Content Delivery Network 服務的主要特性包括：
  * 主伺服器原點支援
  * Object Storage 原點支援
  * 相異路徑之多原點支援
  * 以路徑為基礎的 CDN 對映
  * 清除快取內容
  * 存活時間 (TTL)
  * 具有圖形視圖的度量值
  * 具有萬用字元及 DV SAN 憑證的 HTTPS 通訊協定支援
  * 主機標頭支援
  * 提供陳舊內容
  * 快取金鑰查詢引數
  * 內容壓縮
  * 大型檔案最佳化
  * 隨選視訊

如需完整特性說明，請參閱[本文件](feature-description.html#feature-descriptions)。

## 架構圖

下圖提供 IBM Cloud CDN 三層架構的圖解概觀。

![架構圖](images/3-tier-architecture.png)
