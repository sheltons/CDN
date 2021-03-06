---

copyright:
  years: 2018
lastupdated: "2018-06-28"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# 關於 HTTPS

IBM Cloud 提供兩種使用 HTTPS 來保護 CDN 的方式：「萬用字元憑證」及「網域驗證 (DV) SAN 憑證」。在配置 CDN 時選取 **HTTPS 埠**，即可配置這兩個 HTTPS 選項。預設「HTTPS 埠」為 443，或者您可以選擇不同的埠號來遞送 HTTPS 資料流量。您可以在[常見問題](faqs.html#are-there-any-restrictions-on-what-http-and-https-port-numbers-are-allowed-for-akamai-)中，找到容許的埠號清單。

## 萬用字元憑證支援
>「萬用字元」憑證是將 Web 內容安全地遞送給一般使用者的最簡單方式。完整 CDN CNAME（包括「萬用字元」憑證字尾）**必須**用來作為服務進入點（例如，`https://example.cdnedge.bluemix.net`），才能使用「萬用字元」憑證。
>
>IBM Cloud CDN 使用「萬用字元」憑證 `*.cdnedge.bluemix.net`。CNAME（不論是為您建立還是由您提供，且結尾為 `*.cdnedge.bluemix.net` 字尾）會新增至 CDN Edge Server 上所維護的萬用字元憑證。因此，CNAME 會變成一般使用者針對 CDN 使用 HTTPS 的唯一方式。

![Http 及萬用字元的圖表](images/state-diagram-wildcard.png)

## 主體替代名稱 (SAN) 憑證支援

>「主體替代名稱 (SAN) 憑證」是容許透過單一憑證來保護多個網域或主機名稱的數位 SSL 憑證。
>
>使用 SAN 憑證進行 HTTPS 時，您的主要「CDN 主機名稱」會新增至由「憑證管理中心」發出的憑證。這可讓使用者透過主機名稱（而非 CNAME）安全地存取服務；例如，`https://www.example.com`。
>
>使用 HTTPS SAN 憑證下 CDN 訂單時，會完成要求憑證以及建立「網域控制驗證 (DCV)」的處理程序。DCV 是「憑證管理中心」用來建立您有權存取及控制網域的處理程序。需要您採取動作，才能完成此步驟。建立控制權之後，會將憑證部署至全球的 CDN Edge Server。順利部署憑證之後，即會自動處理憑證的更新。您可以在[特性說明](about.html#https-protocol-support)中，找到此特性的相關資訊。在[完成 HTTPS 的網域控制驗證](how-to-https.html#initial-steps-to-domain-control-validation)頁面上，會更詳細地說明「網域控制驗證」方法。

![具有 SAN 憑證之 HTTPS 的圖表](images/state-diagram-san.png)
