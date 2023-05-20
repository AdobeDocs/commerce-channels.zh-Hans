---
title: '''[!DNL Walmart] 需求'
description: '確認您具備下列必要條件 [!DNL Walmart Marketplace]與Channel Manager整合的資訊和資源。'
exl-id: c4f247e8-280a-4595-a6c8-cf8b732d7aab
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# [!DNL Walmart] 需求

[!DNL Channel Manager] 需要下列資源和資訊才能設定 [!DNL Commerce] 的銷售管道 [!DNL Walmart Marketplace.]

* A [!DNL Walmart] 賣家帳戶

* 連線Adobe Commerce或Magento Open Source的API金鑰 [!DNL Walmart Marketplace]

   此 [!DNL Walmart Marketplace] API金鑰可讓您整合 [!DNL Channel Manager] 用於Adobe [!DNL Commerce] 或Magento Open Source和沃爾瑪商場。 開始管道管理員上線流程之前，請先在賣方中心設定API金鑰。

## 設定 [!DNL Walmart Seller] 帳戶

前往 [!DNL Walmart Seller Center] 以設定您的 [沃爾瑪賣家帳戶](https://seller.walmart.com/signup?q=&amp;origin=solution_provider&amp;src=0014M00001zivMp).

## 產生 [!DNL Walmart Marketplace] 生產API金鑰

1. 前往 [!DNL Walmart Marketplace] 產生 [適用於Adobe的解決方案提供者生產API金鑰](https://developer.walmart.com/#preloginModal?redirectUri=https%3A%2F%2Fdeveloper.walmart.com%2Faccount%2FgenerateKey).

1. 建立金鑰並設定許可權：

   * 選取Adobe作為解決方案提供者。

   * 設定許可權，如下表所示。 如需詳細資訊，請參閱 [API認證](https://sellerhelp.walmart.com/seller/s/guide?article=000006422) 在 _沃爾瑪市集賣家說明_.

   **Walmart的AdobeAPI金鑰設定**

   | **許可權** | **設定** |
   |----------------|-------------|
   | 內容 | 完全存取 |
   | 取得摘要 | 僅供檢視 |
   | 詳細目錄 | 完全存取 |
   | 專案 | 完全存取 |
   | 延遲時間 | 完全存取 |
   | 訂購 | 完全存取 |
   | 價格 | 完全存取 |
   | 報表 | 僅供檢視 |
   | 傳回 | 完全存取 |
   | 規則 | 完全存取 |
   | 送貨 | 完全存取 |

## [!DNL Walmart Marketplace] 存放區狀態

當您將產品連線至市集時，清單的可用性取決於您的狀態 [!DNL Walmart Marketplace] 商店：

* 若是即時商店，您的產品選件會列在清單中，並於比對作業完成後可供出售。

* 對於未上線的商店，您的產品選件會進行暫存，且客戶無法看到。 當 [!DNL Walmart Marketplace] 商店上線，分階段清單會自動推送至上線商店。

![[!DNL Walmart Seller Central] 暫存產品](assets/walmart-seller-central-staged.png)

>[!IMPORTANT]
>
>晚於 [!DNL Channel Manager] 安裝與設定完成，所有存貨、價格及訂單更新會自動同步。 不要連線 [!DNL Channel Manager] 至沃爾瑪商店直播，直到您停用任何其他可更新產品與訂單資料的整合功能。 如果您已設定其他整合，請確認中的料號數量與價格 [!DNL Commerce] 比對下列專案的數量： [!DNL Walmart Marketplace] 連線到即時商店之前。

