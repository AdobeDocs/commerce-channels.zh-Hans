---
title: Amazon銷售管道的最佳作法和限制
description: 檢閱針對Adobe Commerce和Magento Open Source使用Amazon銷售管道時的最佳實務和限制。
exl-id: 7f7faae1-7aa7-413c-b534-1039e6a35173
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---

# AmazonSales Channel的最佳作法和限制

最佳實務包括：

- Amazon sales channel可以透過提高或降低價格、同步產品資訊（包括可用存貨），以及新增、更新和結束（刪除）清單來影響您的Amazon清單。 在設定期間依狀態檢閱您的清單，並調整您的設定([清單設定](./listing-settings.md)， [清單規則](./listing-rules.md)， [定價規則](./pricing-products.md)， [覆寫](./overrides.md)、等等)之後再進行商店設定。 這些設定也可以在設定後視需要修改。

- Amazon sales channel可以設定您的定價規則，以自動調整您的掛牌價格。 自動化定價保障包括 [底價](./floor-price.md) 和 [選擇性最高價格](./optional-ceiling-price.md) 的功能 [智慧型重新訂價規則](./intelligent-repricing-rules.md). 使用這些保障措施有助於確保您的上市價格不會低於您的成本或高於定義的價格。

- Amazon sales channel與Amazon之間的資料同步由您的控制 [[!DNL Commerce] cron](https://docs.magento.com/user-guide/system/cron.html){target="_blank"} 設定。 內建節流，介於 [!DNL Commerce] 和Amazon有助於確保順暢且有效率的資料傳輸，但在電子商務高流量時段（例如黑色星期五），Amazon的系統更新時間可能會比平常長。 設定您的 [!DNL Commerce] cron每五分鐘執行一次。

- Amazon sales channel會匯入您的Amazon訂單資訊。 若要在Amazon sales channel中管理Amazon訂單，您必須確保 [訂單設定](./order-settings.md) 定義來匯入及建立對應的 [!DNL Commerce] 每個Amazon訂單的訂單。 如果未定義，則只能檢視您的Amazon訂單資訊。 所有透過Amazon的銷售稅捐，仍透過您的 [!DNL Amazon Seller Central] 帳戶。 某些州會要求Amazon自動收取及匯出稅金。 對於其他州，銷售者可以選擇手動或自動計算稅捐。 另請參閱 [Amazon：稅務政策](https://sellercentral.amazon.com/gp/help/external/help.html?itemID=200405820&amp;language=en_US/){target="_blank"}. 您可能需要登入 [!DNL Amazon Seller Central] 可檢視Amazon稅務政策檔案的帳戶。

- 針對英國地區，最佳實務是註冊 [Amazon VAT計算服務](https://sell.amazon.co.uk/learn/vat-resources/){target="_blank"} 上線Amazon sales channel之前。


   >[!NOTE]
   >
   >Amazon可能需要10至14天的時間來驗證及啟用您的VAT計算服務帳戶。

限制包括：

- 屬於您的套裝、禮品卡和分組產品型別 [!DNL Commerce] Amazon sales channel不支援將目錄列為Amazon。

- Amazon sales channel無法為沒有現有或先前Amazon清單的產品建立清單。 如果產品不存在於 [!DNL Amazon Seller Central] 若使用ASIN，則必須將其新增至 [!DNL Amazon Seller Central] 以便Amazon可以將產品指派給ASIN。 在Amazon中新增產品並建立清單後，該清單即可與Amazon銷售管道中的目錄比對並同步。
