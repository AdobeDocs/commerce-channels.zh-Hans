---
title: 管理訂單
description: 您可以在「訂單設定」中啟用訂單匯入，以便更輕鬆地透過商務管理員管理您的Amazon訂單。
exl-id: 018a8936-2f03-4a2d-b9af-6b72729ca709
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---

# 管理訂單

Amazon從Amazon收到的訂單資訊，您可以在 _[!UICONTROL Recent Orders]_部分 [存放區儀表板](./amazon-store-dashboard.md) 或在_[!UICONTROL Amazon orders]_ 頁面(也稱為 _[!UICONTROL All Orders]_檢視)。

您如何管理Amazon訂單取決於您的訂單匯入是啟用還是停用 [訂單設定](./order-settings.md#configure-order-settings).

## 啟用訂單匯入時

晚於 [存放區整合](./store-integration.md)，則 [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) 設定為 `Enabled` 依預設。 透過此設定，對應於 [!DNL Commerce] 系統會為您的Amazon訂單建立訂單，並可在以下位置管理： [[!DNL Commerce] 訂購](https://docs.magento.com/user-guide/sales/orders.html){target="_blank"} 工作流程。

>[!NOTE]
>
>無論您的訂單匯入設定為何，您現有的Amazon訂單 [!DNL Amazon Seller Central] 之前的帳戶 [存放區整合](./store-integration.md) 不會匯入。

匯入的Amazon訂單會在以下位置管理： [[!DNL Commerce] 訂購](https://docs.magento.com/user-guide/sales/orders.html){target="_blank"} workflow, just like your other [!DNL Commerce] stores. Click the Amazon order number in the *[!UICONTROL Order Number]* column to open the order in the [[!DNL Commerce] order process](https://docs.magento.com/user-guide/sales/order-processing.html#order-view-descriptions){target="_blank"}. 另請參閱 [檢視Amazon訂單](./amazon-orders-all.md).

### 訂單匯入程式

在Amazon上下達訂單時， [訂單匯入](./order-settings.md) 已啟用，則會開始下列程式。

| 變更 | 動作 |
|---|---|
| 訂單已下達Amazon。 | <ul><li>Amazon將訂單狀態設為 `Pending`.</li><li>訂單資訊已傳送至 [!DNL Commerce].</li><li>訂單已新增至 [_Amazon訂單_ 表格](./amazon-orders-all.md) 搭配 `Pending` 狀態。</li></ul> |
| Amazon會將訂單狀態變更為 `Unshipped`. | <ul><li>狀態變更已傳送至 [!DNL Commerce].</li><li>在 [_Amazon訂單_ 表格](./amazon-orders-all.md)，訂單狀態會變更為 `Unshipped`.</li><li>在 [[!DNL Commerce] 訂單工作流程](https://docs.magento.com/user-guide/sales/orders.html){target="_blank"}，對應 [!DNL Commerce] 訂單是使用 `Processing` 狀態。</li></ul> |
| 在 [[!DNL Commerce] 訂單工作流程](https://docs.magento.com/user-guide/sales/orders.html){target="_blank"}，則 [!DNL Commerce] 訂單已處理且狀態變更為 `Shipped`. | <ul><li>在 [_Amazon訂單_ 表格](./amazon-orders-all.md)，訂單狀態會變更為 `Shipped`.</li><li>在下一個cron作業中，訂單狀態會變更為 `Complete` 在 [[!DNL Commerce] 訂單工作流程](https://docs.magento.com/user-guide/sales/orders.html){target="_blank"}.</li></ul> |

### 訂單建立封鎖程式

有一些案例會阻止建立對應的 [!DNL Commerce] 訂購。 [!DNL Commerce] 當發生下列任何問題時，不會為收到的訂單建立訂單。

| 情境 | 解決方案 |
|---|---|
| 此專案不存在於 [!DNL Commerce] 目錄。 | [建立產品](./creating-assigning-catalog-products.md) 在您的 [!DNL Commerce] 目錄和 [手動比對](./creating-assigning-catalog-products.md) 它對應至產品。 |
| 目錄中的專案已停用。 | 請確定 [產品狀態](https://docs.magento.com/user-guide/catalog/inventory-product-stock-options.html){target="_blank"} 已啟用。 |
| 訂購料號無庫存。 | 更新或設定 [產品選項](https://docs.magento.com/user-guide/catalog/inventory-product-stock-options.html){target="_blank"} 數量與來源。 |

當無法匯入訂單時，熒幕上方會顯示類似下列的系統訊息：

`Your Amazon store(s) has orders that cannot be imported into [!DNL Commerce]. See Recent Orders in the store dashboard(s): <store name>`

問題解決後， [!DNL Commerce] 訂單會在下次同步時建立。

## 已停用訂單匯入

如果您不想要在中匯入及管理您的Amazon訂單 [!DNL Commerce]，您可以變更 [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) 設定為 `Disabled`. 此設定表示從Amazon收到新訂單時，會 [!DNL Commerce] 未建立訂單。

停用後，從Amazon收到的訂單資訊會出現在 _[!UICONTROL Recent Orders]_區段和_[!UICONTROL All Orders]_ 檢視。 此訂單資訊僅供檢視，您必須管理下列訂單： [!DNL Amazon Seller Central]. 若要在中開啟訂單詳細資料，請執行下列步驟： [!DNL Amazon Seller Central]，按一下中的Amazon訂單編號 _[!UICONTROL Order Number]_欄。

另請參閱 [檢視Amazon訂單](./amazon-orders-all.md)， [檢視Amazon訂單詳細資料](./amazon-order-details.md)、和 [常見訂單處理作業](./common-order-processing.md).
