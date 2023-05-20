---
title: 將清單連結至沃爾瑪
description: '連線以下專案的清單 [!DNL Commerce] 產品目標 [!DNL Walmart Marketplace]開始銷售。'
exl-id: 78078b14-ebdd-415d-9486-66b0150167aa
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '1096'
ht-degree: 0%

---

# 將清單連結至沃爾瑪

如同其他市集， [!DNL Walmart] 可讓協力廠商賣家列出其他人銷售的專案。

- [!DNL Walmart Marketplace] 使用UPC和GTIN等產品識別碼來比對產品與現有 [!DNL Walmart Marketplace] 清單。

- 對於相符的產品，沃爾瑪市集列出更新內容，包括 [!DNL Commerce] 產品選件（當您從以下位置連線產品時） [!DNL Channel Manager].

- 通常，價格最低的產品優惠方案會先出現在 [!DNL Walmart Marketplace] 清單，但其他因素（如評論）也會影響位置。

## 比對產品

當您比對產品時，Channel Manager會將產品資料傳送至 [!DNL Walmart Marketplace] 若要搜尋具有符合對應之屬性值的現有清單 [!DNL Commerce] 產品屬性。 符合條件由 [attribute-mapping設定](map-catalog-attributes.md) （針對您的商店頻道）。

如果找到相符專案，則會更新現有產品清單以新增您的優惠方案。

### 必要條件

在比對產品之前，請確認您的產品目錄屬性值符合Walmart要求，並設定產品屬性設定。 另請參閱 [對應目錄屬性](map-catalog-attributes.md).

#### 選取並比對產品

1. 開啟連線的銷售管道。

1. 從 **[!UICONTROL Listings]**，選取產品以比對 *[!UICONTROL Draft]* 狀態。

   ![從清單中選取產品並傳送以進行比對](assets/products-in-marketplace-sales-channel.png)

1. 選取 **[!UICONTROL Match Products]**.

   訊息會指出為了比對而傳送的產品數量。

   所選產品的狀態變更為 [!UICONTROL *處理中*] 直到比對作業完成為止。 Walmart Marketplace最多可能需要30分鐘才能完成比對作業。

### 檢查比對狀態

比對完成後，選取 **[!UICONTROL Refresh products]** 以檢視目前的產品狀態。 *符合* 或 *錯誤*.

- **[!UICONTROL Match]** 表示產品已成功比對。 您的產品選件已連線至沃爾瑪市集清單。 如果 [Marketplace商店未啟用](walmart-requirements.md#walmart-marketplace-store-status)， *[!UICONTROL Staged for Match]* 會顯示在 *[!UICONTROL Status detail]* 欄。 當以下情況發生時，分段產品會自動連線： [!DNL Walmart Marketplace] 存放區已啟用。

- **[!UICONTROL Error]** 指出比對作業因下列其中一個問題而失敗：

   - [!DNL Channel Manager] 由於連線問題，無法傳送以進行比對。

   - 找不到相符專案。

   - 找到相符專案，但清單無法連線，因為 [!DNL Walmart Marketplace] 傳回錯誤碼。 請參閱 **[!UICONTROL Error Description]** 以取得問題的相關資訊。

### 檢視沃爾瑪的清單

比對產品後，請檢閱更新的產品清單，並從以下位置驗證產品詳細資料、價格和存貨數量： [[!UICONTROL Walmart Marketplace Seller Account Items] 儀表板](https://seller.walmart.com/items-and-inventory/manage-items) 以檢閱更新的產品。

### 產品比對錯誤疑難排解

如果產品比對作業失敗並出現錯誤，則錯誤訊息會顯示在 *[!UICONTROL Status detail]* 中的欄 [!UICONTROL Channel Manager] 產品清單。

傳回的常見錯誤為產品ID值的格式不正確或缺少必要的屬性。

#### 修正產品ID值

| 型別 | 說明 | 範例 |
|------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| UPC | GTIN-12,12位數的數字，包含檢查位數。 </br></br>如果您的UPC少於12位數，例如UPC-E為8位數，請新增結尾零以符合需求。 | 變更自 `45678912345` 至 `045678912345` |
| GTIN | GTIN-14,14位數的數字，包含檢查位數。 </br></br>如果您的GTIN少於14位數，請新增前導零 </br>以符合需求。 | 變更 `456789123456` 至 `0045678912345` |
| EAN | GTIN-13,13位數的數字，包含檢查位數。 </br></br>如果您的EAN少於13位數，請新增行距 </br>零以符合需求。 | 變更自 `4567891234` 至 `0004567891234` |

如需Walmart Marketplace錯誤碼的詳細資訊，請參閱 [沃爾瑪賣家說明](https://sellerhelp.walmart.com/s/guide?article=000005844).

## 上傳新產品清單

若產品在沃爾瑪市集中沒有匹配項，請使用沃爾瑪產品類別Excel範本，大量上傳產品清單。 您會使用從匯出的產品目錄資料填入Walmart範本 [!DNL Commerce] 執行個體。

關於新產品清單，請檢查您的產品目錄，以確保您計畫在Walmart Marketplace上銷售的產品具有Walmart Marketplace產品清單所需的屬性。

**Walmart Marketplace清單 — 屬性需求**

| **屬性** | **需求層級** |
|--------------------------|-----------------------|
| SKU | 必填 |
| 產品名稱 | 必填 |
| 產品ID型別 | 必填 |
| 產品ID | 必填 |
| 品牌 | 必填 |
| 簡短說明 | 必填 |
| 售價 | 必填 |
| 網站說明 | 必填 |
| 主要影像URL | 必填 |
| 送貨重量 | 必填 |
| 主要功能 | 建議 |
| 型號 | 建議 |
| 製造商名稱 | 建議 |
| 製造商零件編號 | 建議 |
| 大小 | 建議 |
| 顏色 | 建議 |
| 主要影像URL | 可選 |
| 其他影像URL | 可選 |
| 製造商 | 可選 |

### 必要條件

- 確認您符合 [沃爾瑪要求](walmart-requirements.md).

- 在您的 [!DNL Commerce] 產品目錄，確認要在Walmart Marketplace上列出的產品的目錄設定具有所有必要的屬性，並符合Walmart Marketplace內容准則。

- 確認cron工作正在執行中，以完成匯出操作。

   - 如需內部部署執行個體，請參閱 [設定並執行cron](https://devdocs.magento.com/guides/v2.4/config-guide/cli/config-cli-subcommands-cron.html).

   - 如需Adobe雲端基礎結構的相關資訊，請參閱 [設定cron工作](https://devdocs.magento.com/cloud/configure/setup-cron-jobs.html).

### 建立要上傳的產品資料檔案

1. 從您的 [沃爾瑪賣家帳戶](https://login.account.wal-mart.com/authorize?responseType=code&amp;clientId=66620dfd-1f3f-479b-8b9c-e11f36c5438b&amp;scope=openId&amp;redirectUri=https://seller.walmart.com/resource/login/sso/torbit&amp;nonce=SX17QLMBKR&amp;state=ZBWWNZXXXM&amp;clientType=seller)，從Walmart賣家中心下載產品清單範本。

   - 從產品目錄專案頁面中，選取 **[!UICONTROL Add Items]**. 然後，選取 **[!UICONTROL Add items in bulk]**.

      ![在Walmart Marketplace專案組態中新增大量專案選項](assets/walmart-seller-account-add-items-bulk.png)

   - 在下載頁面上，選取 **[!UICONTROL Full Setup]**. 然後，選取料號分類並下載分類範本。

      ![在Walmart Marketplace專案設定中下載類別範本選項](assets/walmart-seller-account-full-setup-download.png)

   - 確認範本包含產品清單的必要和建議屬性。

1. 從 [!DNL Commerce] 管理員，從Adobe中選取要匯出的產品資料 [!DNL Commerce] 網站。

   - 從「管理員」中選取「 」 [!UICONTROL **系統** >資料傳輸> **匯出**].

   - 於 [!UICONTROL Export] 中的頁面 [!UICONTROL Entity Type] 欄位，選取 [!UICONTROL **產品**].

   - 在 [!UICONTROL Entity Attributes] 表格中，設定產品資料匯出的選取條件。
   ![在中匯出產品資料頁面 [!UICONTROL [!DNL Commerce] Admin]](assets/walmart-seller-account-full-setup-download.png)

   使用篩選條件來選取和設定屬性值，這些屬性值適用於您銷售的產品類別。 請務必加入沃爾瑪必要和建議的屬性。 (請參閱 [匯出資料](https://docs.magento.com/user-guide/system/data-export.html) 在Adobe中 [!DNL Commerce] 使用手冊以取得詳細指示。)

   若要在匯出中省略屬性，請選取 [!UICONTROL **排除**] 核取方塊。

1. 捲動至屬性表格的結尾並選取 [!UICONTROL **繼續**] 以開始匯出資料。

   CSV匯出檔案會透過訊息佇列使用cron工作進行處理，並儲存在 `var/export/folder`. (請參閱 [管理訊息佇列](https://devdocs.magento.com/guides/v2.4/config-guide/mq/manage-message-queues.html) 在 *Commerce開發人員指南*.)

1. 開啟Walmart Marketplace產品類別的Excel範本，並使用Excel巨集功能將匯出的產品資料合併至Excel範本。

1. 上傳含有已匯出產品資料的Excel檔案。

   - 返回「 」中的「產品目錄專案」頁面 [沃爾瑪賣家中心](https://login.account.wal-mart.com/authorize?responseType=code&amp;clientId=66620dfd-1f3f-479b-8b9c-e11f36c5438b&amp;scope=openId&amp;redirectUri=https://seller.walmart.com/resource/login/sso/torbit&amp;nonce=SX17QLMBKR&amp;state=ZBWWNZXXXM&amp;clientType=seller).

   - 選取 [!UICONTROL **新增專案** > **大量新增專案**].
   - 將完成的試算表拖曳至「上傳」區段。
   - 選取 [!UICONTROL **提交**].
   - 選取&#x200B;[!UICONTROL  **活動資訊源**] 以檢視進度。

如需完整指示，請參閱 [使用完整專案規格大量新增專案](https://sellerhelp.walmart.com/s/guide?article=000007680) 在 [!DNL *沃爾瑪賣家說明*].
