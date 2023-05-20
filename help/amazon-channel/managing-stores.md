---
title: Amazon商店檢視
description: 前往Amazon商店檢視，快速檢閱每個Amazon商店的基本統計資料，以及存取管理選項。
exl-id: 1376cd84-da81-4d3b-a5be-218aa802eed6
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---

# Amazon商店檢視

檢視Amazon銷售管道首頁時， _Amazon商店_ 依預設，檢視會開啟。

![Amazon商店檢視](assets/amazon-sales-channel-home-tabs.png)

此 _[!UICONTROL Amazon Stores]_檢視會顯示每個Amazon商店的「商店卡」，以及一些基本統計和管理選項。 每張卡片中所顯示的摘要資訊包含各商店狀態、建立日期、上次更新日期、需要注意的清單（例如：未完成的清單）以及指定的清單 [!DNL Commerce] 網站。

檢視 _[!UICONTROL Amazon Store]_檢視，每個商店卡可讓您：

- 若要開啟商店，請執行下列步驟： [儀表板](./amazon-store-dashboard.md)，按一下 **[!UICONTROL View Store]**.

- 若要變更商店狀態或刪除商店，請按一下 **[!UICONTROL Action]** 並選擇：

   - **[!UICONTROL Activate]** / **[!UICONTROL Deactivate]**  — 選擇將存放區的狀態變更為 `Active` 或 `Inactive`（分別）。

      變更 `Inactive` 儲存至 `Active` status會使用商店目前的商店設定（例如清單設定、價格規則和覆寫）來啟用商店的清單和訂單活動。

      變更存放區狀態，從 `Active` 至 `Inactive` status會暫停商店的清單和訂單活動。 非使用中存放區會保留所有存放區設定與清單，但會暫時停止訂價、數量及訂單管理的同步化，直到存放區變更回為止 `Active` 狀態。 此功能可讓您在地區層級控制商店活動，而不需要重新建立或重新整合您的Amazon商店，或遺失歷史訂單和銷售資料。

   - **[!UICONTROL Delete]**  — 選擇刪除不再需要的存放區。

      選擇您何時想要刪除現有的Amazon商店及其與的整合設定 [!DNL Amazon Seller Central] 帳戶。 刪除帳戶會從Amazon銷售管道中移除該商店，以及所有帳戶設定、清單、記錄和其他與此商店相關的資訊。 刪除後無法擷取存放區，必須建立新存放區。

>[!NOTE]
>若要在整合期間變更指派給商店的網站，您必須刪除商店，然後使用商店整合期間定義的不同網站再次新增商店。

| 商店卡 | 說明 |
|--- |--- |
| 頂端區段 | 包括： <br>存放區的區域圖示，定義於 [存放區整合](./store-integration.md).<br> 已指派 _[!UICONTROL Magento Website]_，會在存放區整合期間定義。<br>此_[!UICONTROL Status]_ ，屬於您的商店。 選項： **[!UICONTROL Active]**  — 商店整合已透過Amazon完成及驗證，並可用於銷售活動。 **[!UICONTROL Inactive]**  — 商店整合已完成，但並未使用或可供銷售活動使用。 時間 `Inactive`，您的Amazon銷售已暫停。 時間 `Active`，銷售收入和其他設定會在啟用前儲存以更新。<br>此 *[!UICONTROL Last Updated]* 最近變更Amazon商店設定的日期。<br>此 *[!UICONTROL Created]* 在Amazon銷售管道中建立Amazon商店的日期。 |
| 中間截面 | 包含過去30天的商店活動摘要圖表，並包含任何需要注意的清單和警報。 |
| 底部區段 | 包含「檢視存放區」和「動作」選項。<br>若要開啟商店，請執行下列動作： [儀表板](./amazon-store-dashboard.md)，按一下 **[!UICONTROL View Store]**.<br>若要啟用、停用或刪除商店，請按一下 **[!UICONTROL Actions]**. |
