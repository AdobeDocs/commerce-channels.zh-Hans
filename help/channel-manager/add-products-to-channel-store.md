---
title: 新增產品至管道管理員
description: '''建立產品分類 [!DNL Walmart Marketplace] 將目錄中的產品新增至在「管道管理員」中設定的銷售管道進行銷售。 '
exl-id: 00932df7-bdc7-42a1-b269-88dffcc918bc
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 0%

---


# 將產品新增至 [!DNL Channel Manager]

若要將產品新增至 [!DNL Walmart Marketplace] sales channel，請從 [!DNL Commerce] 產品目錄並將其匯入 [!DNL Channel Manager].
視您選取的產品數量而定，匯入程式最多可能需要30分鐘或更長時間。

## 先決條件

**[對應目錄屬性](map-catalog-attributes.md)** — 在 [!DNL Channel Settings] 設定，從以下位置至少對應一個屬性： [!DNL Commerce] 產品目錄至其中一個必要的沃爾瑪產品識別碼 — GTIN、ISBN、ISSN、UPC、EAN。

## 清單需求

[!DNL Commerce] 產品清單必須具備下列必要的屬性組態：

- **[!UICONTROL Connect to Channel Manager]** 屬性已啟用

- 為必要的Walmart屬性提供有效值。

   - 至少一個產品屬性符合其中一個必要屬性 [!DNL Walmart Marketplace] 產品識別碼 — GTIN、ISBN、ISSN、UPC、EAN。

   - 例如，產品價格指定至最多兩位小數 `9.99`

   - 例如，產品權重指定至最多兩位小數 `1.25`

>[!TIP]
>
>如需針對您的銷售管道最佳化清單的其他資訊，請參閱 [Walmart Marketplace清單品質最佳化指南](https://marketplace.walmart.com/wp-content/uploads/2020/09/WMP_listing_quality_optimization_guide.pdf).

## 新增產品

1. 從連線的銷售管道商店中，選取 **新增產品** 以開啟產品目錄。

   ![新增產品至銷售管道商店](assets/add-initial-products-to-connected-channel.png)

   目錄會在新標籤中開啟。

1. 從目錄產品格線中，選取銷售產品 [!DNL Walmart Marketplace].

   ![將產品傳送至銷售管道商店](assets/select-products-from-catalog.png)

1. 啟用 **[!UICONTROL Connect to Channel Manager]** 所選專案的屬性。

   - 從 **[!UICONTROL Actions]**，選取 **[!UICONTROL Update attributes]**.

   - 捲動至 **[!UICONTROL Connect to Channel Manager]** 屬性並啟用它。

   - 確認產品屬性至少包含其中一個必要專案 [!DNL Walmart Product IDs].

   - 選取 **[!UICONTROL Save]**.

      確認訊息隨即顯示。

      ![從目錄匯入產品至銷售管道確認訊息](assets/product-import-from-catalog-confirmation.png)

      如果訊息指出已排程更新，請使用 [佇列:consumers:開始](https://devdocs.magento.com/guides/v2.4/config-guide/cli/config-cli-subcommands-queue.html) [!DNL CLI] 立即處理更新的命令。

      ```bash
      $ bin/magento queue:consumers:start product_action_attribute.update
      ```

1. 匯入作業完成後，請回到以驗證您新增的產品 [!DNL Channel Manager] 並選取 **[!UICONTROL Listings]**.

   最初，產品位於 *草稿* 狀態。 選取 **[!UICONTROL Refresh products]** 以更新表格。

1. 選取「 」，更新檢視以顯示新增至「管道管理員」的新產品 **[!UICONTROL Draft]** 狀態卡。

   ![產品已匯入連線銷售管道](assets/products-in-marketplace-sales-channel.png)


