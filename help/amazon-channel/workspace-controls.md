---
title: 工作區控制項
description: AmazonSales Channel提供工作區控制項，可協助您找出清單、檢視資訊，以及輕鬆套用動作。
exl-id: 4f76b1d0-ae58-435b-bd6d-50155a023421
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 0%

---

# 工作區控制項

Amazon銷售管道 [首頁](./amazon-sales-channel-home.md) 有一些常見的工作區控制項，包括篩選器、預設檢視、欄和匯出。 並非所有頁面都具有相同的控制選項。

![AmazonSales Channel工作區控制項範例](assets/amazon-workspace-controls.png)

## 動作

此 _[!UICONTROL Actions]_選擇器提供使用者可用於頁面的動作清單。 選取後，動作會套用至所有選取的專案。 若要將動作套用至特定專案，請選取每個專案第一欄中的核取方塊，然後選擇下方的選項_[!UICONTROL Actions]_.

例如，當選取器顯示在 _[!UICONTROL Attributes]_頁面中，包含_[!UICONTROL Re-import Product Attribute Values]_ 動作。 選擇此動作會偵測對應 [!DNL Amazon Seller Central] 帳戶並重新整理 [!DNL Commerce] 在左側欄中勾選每個Amazon存放區專案的資料。

![動作功能表範例](assets/amazon-sales-channel-home-actions-option.png)

## 篩選器

此 _[!UICONTROL Filters]_控制項顯示縮小表格中所顯示資料範圍的選項。 篩選選項是根據在「欄」控制項中選取的欄而定。 篩選選項只會顯示在「欄」控制項中啟用的欄。

篩選器控制項可包含用於縮小指定日期資料範圍的動態行事曆、具有預先定義選取範圍的欄的下拉式功能表，以及可能包含自訂資料的任意文字欄位。

下列範例顯示篩選訂單清單的設定，以僅顯示符合以下條件的訂單：

- 在2019年2月1日到2019年2月7日之間所下的訂單，以及
- 採購員為的訂單 `Smith`、和
- 狀態為「 」的訂單 `Shipped`.

設定好篩選選項後，按一下 **[!UICONTROL Apply Filters]** 以篩選列出的資料。 按一下「取消」結束「篩選器」控制項而不套用。

![篩選器控制項範例](assets/workspace-controls-filters.png)

將篩選器套用至資料後， **[!UICONTROL Active Filters]** 資訊隨即顯示。 您可以按一下 ![清除篩選器圖示](assets/x-icon-clear-filters.png) 圖示以清除特定的篩選選項，或按一下 **[!UICONTROL Clear All]** 以清除所有套用的篩選器。

![作用中篩選器範例](assets/applied-filters-line.png)

## 檢視

「檢視」控制項以頁面的預設欄為基礎，因此命名為「預設檢視」。 您可以使用「欄」控制項來新增或移除可用的欄。 當您自訂欄時，隨後可以將檢視儲存為「檢視」控制項中的自訂檢視。

當您在頁面顯示中新增或移除欄時：

1. 按一下 **[!UICONTROL Default View]** > **[!UICONTROL Save View As...]**.

1. 輸入檢視的名稱。

1. 若要儲存自訂檢視，請按一下箭頭圖示。

![檢視控制項範例](assets/workspace-controls-view.png)

在此範例中， _訂單ID_ 欄會新增至「欄」控制項中，並儲存為自訂檢視。 請注意，儲存自訂檢視名稱后，「檢視」的名稱會從 _預設檢視_ 至輸入的名稱。

您可以選取下列專案中的所需檢視，在檢視之間切換 _[!UICONTROL View]_功能表。

如果您想要刪除或變更自訂檢視的名稱，請按一下鉛筆圖示。 然後您可以輸入不同的名稱，或按一下垃圾桶圖示以刪除自訂檢視。 無法刪除預設檢視。

## 欄

「欄」控制項可讓您新增或移除頁面顯示中的資料欄。 每個Amazon銷售管道頁面都有資料欄的預設組合，但大多數頁面都有其他可用欄。 如果沒有可用的其他欄，您仍然可以從顯示中移除預設欄。

下列範例顯示欄控制項。 核取選項對應至頁面上顯示的欄標題。

- 若要新增資料欄至頁面，請選取核取方塊。
- 若要從頁面中移除資料欄，請勿選取核取方塊。

![欄控制項範例](assets/workspace-controls-columns.png)

核取方塊變更會立即顯示。 如果您進行變更並退出頁面，頁面會返回到預設欄顯示。 對於您定期進行的變更，您可以將欄變更儲存為「檢視」控制項中的自訂檢視。 然後，您就可以在「檢視」控制項中切換，而不必手動新增或移除欄。

您可以按一下 **[!UICONTROL Reset]** 以將選項設定回預設設定，或者您可以按一下 **[!UICONTROL Cancel]** 以結束，而不進行變更。

## 匯出

「匯出」選項可讓您將資料匯出至資料檔，而資料檔無法匯入至協力廠商軟體或個別資料庫。 匯出的資料僅限於顯示的資料。 如有需要，請先確認您新增或移除欄，再使用「匯出」控制項。

準備匯出資料時，請選擇匯出格式選項，然後按一下 **[!UICONTROL Export]**.

- CSV — 包含純文字資料的逗號分隔值檔案
- Excel XML — 以XML為基礎的試算表資料格式（通常用於Excel使用者）

產生的資料檔案會自動儲存到您指定的資料夾以供下載。

![匯出控制](assets/workspace-controls-export.png)
