---
title: '連線 [!DNL Channel Manager] 至 [!DNL Walmart Marketplace]'
description: 將Commerce商店檢視連線至 [!DNL Walmart Marketplace] 建立銷售管道，以管理Commerce產品清單、存貨、價格和Walmart Marketplace銷售訂單。」
exl-id: 8c78c582-7b57-4f73-894e-134ba0ba3640
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%

---

# Connect [!DNL Channel Manager] 至 [!DNL Walmart Marketplace]

在您的裝置上安裝「頻道管理員」後 [!DNL Commerce] 執行個體，在Channel Manager中建立Sales Channel並設定要連線的認證 [!DNL Channel Manager] 至 [!DNL Walmart Marketplace].

1. [建立銷售管道](#create-the-sales-channel) 藉由選取 [!DNL Commerce] 用於產品清單的商店。

1. [將頻道連線至 [!DNL Walmart Marketplace] 藉由新增 [!UICONTROL Walmart API credentials]](#connect-the-channel-to-walmart-marketplace).

1. [完成銷售管道設定](#complete-sales-channel-store-setup) 若要管理清單、存貨、訂價及訂單，請執行下列步驟： [!DNL Walmart Marketplace] 產品分類。

>[!NOTE]
>
>「通路管理員」需要在Walmart帳戶和 [!DNL Commerce] 存放區檢視。 您無法將相同的商店檢視連線到多個Walmart帳戶。

## 建立銷售管道

1. 從管理員中，開啟 [!DNL Channel Manager] 藉由選取 **[!UICONTROL Marketing** > _頻道&#x200B;_> **頻道管理員]**.

1. 在 **[!UICONTROL Marketplaces available to connect]** 區段，選取 **[!UICONTROL Get Started]**.

   ![連線新增 [!DNL Walmart] 儲存至 [!DNL Channel Manager]](assets/channel-manager-home.png)

1. 如有需要，請設定 [!DNL Walmart Marketplace Seller] 帳戶。

1. 設定存放區和連線：

   - 選取 **[!UICONTROL Add Credentials]**.

   - 選取 [!DNL Commerce] 提供您要在Marketplace上銷售之產品的商店檢視。

      ![設定之間的連線 [!DNL Commerce] 和 [!DNL Walmart Marketplace] 從 [!DNL Channel Manager]](assets/configure-commerce-to-marketplace-connection.png)

   - 輸入唯一值 **[!UICONTROL store name]**.

   - 選取 **[!UICONTROL Adobe [!DNL Commerce] site]** 用於產品清單和訂單處理。

   - 若要接收相關通知，請執行下列動作： [!DNL Channel Manager]，新增 **[!UICONTROL email address]**.

1. 將頻道連線至 [!DNL Walmart Marketplace].

   - 為新增認證 [[!DNL Walmart Marketplace Adobe Production API key]](walmart-requirements.md#generate-a-walmart-marketplace-production-api-key) 從您的 [!DNL Walmart Marketplace Seller] 帳戶。

   - 如果您沒有認證，請從 [!DNL Walmart Marketplace Developer Portal] 藉由選取 **[!UICONTROL Get API credentials]**.

      在開發人員入口網站上，選取您所在的地區（美國和加拿大），然後登入。

      ![[!DNL Walmart Marketplace] 帳戶登入](assets/walmart-marketplace-login-page.png)

   - 在API金鑰表單上，複製並儲存 **[!UICONTROL Client ID]** 和 **[!UICONTROL Client Secret]** 的值 [!UICONTROL Adobe Inc Production API key] 至安全位置。

      ![[!DNL Walmart Marketplace API key] 設定頁面](assets/walmart-api-key-management-form.png)

      >[!NOTE]
      >
      >如果 [!DNL Adobe Inc] 金鑰未列在開發人員入口網站中，請選取 **[!UICONTROL Add New Key for a Solution Provider]** 以設定許可權並產生金鑰。 如需設定詳細資訊，請參閱 [產生 [!DNL Walmart Marketplace API Key]](walmart-requirements.md#generate-a-walmart-marketplace-api-key).

   - 返回至 [!DNL Channel Manager] 將認證新增至 **[!UICONTROL Walmart Connection]** 資訊。

      當您新增認證時，Adobe會隱藏使用者端密碼，並將值儲存在安全的儲存庫中。

1. 選取 **[!UICONTROL Save Store]** 以套用設定並連線至 [!DNL Walmart marketplace].

1. 成功連線後， [完成商店設定](complete-sales-channel-store-setup.md) 從 **[!UICONTROL Channel Manager]** 商店頁面。

![設定第一個存放區](assets/channel-manager-setup-first-store.png)

### 疑難排解連線問題

如果連線到 [!DNL Walmart] 失敗，請參閱 [沃爾瑪市集常見問題集](https://developer.walmart.com/faq/us/faq-auth/){target="_blank"} 以取得疑難排解提示。

- 從 [!DNL Walmart Developer Portal]，確認您為的生產API金鑰複製了正確的認證 [!UICONTROL Adobe Inc.]

- 驗證「 」的存取設定 [!UICONTROL Walmart Adobe API key] 具有正確的許可權。 另請參閱 [[!DNL Walmart Requirements]](walmart-requirements.md##generate-a-walmart-marketplace-api-key).

- 確認 [!DNL Walmart API] 服務可從以下網址取得： [Walmart API狀態頁面](https://developer.walmart.com/us/whats-new/new-api-status-information-now-available/){target="_blank"}.
