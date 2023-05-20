---
title: 訂單設定
description: 使用訂單設定來決定如何將Amazon訂單匯入您的Commerce商店並進行處理。
redirect_from: /sales-channels/asc/ob-order-settings.html
exl-id: dc8d0ce1-86a8-4949-b49a-73c5cf62db16
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '1377'
ht-degree: 0%

---

# 訂單設定

訂單設定會定義是否及如何將Amazon訂單匯入及處理 [!DNL Commerce] 並可從 [存放區儀表板](./amazon-store-dashboard.md).

訂單匯入設定設為 `Enabled` 根據預設，這表示您的Amazon訂單會出現在商店控制面板上，並建立對應的 [!DNL Commerce] 訂購。 匯入的訂單可在以下位置管理： [!DNL Commerce] [訂購](https://docs.magento.com/user-guide/sales/orders.html){target="_blank"} 工作流程。

>[!NOTE]
>
>無論您的訂單設定為何，系統都不會匯入您商店整合前已有的Amazon訂單。

晚於 [存放區整合](./store-integration.md) 完成，您可以變更訂單設定。 如果您將訂單設定設為 `Disabled`，Amazon訂單會顯示在商店儀表板上，但必須在以下位置管理： [!DNL Amazon Seller Central] 帳戶。

在Amazon上建立訂單時，不會立即匯入 [!DNL Commerce]. Amazon指派 `Pending` 新建立訂單的狀態。 Amazon驗證訂單和付款方式後，訂單的狀態會變更為 `Unshipped`. 此狀態變更會觸發訂單匯入，並且 [!DNL Commerce] 建立相符的對應順序。

從Amazon匯入的訂單可在以下位置管理： [!DNL Commerce] [訂單工作流程](https://docs.magento.com/user-guide/sales/orders.html){target="_blank"}. 另請參閱 [管理訂單](./managing-orders.md).

## 設定訂單設定 {#configure-order-settings}

1. 按一下 **[!UICONTROL Order Settings]** 在商店控制面板上。

1. 對象 **[!UICONTROL Import Amazon Orders]** （必要），選擇一個選項：

   - `Disabled`  — 選擇您不想在中建立對應訂單的時間 [!DNL Commerce] 從Amazon收到新訂單時。 選擇後，會停用此頁面上的所有其他欄位。

   - `Enabled` - （預設）選擇何時建立對應的 [!DNL Commerce] 從Amazon收到新訂單時的訂單。 [!DNL Commerce] 訂單是根據Amazon狀態和存貨層次建立的。

      >[!NOTE]
      >
      >匯入Amazon訂單必須設定為 `Enabled` 若要在中管理Amazon訂單 [!DNL Commerce] [訂購](https://docs.magento.com/user-guide/sales/orders.html){target="_blank"} 工作流程。 當設定為 `Disabled`，您的Amazon訂單中沒有對應的 [!DNL Commerce] 訂單編號，且無法在中管理 [!DNL Commerce]. 您可以管理下列訂單： [!DNL Amazon Seller Central] 帳戶。

1. 對象 **[!UICONTROL Import Amazon Orders Into Magento Store]**，選擇哪一個 [!DNL Commerce] 儲存於中建立對應訂單時，相關聯的Amazon訂單 [!DNL Commerce].

   此設定預設為您在選取的網站時，使用「商店檢視」 [已新增Amazon存放區](./store-integration.md). 若要變更此設定，選項清單取決於 [!DNL Commerce] 您在設定中設定的存放區。 另請參閱 [商店](https://docs.magento.com/user-guide/stores/stores-all-create-view.html#create-a-new-store-view){target="_blank"}.

1. 對象 **[!UICONTROL Customer Creation]**，選擇一個選項：

   - `No Customer Creation (guest)` - （預設）選擇您不想在中建立客戶帳戶的時間 [!DNL Commerce] 使用從Amazon訂單匯入的客戶資料。 選擇後， [!DNL Commerce] 會以處理訪客結帳的方式處理匯入的Amazon訂單 [!DNL Commerce].

   - `Build New Customer Account`  — 選擇您要在中建立新客戶帳戶的時間 [!DNL Commerce] 使用隨Amazon訂單匯入的客戶資料。 此選項可協助您根據Amazon訂單建立客戶資料庫。

1. 對象 **[!UICONTROL Order Number Source]**，選擇一個選項：

   - `Build Using Magento Order Number` - （預設）選擇何時建立唯一 [!DNL Commerce] 使用的對應Amazon訂單的訂單編號 [!DNL Commerce] 增量指派的訂單ID。

   - `Build Using Amazon Order Number`  — 選擇您想要建立 [!DNL Commerce] 訂單編號，使用對應的Amazon指派的訂單編號。
   >[!NOTE]
   >
   >匯入訂單後，Amazon訂單編號會顯示在 _[!UICONTROL Recent Orders]_在商店控制面板上的清單。 此 [!DNL Commerce] 訂單編號會在檢視訂單詳細資料時顯示 [!DNL Commerce] [訂購](https://docs.magento.com/user-guide/sales/orders.html){target="_blank"} 工作區。

1. 對象 **[!UICONTROL Order Status]** （必要），選擇一個選項：

   - `Default Order Status` - （預設）選擇何時要將從Amazon匯入的新建立訂單指派給您為新訂單定義的預設訂單狀態。 新訂單的預設狀態（除非您已為新訂單建立自訂訂單狀態）為 `Pending`. 另請參閱 [處理訂單](https://docs.magento.com/user-guide/sales/order-processing.html){target="_blank"}.

   - `Custom Order Status`  — 選擇何時要將從Amazon匯入的新建立訂單指派給預設以外的狀態。

   - `Processing Order Status`  — 啟用時機 **[!UICONTROL Order Status]** 設為 `Custom Order Status`. 選擇您要用於從Amazon匯入之新建立訂單的狀態。 此欄位中的選項是根據中的預設狀態選項 [!DNL Commerce]. 另請參閱 [訂單狀態](https://docs.magento.com/user-guide/sales/order-status.html). 您也可以建立自訂訂單狀態，顯示於此處以供選取。 若要建立自訂訂單狀態，請參閱 [自訂訂單狀態](https://docs.magento.com/user-guide/sales/order-status-custom.html){target="_blank"}.

1. 完成後，按一下 **[!UICONTROL Save order settings]**.

![訂單設定](assets/amazon-order-settings.png)

| 欄位 | 說明 |
|---|---|
| [!UICONTROL Import Amazon Orders] | 選項：<ul><li>**[!UICONTROL Disabled]**  — 選擇您不想在中建立對應訂單的時間 [!DNL Commerce] 從Amazon收到新訂單時。 選擇後，會停用此頁面上的所有其他欄位。</li><li>**[!UICONTROL Enabled]** - （預設）選擇何時建立對應的 [!DNL Commerce] 從Amazon收到新訂單時的訂單。 [!DNL Commerce] 訂單是根據Amazon狀態和存貨層次建立的。</li></ul><br><br>`Enabled` 必須選取此項才能管理Amazon訂單 [!DNL Commerce]. 時間 `Disabled` ，您的Amazon訂單會顯示在商店儀表板上，但訂單必須在以下位置進行管理： [!DNL Amazon Seller Central] 帳戶。 |
| [!UICONTROL Import Amazon Orders Into Magento Store] | 選擇哪一個 [!DNL Commerce] 儲存在中建立訂單時，相關聯的Amazon訂單 [!DNL Commerce] [訂購](https://docs.magento.com/user-guide/sales/orders.html){target="_blank"} workspace. This setting defaults to the Store View for the [!DNL Commerce] website selected when you [added the Amazon store](./store-integration.md). If you want to change this setting, the list of options depends on the [!DNL Commerce] stores you have set up in your configuration. See [Stores](https://docs.magento.com/user-guide/stores/stores-all-stores.html){target="_blank"}. |
| [!UICONTROL Customer Creation] | 選項：<ul><li>**[!UICONTROL No Customer Creation (guest)]** - （預設）選擇您不想在中建立客戶帳戶的時間 [!DNL Commerce] 使用從Amazon訂單匯入的客戶資料。 選擇此選項時，此選項會告知 [!DNL Commerce] 以處理匯入的Amazon訂單，就像處理訪客結帳一樣。</li><li>**[!UICONTROL Build New Customer Account]**  — 選擇您要在何時在中建立新的客戶帳戶 [!DNL Commerce] 客戶資料庫，使用隨Amazon訂單匯入的客戶資料。 此選項有助於建立 [!DNL Commerce] 來自您Amazon訂單的客戶資料庫。</li></ul> |
| 訂單編號來源 | 選項：<ul><li>**[!UICONTROL Build Using Magento Order Number]** - （預設）選擇何時建立唯一 [!DNL Commerce] 使用的對應Amazon訂單的訂單編號 [!DNL Commerce] 增量指派的訂單ID。 </li><li>**使用Amazon訂單編號建立**  — 選擇您想要建立 [!DNL Commerce] 訂單編號，使用對應的Amazon指派的訂單編號。</li></ul> |
| 擱置中的訂單 | 選項：<ul><li>**[!UICONTROL Do Not Reserve Quantity]**  — 選擇何時不想要您的 [!DNL Commerce] 受您的Amazon訂單影響的庫存數量。 選擇您是否將Amazon用於履行流程(FBA)。 當您選擇並收到Amazon訂單時，訂購數量不會影響 [!DNL Commerce] 庫存量。</li><li>**[!UICONTROL Reserve Quantity]**  — 選擇您希望Amazon訂單中的訂單數量在您的 [!DNL Commerce] 庫存量。 當您選擇並收到Amazon訂單時，訂購數量將「預留」在 [!DNL Commerce] 庫存數量，以防止您的 [!DNL Commerce] 庫存來自「超量銷售」。 「預留」數量無法透過您的購買。 [!DNL Commerce] 店面。</li></ul> |
| [!UICONTROL Order Status] | 選項：<ul><li>**[!UICONTROL Default Order Status]** - （預設）選擇何時要將從Amazon匯入的新建立訂單指派給新訂單的預設訂單狀態。 新訂單的預設狀態（除非您已為新訂單建立自訂訂單狀態）為 `Pending`. 另請參閱 [處理訂單](https://docs.magento.com/user-guide/sales/order-processing.html).</li><li>>**[!UICONTROL Custom Order Status]**  — 選擇何時要將從Amazon匯入的新建立訂單指派給預設以外的狀態。 選擇後， **[!UICONTROL Processing Order Status]** 可讓您選擇要用於從Amazon匯入之新建立訂單的狀態。</li></ul> |
| [!UICONTROL Processing Orders Status] | 啟用時機 _[!UICONTROL Order Status]_設為 `Custom Order Status`. 選擇您要指定給新訂單的訂單狀態。 此欄位中的選項取決於中的預設狀態選項 [!DNL Commerce]. 另請參閱 [訂單狀態](https://docs.magento.com/user-guide/sales/order-status.html){target="_blank"}. You can also create a custom order status to show here. To create a custom order status, see [Custom Order Status](https://docs.magento.com/user-guide/sales/order-status-custom.html){target="_blank"}. |

## [!DNL Commerce] 訂單建立

[!DNL Commerce] 系統會根據下列狀態與存貨條件，為Amazon訂單建立訂單。

### 使用Inventory management建立訂單

>[!NOTE]
>
>僅於Adobe Commerce和Magento Open Source 2.3.x整合中支援。

| 履行管道 | [!DNL Commerce] 詳細目錄狀態 | Amazon訂單狀態 | [!UICONTROL Create Magento Order] 設定 | 庫存預留 |
|---|---|---|---|---|
| FBA | 有貨<br>無庫存<br>不管理 | 擱置中 | 否 | 否 |
| FBA | 有貨<br>無庫存<br>不管理 | PendingAvailable | 否 | 否 |
| FBA | 有貨<br>無庫存<br>不管理 | 已取消 | 否 | 否 |
| FBA | 有貨<br>無庫存<br>不管理 | 錯誤 | 否 | 否 |
| FBA | 有貨<br>無庫存<br>不管理 | 未送出 | 否 | 否 |
| FBA | 有貨<br>無庫存<br>不管理 | 已部分出貨 | 否 | 否 |
| FBA | 有貨<br>不管理 | 已送出 | 是 | 否 |
| FBA | 無庫存 | 已送出 | 否 | 否 |
| FBM | 有貨<br>無庫存<br>不管理 | 擱置中 | 否 | 否 |
| FBM | 有貨<br>無庫存<br>不管理 | PendingAvailable | 否 | 否 |
| FBM | 有貨<br>無庫存<br>不管理 | 已取消 | 否 | 否 |
| FBM | 有貨<br>無庫存<br>不管理 | 錯誤 | 否 | 否 |
| FBM | 有貨<br>不管理 | 未送出 | 是 | 是 |
| FBM | 無庫存 | 未送出 | 否 | 否 |
| FBM | 有貨<br>不管理 | 已部分出貨 | 是 | 是 |
| FBM | 無庫存 | 已部分出貨 | 否 | 否 |
| FBM | 有貨<br>不管理 | 已送出 | 是 | 是 |
| FBM | 無庫存 | 已送出 | 否 | 否 |

>[!NOTE]
>若在中匯入Amazon訂單 `Partially Shipped` 或 `Shipped` 狀態，所建立的存貨預留適用於訂單中的所有料號。 Amazon sales channel不會補償先前已出貨的專案。
>
>如果訂單已由Amazon (FBA)履行，但料號位於 `out of stock` 狀態， [!DNL Commerce] 無法建立對應的訂單。 這是Inventory management整合的限制。
