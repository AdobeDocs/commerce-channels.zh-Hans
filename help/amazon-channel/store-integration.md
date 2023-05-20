---
title: 存放區整合
description: 開始入門流程之前，您必須建立（新增） AmazonSales Channel商店，並將其連結至您的Amazon賣家帳戶。
exl-id: ea79e91d-7d92-4992-a921-7ac7632a0519
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 0%

---

# 存放區整合

若要開始使用Amazon銷售管道，您必須建立（新增） Amazon銷售管道商店，並將其連結至您的Amazon賣家帳戶。 這兩個步驟會整合 [!DNL Commerce] 和Amazon帳戶共用資料、同步產品等。

_您需要的主要登入認證 [!DNL Amazon Seller Central] 帳戶（用來建立賣家帳戶的電子郵件或電話）以連線您的商店。_

>[!NOTE]
>
>第一次整合商店後，系統會每年提示您重新授予存取權，以續約您與Amazon的Amazon銷售管道連線。 您可以在下列位置更新或撤銷此授權： _目前的授權_ 中的表格 _Amazon MWS開發人員許可權_ 部分 **設定** > **使用者許可權** Seller Central帳戶頁面。

## 新增Amazon存放區

1. 於 _管理員_ 側欄，前往 **行銷** > _頻道_ > **AmazonSales Channel**.

   新增您的第一個Amazon銷售管道商店時， _預先設定任務_ 強制回應視窗隨即顯示。 新增第一個商店後，您可在以下位置存取預先設定工作： [Amazon銷售管道首頁](./amazon-sales-channel-home.md) 頁面於 _學習與準備_ 在左側功能表中。

1. 按一下 **[!UICONTROL Add Amazon Store]**.

   此 _[!UICONTROL Add Amazon sales channel]_頁面隨即開啟。

   ![新增Amazon sales channel store](assets/amazon-store-integration.png)

1. 對象 **[!UICONTROL Magento Website to use for Amazon Listing]**，選擇您的 [!DNL Commerce] 為此Amazon sales channel商店連線的網站。

   此設定也會定義預設值 [!DNL Commerce] 儲存對象 [匯入Amazon訂單](./order-settings.md).

1. 對象 **[!UICONTROL Email Address]**，請輸入您偏好的連絡人電子郵件地址。

1. 對象 **[!UICONTROL New Store Name]**，為您新的Amazon銷售管道商店輸入描述性名稱。

   >[!NOTE]
   >
   >此名稱會用作 [!DNL Commerce] 僅供參考，並在上識別存放區 [Amazon銷售管道首頁](./amazon-sales-channel-home.md) 頁面。 您希望讓您的團隊能夠輕鬆識別它。 例如，您在美國地區銷售的Amazon商店可能會命名為 `Amazon Store USA`.

1. 對象 **[!UICONTROL Amazon Marketplace Country]**，選擇此Amazon銷售管道商店銷售產品的地區/國家。 選項：

   - 美國
   - 加拿大
   - 墨西哥
   - 英國

1. 在 _[!UICONTROL Map your Magento attributes to Amazon]_區段，請執行下列動作：

   - 對象 **[!UICONTROL Product ID on the Amazon market]**，選擇要對應至的Amazon屬性 [!DNL Commerce] 屬性已選取如下。

      此ID可協助您正確比對產品在 [!DNL Commerce] 目錄。

   - 對象 **[!UICONTROL Map a Magento attribute]**，選擇 [!DNL Commerce] 對應至上述所選Amazon屬性的產品屬性。

      [對應屬性](./ob-creating-magento-attributes.md) 有助於確保您的Amazon清單正確符合中的對應產品 [!DNL Commerce] 目錄。

1. 按一下 **[!UICONTROL Connect]**.

   對話方塊關閉，新存放區出現在 [Amazon銷售管道首頁](./amazon-sales-channel-home.md) 頁面，其中包含確認訊息。

## 將存放區連線至 [!DNL Amazon Seller Central]

1. 在商店控制面板上，按一下 **[!UICONTROL Connect store]** 在要啟動的商店卡片上 [!DNL Amazon Seller Central] 在新標籤中。

1. 輸入您的 [!DNL Amazon Seller Central] 帳戶認證，然後按一下 **[!UICONTROL Sign in]**.

   若要完成此連線，您必須登入 [!DNL Amazon Seller Central] 使用主要使用者登入憑證的帳戶（用來建立賣家帳戶的電子郵件或電話）。

1. 如果出現提示，請輸入您從Amazon收到的程式碼，然後按一下，以完成Amazon雙因素授權(2FA) **[!UICONTROL Sign in]**.

1. 於 _[!UICONTROL Amazon Marketplace Web Service]_確認頁面，選取&quot;[!UICONTROL I understand...]」核取方塊並按一下&#x200B;**[!UICONTROL Next]**.

1. 於 _[!UICONTROL You are almost done]_訊息，按一下&#x200B;**[!UICONTROL Continue]**.

   您已授予Amazon Sales Channel存取許可權並與您共用資料 [!DNL Amazon Seller Central] 帳戶。 Amazon頁面會關閉，並顯示確認訊息。

   此 [Amazon銷售管道首頁](./amazon-sales-channel-home.md) 頁面開啟，顯示您的Amazon商店卡片。

   若要檢視商店儀表板，請按一下 **[!UICONTROL View Store]** 在商店資訊卡上。

![Amazon銷售管道首頁（含新商店卡）](assets/asc-dashboard-after-2fa.png)

您新的Amazon銷售管道商店現在已連線至您的 [!DNL Amazon Seller Central] 帳戶。

![「下一步」圖示](assets/btn-next.png) [**繼續建立清單規則**](./ob-create-listing-rule.md)
