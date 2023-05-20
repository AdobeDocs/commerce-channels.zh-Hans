---
title: 預先設定任務
description: 在AmazonSales Channel中整合Adobe Commerce或Magento Open Source商店之前，請先檢閱要完成的必要工作。
exl-id: eb9d9136-925f-4b20-9d65-b166173f434b
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '871'
ht-degree: 0%

---

# 預先設定任務

早於 [存放區整合](./store-integration.md)，您必須確保 [!DNL Amazon Seller Central] 帳戶與您的 [!DNL Commerce] 帳戶已準備好進行整合。 為了成功整合，有一些必要的預先設定工作。

當您在Amazon sales channel中設定第一個Amazon商店時，會出現設定工作清單。 建議您先檢閱這些工作 [新增Amazon存放區](./store-integration.md). 新增您的第一個商店後，您可以在Amazon銷售管道的「學習和準備」檢視中檢視這些任務 [首頁](./amazon-sales-channel-home.md).

## 1.在中啟用背景工作 [!DNL Commerce]

所有產品和資料都同步於 [!DNL Commerce] 而Amazon是由 [cron工作](https://docs.magento.com/user-guide/system/cron.html){target="_blank"}. 當您完成新增或更新清單和接收訂單等作業時，cron工作會在您之間 [!DNL Commerce] 後端與您的 [!DNL Amazon Seller Central] 帳戶。

- [啟用 [!DNL Commerce] cron](https://docs.magento.com/user-guide/system/cron.html){target="_blank"}.

- 為獲得最佳效能， [set [!DNL Commerce] cron](https://docs.magento.com/user-guide/configuration/advanced/system.html){target="_blank"} 每五分鐘執行一次。

## 2.建立您的 [!DNL Amazon Seller Central] 帳戶

在開始設定Amazon銷售管道之前，您必須擁有使用中 [!DNL Amazon Seller Central] 帳戶。 如果您在中沒有Amazon賣家帳戶 [北美（美國、加拿大、MX）](https://sell.amazon.com/){target="_blank"} or [European (UK)](https://sell.amazon.co.uk/sell-online/beginners-guide){target="_blank"} 區域，您可以完成Amazon的賣家帳戶設定程式。

Amazon sales channel需要 [!DNL Professional Seller] 帳戶於 [!DNL Amazon Seller Central]. Amazon每月會收取訂閱及銷售費用。 另請參閱 [Amazon：選擇您的銷售計畫](https://sell.amazon.com/pricing.html){target="_blank"}.

## 3.確認您是獲認可的Amazon銷售商

若要整合，您必須擁有核准許可權 [!DNL Amazon Seller Central] 帳戶。 您的帳戶對產品或類別不得有任何限制。 有些產品和類別在建立清單之前需要核准。 檢閱類別和產品核准的Amazon原則，以確保您的產品獲得核准。 另請參閱 [Amazon：需要核准的類別和產品](https://sellercentral.amazon.com/gp/help/200333160){target="_blank"} （需要使用Seller Central登入）。

同樣重要的是，請確定您已在 [!DNL Amazon Seller Central] 帳戶：

- 確保您的退貨政策與Amazon退貨政策相同或更好。 另請參閱 [Amazon：回訪政策](https://www.amazon.com/gp/help/customer/display.html){target="_blank"}.

- 確定已設定您的稅捐設定。 另請參閱 [Amazon：稅務政策](https://sellercentral.amazon.com/gp/help/external/help.html){target="_blank"} （需要使用Seller Central登入）。

- 確保正確設定您的送貨方法。 若要設定符合下列條件的送貨方法： [!DNL Commerce] 提供給客戶以履行您的Amazon訂單，更新 [Amazon：送貨設定](https://sellercentral.amazon.com/sbr/ref=xx_shipset_dnav_xx#shipping_templates){target="_blank"} 在您的 [!DNL Amazon Seller Central] 帳戶。

## 4.確定已為商店設定您的VAT

（主要供英國賣家使用。） Amazon建議註冊 [Amazon VAT計算服務](https://sell.amazon.co.uk/learn/vat-resources#vat-services-on-amazon){target="_blank"}. 若您選擇不同的方式，則您需負責VAT法規遵循。

>[!NOTE]
>
>Amazon可能需要10至14天的時間來驗證及啟用您的VAT計算服務帳戶。

## 5.增加自動目錄相符專案的數量

在上線期間，Amazon銷售管道會使用產品屬性，將您現有的Amazon清單（如果適用）與您現有的產品進行比對 [!DNL Commerce] 目錄。 上線後，這些產品屬性會用於發佈您的 [!DNL Commerce] 將目錄專案新增至Amazon清單，並將您的產品資料同步到 [!DNL Commerce] 和Amazon。

擁有最高數量的 [!DNL Commerce] 產品會自動符合Amazon清單，您應該為您的建立一組產品屬性， [!DNL Commerce] 目錄。 在設定Amazon銷售管道商店之前，您應該先新增 [!DNL Commerce] 產品屬性以符合這些Amazon屬性，例如：ASIN、EAN、ISBN、UPC或GCID。 另請參閱 [在中建立產品屬性 [!DNL Commerce]](./ob-creating-magento-attributes.md).

## 6.視需要設定貨幣和轉換

如果您的Amazon商店使用的貨幣與為設定的貨幣不同 [!DNL Commerce] 商店， [啟用貨幣](https://docs.magento.com/user-guide/configuration/general/currency-setup.html){target="_blank"} and set the [currency conversion rate](https://docs.magento.com/user-guide/stores/currency-update.html){target="_blank"}.

## 7.建立產品條件屬性（視需要）

如果您的Amazon清單包含多個產品條件(例如 _新_， _已使用_，或 _喜歡新的_)，建立 [!DNL Commerce] 屬性和指派條件值。 您必須在上線期間將此屬性對應至Amazon條件產品屬性。 另請參閱 [建立Amazon的屬性](./ob-creating-magento-attributes.md).

## 8.設定您的 [!DNL Amazon Seller Central] 送貨方法

若要設定您要提供的送貨方式，以完成Amazon訂單，請參閱 [設定和送貨設定][10] 在您的 [!DNL Amazon Seller Central] 帳戶。

## 其他設定

設定並啟用Amazon帳戶時，會有數個專案 [!DNL Commerce] 有助於簡化Amazon銷售管道上線流程的建議。

### 檢閱並記下您要排除的任何產品

您可能不希望某些產品列在Amazon上。 Amazon sales channel有一個清單規則引擎，可用來判斷哪些產品符合發佈至Amazon的資格。 [清單規則](./listing-rules.md) 可讓您選取要發佈（或未發佈）至您的產品的子集 [!DNL Amazon Seller Central] 帳戶，例如依類別選取或定義一或多個產品屬性。 按讚 [!DNL Commerce] [目錄](https://docs.magento.com/user-guide/marketing/price-rules-catalog.html){target="_blank"} or [shopping cart](https://docs.magento.com/user-guide/marketing/price-rules-cart.html){target="_blank"} price rules, product attributes used for Amazon listing eligibility must have **[!UICONTROL Use for Promo Rule Conditions]** set to `Yes`. See the **[!UICONTROL Use for Promo Rule Conditions]** in [Product Attributes](https://docs.magento.com/user-guide/stores/attributes-product.html){target="_blank"}.

### 設定您的 [!DNL Amazon Seller Central] 區域至非使用中

為協助在整合期間順利轉換資料，建議您將Amazon區域設為 `Inactive` 「設定>帳戶資訊>休假設定」中的狀態。 請參閱 [Amazon：休假的清單狀態][11]. 完成設定後，將狀態變更回 `Active` 在Amazon中。

![「下一步」圖示](assets/btn-next.png) [**繼續建立 [!DNL Commerce] 屬性**](./ob-creating-magento-attributes.md)
