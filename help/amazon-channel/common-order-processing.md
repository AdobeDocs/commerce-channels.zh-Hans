---
title: 常見訂單處理作業
description: 使用對應的 [!DNL Commerce] 已為Amazon訂單建立訂單，以管理訂單活動與處理 [!UICONTROL Commerce] 管理員。
exl-id: a44f36f0-db18-4de5-9c5b-cc68f4793008
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# 常見訂單處理作業

[[!DNL Commerce] 訂單處理](https://docs.magento.com/user-guide/sales/order-processing.html){target="_blank"} 可以管理您的Amazon訂單，包括傳送電子郵件給採購員、履行訂單（出貨）、簽發銷退折讓/退款、新增註解等。 若要管理您的Amazon訂單，請 [**匯入Amazon訂單**](./order-settings.md) 設定必須設定為 `Enabled` 因此，相應 [!DNL Commerce] 訂單會在收到Amazon訂單時建立。 Amazon訂單資訊顯示在 *[!UICONTROL Recent Orders]* 區段。

啟用時，對應於 [!DNL Commerce] 系統會為Amazon訂單建立訂單，而Amazon訂單編號會顯示在 _[!UICONTROL Order Number]_欄。 若相應 [!DNL Commerce] 建立訂單後，按一下訂單編號以開啟 [!DNL Commerce] [訂單處理](https://docs.magento.com/user-guide/sales/order-processing.html){target="_blank"} page. You can manage the order as you do your other [[!DNL Commerce] order processing](https://docs.magento.com/user-guide/sales/order-processing.html){target="_blank"}.

此 [!DNL Commerce] 訂單編號不會與一起顯示 _[!UICONTROL Recent Orders]_資訊。 此 [!DNL Commerce] 只有當您按一下商店控制面板上的訂單編號，並在以下位置開啟訂單時，才會顯示訂單編號： [[!DNL Commerce] 訂單處理](https://docs.magento.com/user-guide/sales/order-processing.html){target="_blank"}. 檢視 [!DNL Commerce] 訂購，Amazon訂購編號會出現在&#x200B;*[!UICONTROL Payment & Shipping Method]*區段。 其中也包含&#x200B;*[!UICONTROL View or Cancel Amazon Order]*和&#x200B;*[!UICONTROL View all Amazon Orders]*，視訂單送貨狀態而定。

另請參閱 [取消未出貨的訂單](./cancel-unshipped-order.md).

![商務訂單中的Amazon訂單資訊](assets/amazon-order-number-payment-info.png)

處理Amazon訂單時，Amazon銷售管道會更新訂單資訊，並將其與您的 [!DNL Amazon Seller Central] 帳戶。 您的cron設定會決定訂單資訊在Amazon和Amazon銷售管道之間同步的頻率。

通用 [!DNL Commerce] [訂單處理](https://docs.magento.com/user-guide/sales/order-processing.html){target="_blank"} 工作包括：

- [訂購動作](https://docs.magento.com/user-guide/sales/order-actions.html){target="_blank"}
- [訂單搜尋](https://docs.magento.com/user-guide/sales/orders-search.html){target="_blank"}
- [處理訂單](https://docs.magento.com/user-guide/sales/order-processing.html){target="_blank"}
   - [檢視訂單](https://docs.magento.com/user-guide/sales/order-processing.html#view-an-order){target="_blank"}
   - [處理訂單](https://docs.magento.com/user-guide/sales/order-processing.html#process-an-order){target="_blank"}
   - [訂單與帳戶資訊](https://docs.magento.com/user-guide/sales/order-processing.html#order-and-account-information){target="_blank"}
   - [地址資訊](https://docs.magento.com/user-guide/sales/order-processing.html#address-information){target="_blank"}
   - [付款與送貨方式](https://docs.magento.com/user-guide/sales/order-processing.html#payment--shipping-method){target="_blank"}
   - [檢閱訂購的專案](https://docs.magento.com/user-guide/sales/order-processing.html#review-items-ordered){target="_blank"}
- [核發銷退折讓/退款](https://docs.magento.com/user-guide/sales/credit-memo-create.html){target="_blank"}
- [履行/送貨訂單](https://docs.magento.com/user-guide/sales/shipments-create.html){target="_blank"}
- [建立發票](https://docs.magento.com/user-guide/sales/invoice-create.html){target="_blank"}
- [取消未出貨的訂單](./cancel-unshipped-order.md)

>[!NOTE]
>
>如果訂單位於 `Unshipped` 狀態，您可以 [取消Amazon訂單](./cancel-unshipped-order.md) 於 [[!UICONTROL Amazon Order Details]](./amazon-order-details.md) 頁面。 如果訂單已出貨，則無法取消。

另請參閱 [Commerce訂單管理](https://docs.magento.com/user-guide/sales/order-management.html){target="_blank"}.
