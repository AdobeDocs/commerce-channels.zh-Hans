---
title: 處理訂單
description: '''送貨與取消說明 [!DNL Walmart Marketplace] Adobe Commerce和Magento Open Source的訂單。'
exl-id: 2fdcb348-5c02-464f-a114-16ec657bed6b
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 0%

---

# 處理訂單

晚於 [!DNL Walmart Marketplace] 訂單已確認並成功傳送至 [!DNL Channel Manager]，您會使用 [Commerce訂單管理](https://docs.magento.com/user-guide/sales/orders-workspace.html) 以處理訂單。

頻道管理員將更新同步到 [!DNL Walmart Marketplace] 以確保訂單狀態與出貨資訊來自 [!DNL Commerce] 符合中追蹤的資料 [!DNL Walmart Marketplace].

* **訂單出貨** — 沃爾瑪要求所有出貨都要有追蹤編號。 如果部份料號無庫存，您可以建立部份出貨，以傳送目前可用的料號。 在您提交出貨之後，訂單更新會同步至 [!DNL Walmart Marketplace]. 然後，沃爾瑪會通知客戶訂單狀態和送貨細節。

* **訂單取消** — 當您取消 [!DNL Walmart Marketplace] 訂單，Walmart要求取消原因，包含在寄給客戶的訂單取消通知中。 取消原因也會顯示在 [!DNL Commerce] 訂單付款資訊。 在您提交取消之後，庫存更新會同步到 [!DNL Walmart Marketplace]. 然後，沃爾瑪會通知客戶訂單狀態和送貨細節。

   在店面，您必須取消整個訂單。 [!DNL Commerce] 不允許部分取消。

* **退款請求** — 如果要求沃爾瑪市集退回已出貨的訂單，則 [!UICONTROL Status details] 包含回訪連結。 退款及退款由 [傳回](return-refund-orders.md) 儀表板。

處理商務訂單時，並 [!DNL Channel Manager] 成功將出貨、部份出貨及取消更新同步至 [!DNL Walmart Marketplace]，訂單處理完成。 已出貨訂單的退貨請求與退款管理會從 [傳回](return-refund-orders.md) 儀表板。

>[!NOTE]
>
> 訂單更新最多可能需要5分鐘的時間才能同步至 [!DNL Walmart Marketplace]. 若要檢查訂單狀態，請返回 [!DNL Channel Manager] 訂單頁面。

## 出貨訂單

1. 從「管理員」中選取「 」 **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. 選取銷售管道商店的眼睛圖示，以開啟商店檢視。

1. 檢視 [!DNL Walmart Marketplace] 訂購，選取 **[!UICONTROL Orders]**.

1. 在「訂單」表格中，選取下列專案以開啟要出貨的訂單： **商務訂單編號**.

1. 選取下列專案，為全部或部份訂單建立及提交出貨 **[!UICONTROL Ship]**.

   ![的商務訂單詳細資料檢視 [!DNL Walmart Marketplace] 訂購](assets/order-detail-with-external-order-id.png)

   * 選擇出貨承運商，並透過選取 **[!UICONTROL Add tracking number]**.

      ![的商務訂單詳細資料檢視 [!DNL Walmart Marketplace] 訂購](assets/order-shipment-add-tracking-number.png)


   * 視需要完成其餘的送貨表格。 另請參閱 [[!DNL Shipping an Order]](https://docs.magento.com/user-guide/sales/order-ship.html) 以取得詳細指示。

1. 提交出貨後，追蹤 [訂單狀態](manage-orders.md#about-order-status) 在 [!DNL Channel Manager] 驗證更新是否已傳送至 [!DNL Walmart Marketplace].

在訂單出貨後，您可以處理全部或部份退款 [!DNL Channel Manager] 適用於訂單中包含的料號，根據從收到的退貨請求 [!DNL Walmart Marketplace]. 另請參閱 [退貨與退款訂單](return-refund-orders.md).

## 取消訂單

1. 從「管理員」中選取「 」 **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. 選取銷售管道商店的眼睛圖示，以開啟商店檢視。

1. 檢視 [!DNL Walmart Marketplace] 訂購，選取*[!UICONTROL *Orders]**。

1. 在「訂單」表格中，開啟 [訂單詳細資訊頁面](manage-orders.md#view-order-detail) 藉由選取 **商務訂單編號** 以取消訂單。

   ![的商務訂單詳細資料檢視[!DNL Walmart Marketplace]訂購](assets/order-detail-with-external-order-id.png)

1. 取消訂單。

   * 選取 **取消** 從「訂單明細」功能表。

   * 於 [!UICONTROL Cancel Order] 表單中，選取 **取消原因**.
   ![的商務訂單詳細資料檢視 [!DNL Walmart Marketplace] 訂購](assets/cancel-order-reason-selector.png)

   * 選取 **取消訂單**.


1. 提交取消後，追蹤 [訂單狀態](manage-orders.md#about-order-status) 在 [!DNL Channel Manager] 驗證更新是否已傳送至 [!DNL Walmart Marketplace].

## 修正訂單錯誤

在訂單同步處理過程中，可能會發生下列錯誤： [!DNL Walmart Marketplace]，或在出貨、部份出貨及取消的訂單更新處理期間。

如果出貨、部份出貨或取消更新的同步化作業失敗，則 [!DNL Channel Manager] 訂單頁面會顯示 _錯誤_ 訂單的狀態。 為確保出貨資訊與訂單取消資訊準確反映在Walmart Marketplace帳戶中，請手動更新 [!DNL Walmart Marketplace] 商店。


