---
title: 對應目錄屬性
description: '對應屬性以符合[DNL！ Commerce]產品至現有 [!DNL Walmart Marketplace] 清單和同步資料 [!DNL Channel Manager] 和 [!DNL Walmart].'
exl-id: 6678d81f-d167-460d-b656-d082d56f670c
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---

# 對應目錄屬性

從以下連結清單之前： [!DNL Commerce] 至 [!DNL Walmart Marketplace]，您必須至少對應一個唯一識別碼， [!DNL Commerce] 類別目錄至來自Walmart的對應識別碼。

需要此步驟才能比對 [!DNL Commerce] 產品至現有 [!DNL Walmart] 清單及同步化產品資料的方式 [!DNL Commerce] 和 [!DNL Walmart]. 此 [!DNL Commerce] 產品必須至少有一個產品屬性符合以下所需的產品識別碼（產品ID）之一 [!DNL Walmart].

**必填 [!DNL Walmart] 產品ID**

| **接受的型別** | **名稱** | **用途** | **可接受位數** |
|-------------------|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| GTIN | 全球貿易專案 | 一般用途，全球使用 | 14位數 |
| ISBN | 國際標準書號 | 平裝本、精裝本及電子書 | 10或13位數 |
| ISSN | 國際標準序號 | 8位數的序號，用於識別所有媒體印刷和電子媒體上所遞送的各類雜誌、期刊、報章和期刊 | 8位數 |
| UPC | 通用產品代碼 | 標準零售追蹤代碼 | 12位數 |

如果您的目錄沒有相符的屬性， [新增或轉換現有的目錄屬性](https://docs.magento.com/user-guide/catalog/product-attributes.html).

## 對應唯一識別碼

1. 從 **[!UICONTROL Listings]** 或 **[!UICONTROL Orders]** 銷售管道商店的頁面，選取 **[!UICONTROL Channel Settings]**.

1. 開啟 **[!UICONTROL Channel Settings]**，選取 **[!UICONTROL Map Attributes]**.

   - 尋找 [!DNL Walmart Marketplace] 要對應的屬性。

   - 從中選擇對應的屬性 [!DNL Commerce] 存放區目錄。

      以下範例對應 [!UICONTROL Walmart Marketplace UPC] 屬性至產品目錄中的UPC屬性。

      ![對應產品符合條件的屬性](assets/products-map-attributes-for-match.png)

   - 選取 **[!UICONTROL Save]**.
