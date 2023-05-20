---
title: 管理屬性
description: 您可以管理Commerce產品屬性與Amazon屬性的對應，以確保系統之間的產品資訊準確。
exl-id: 6f9ded2d-292e-4b7e-8c10-48f478a4383e
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---

# 管理屬性

Amazon和 [!DNL Commerce] 兩者都使用用於定義產品的產品屬性系統（稱為屬性）。 屬性可定義產品的說明、內容、影像、價格和各種資料。

Commerce與Amazon之間的成功通訊需要 [!DNL Commerce] 屬性必須正確對應（或比對）至對應的Amazon屬性。 與Amazon整合時，您可以將這些屬性對應至Amazon屬性。 完成時， [!DNL Commerce] 可以與同步並維護您的Amazon清單， [!DNL Commerce] 產品目錄。

例如，假設您的檔案中有相同專案， [!DNL Commerce] 目錄和Amazon清單。 產品的一個屬性可能是料號的清單價格。 中的掛牌價格名稱 [!DNL Commerce] 可命名為 `Price`，而Amazon的掛牌價格可能會命名為 `ListingPrice`. 您必須指示 [!DNL Commerce] 與Amazon通訊時， [!DNL Commerce] 已命名的屬性 `Price` 與命名的Amazon屬性相同 `ListingPrice`. 此程式稱為 _管理屬性_，並包括建立新屬性和編輯現有屬性。 確定屬性正確相符，確保彼此之間能夠正確通訊 [!DNL Commerce] 和Amazon。

設定屬性對應時， [!DNL Commerce] 可與Amazon來回溝通產品資訊。 如果您有Amazon產品清單， [!DNL Commerce] 可將您的Amazon產品和詳細資料匯入 [!DNL Commerce] 目錄，可讓您從單一集中式產品目錄管理您的Amazon清單。

Amazon sales channel可讓您視需要存取、檢閱、建立和管理屬性，於 [_[!UICONTROL Attributes]_檢視](./attributes-view.md) 在Amazon sales channel首頁。 如果您將屬性新增至 [!DNL Commerce] 型錄中，則可能需要更新所有產品的這些值。

如需有關的詳細資訊 [!DNL Commerce] 和Amazon屬性集及值，請參閱：

- [管理屬性基本知識](https://docs.magento.com/user-guide/catalog/product-attributes.html){target="_blank"}
- [建立屬性](./creating-attributes.md#create-an-attribute)
- [編輯現有屬性](./creating-attributes.md#edit-an-attribute)
- [檢視屬性對應](./amazon-matching-attributes-values.md)
- [編輯或建立屬性對應](./amazon-manually-update-incomplete-listing.md)
