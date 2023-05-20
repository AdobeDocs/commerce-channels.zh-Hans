---
title: 手動發佈Amazon清單
description: 如有需要，您可以從Commerce管理員手動發佈已結束的Amazon清單。
exl-id: ca3f674e-d93a-44a6-8c06-b417694a0f1e
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---

# 手動發佈Amazon清單

您可以手動發佈一或多個已結束的Amazon清單。

1. 檢視一或多個清單 _[!UICONTROL Ended]_標籤上的 [產品清單](./managing-product-listings.md) 頁面(_[!UICONTROL Inactive]_， _[!UICONTROL Active]_，或_[!UICONTROL Ineligible]_ 標籤)。

1. 在左側欄中，按一下以核取您要重新發佈的每個清單。

1. 下 _[!UICONTROL Actions]_，按一下&#x200B;**[!UICONTROL Publish Product to Amazon]**.

1. 按一下 **[!UICONTROL OK]** 在確認訊息中。

   系統會顯示訊息，確認系統正在處理選取的清單，以便發佈至Amazon。

   清單資訊會根據您的cron設定發佈至Amazon。 清單資訊會在下次資料同步時傳送到Amazon。 在Amazon回覆清單確認之前，手動發佈的清單會保留在 _準備列出_ 以Tab鍵定位 `List in Progress` 狀態。 從Amazon收到清單確認時，清單會移至 _作用中_ 以tab鍵定位 `Active` 狀態。
