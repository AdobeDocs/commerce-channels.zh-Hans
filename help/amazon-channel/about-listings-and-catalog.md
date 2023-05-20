---
title: 關於Amazon和Commerce目錄
description: Amazon銷售管道會將您的Amazon清單匯入您的Commerce後端，並持續與產品和銷售同步。
exl-id: 659c9830-0a1d-4a0d-bb9c-afb609c0fbba
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 0%

---

# 關於Amazon和 [!DNL Commerce] 目錄

您的Adobe Commerce或Magento Open Source後端包含目錄，內含所有產品及相關設定和資訊（影像、選項、價格等），以及訂單和送貨設定。 您的 [!DNL Amazon Seller Central] 帳戶也有目錄和訂單設定，透過 [!DNL Amazon Marketplace].

為了更有效管理和檢閱您的產品目錄和透過單一位置的銷售，Amazon銷售管道會將您的Amazon清單匯入您的 [!DNL Commerce] 後端，持續與產品和銷售同步，並報告問題和趨勢。 支援與多個專案整合 [!DNL Amazon Seller Central] 帳戶，透過單一介面追蹤多個店面的所有資料。

## 產品屬性

Adobe Commerce和Magento Open Source使用產品來管理目錄同步 [屬性](https://docs.magento.com/user-guide/catalog/product-attributes.html){target="_blank"} 以定義產品設定和資料。 Amazon也使用屬性，透過上線進行對應。 期間 [預先設定任務](./amazon-pre-setup-tasks.md) 針對Amazon sales channel，您可以定義其他Amazon屬性（如有需要），以便在將Amazon清單匯入您的時，確保產品對應正確。 [!DNL Commerce] 目錄。 這些屬性包括UPC、EAN、ISBN和ASIN ([!DNL Amazon Standard Identification Number])。 透過上線，產品可在Amazon和之間同步 [!DNL Commerce] 使用您屬性的目錄。 適當的對應 [!DNL Commerce] 和Amazon產品可確保產品資訊、訂單和存貨的持續同步。

如果您尚未針對目錄建立或設定這些屬性，則應新增 [!DNL Commerce] [產品屬性](https://docs.magento.com/user-guide/catalog/product-attributes.html){target="_blank"} and values to your products before onboarding. When an Amazon attribute is imported, it can be used for search, navigation, price rules, and much more. See [What Do ASIN, UPC, EAN, ISBN, SKU and Other Barcodes Mean?](https://sellerskills.com/multi-channel-operations/what-asin-upc-ean-isbn-sku-and-other-barcodes-mean/#what-is-isbn-number){target="_blank"}

上線後，您可以隨時管理和更新產品屬性和Amazon對應。

## 產品清單

Amazon清單是您透過銷售的每個產品的產品頁面。 [!DNL Amazon Marketplace]，透過屬性顯示產品說明、價格、影像等更多對應。 在上線期間，您可以設定 [!DNL Commerce] 產品可自動發佈至Amazon清單。 您也可以將現有的Amazon清單對應至您的 [!DNL Commerce] 產品。

當您建立清單時 [!DNL Commerce] 產品，則會提交至Amazon以供核准。 大多數成功的清單都會在數小時內獲得核准。 如果您的清單獲得核准，它會顯示在 [!DNL Amazon Marketplace] 以取得客戶的即時訂單。 此 [!DNL Amazon Sales Channel] 擴充功能提供一組標籤，供您檢閱Amazon清單。 根據問題或所需的資料，您應檢閱您的 [!DNL Amazon Seller Central] 說明這些清單的特定細節。

- [作用中](./active-listings.md)：列出可透過市集取得的已核准產品清單。

- [準備列出](./ready-to-list.md)：列出符合清單規則要求且可發佈至Amazon的產品。

- [非使用中](./inactive-listings.md)：列出由於特定原因（例如品牌問題）遭到封鎖、已關閉且需要重新刊登等而無法在市面上使用的產品。

- [不合格](./ineligible-listings.md)：由於清單規則的原因，會列出無法主動在市集上列出的產品(例如 `0` 數量或銷售日期)。

- [未完成](./incomplete-listings.md)：列出遺失必要資訊的產品。 更新產品資料以供其他評論使用。

- [已結束](./ended-listings.md)：列出符合清單資格，但手動從Amazon中移除的產品清單。 您可以重新列出這些產品。

## 正在同步資料

Adobe Commerce和Magento Open Source可在您的 [!DNL Amazon Seller Central] 帳戶和 [!DNL Commerce] 後端。 持續更新透過提供單一來源 [!DNL Commerce] 管理及維護您的存貨、完成訂單、追蹤銷售，以及減少製造費用與重複工作。 報告會擷取最新資料，以追蹤趨勢並解決兩個系統之間所發生的通訊問題。

所有同步處理都由管理 [cron工作](https://docs.magento.com/user-guide/system/cron.html){target="_blank"}，設定為每5分鐘更新一次 [預先設定任務](./amazon-pre-setup-tasks.md).
