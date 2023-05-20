---
title: 上線 [!DNL Channel Manager]
description: '將您的執行個體連線到 [!DNL Channel Manager] 完成幾個入門步驟即可完成服務。'
role: User
level: Intermediate
exl-id: 7c4ccd9e-ae32-4511-8d1e-baa690604612
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---


# 上線 [!DNL Channel Manager]

在您完成通路經理上線流程後，即可從Adobe Commerce存取、設定及管理Walmart Marketplace通路銷售作業。 管道管理員可從以下網址取得： [!UICONTROL Channel Manager] 上的選項 [!UICONTROL Commerce Admin Marketing] 功能表。

![[!DNL Channel Manager] 「管理員」檢視中的選項](assets/channel-manager-admin-view.png)

## 需求

檢閱使用Channel Manager的需求，並收集下載、安裝和設定擴充功能所需的帳戶資訊和認證。

- **[沃爾瑪市集需求](walmart-requirements.md)** — 確認您符合整合通路管理器的需求，包括 [設定您的賣家帳戶](https://sellerhelp.walmart.com/seller/s/guide?article=000008219) 以及產生API金鑰來啟用整合。

- **Commerce帳戶資訊** — 下載和安裝 [!DNL Channel Manager] 需要 [Commerce帳戶](https://docs.magento.com/user-guide/magento/magento-account.html){target="_blank"}. 您需要帳戶ID和憑證，以及擁有該帳戶擁有者或管理員許可權的 [!DNL Adobe Commerce] 或 [!DNL Magento Open Source] 執行個體。

   - **影像ID**-[登入](https://account.magento.com/customer/account/login/) 至 [!DNL Commerce] 要從中取得ID的帳戶 **[!UICONTROL My Account - Magento settings]**.

      ![[!DNL MAGEID] 於 [!DNL Commerce] 帳戶設定](assets/mageid-my-commerce-account.png)

   - **存取金鑰 —** 取得要下載的驗證金鑰 [!DNL Commerce] 擴充功能來自 [!DNL Commerce] Composer存放庫 `([!DNL repo.magento.com]`)。

      ![[!UICONTROL Commerce Marketplace access keys]](assets/commerce-marketplace-access-keys.png)

      在Adobe Commerce和Magento Open Source專案中，擁有者可以設定 [共用存取](https://docs.magento.com/user-guide/magento/magento-account-share.html) 可讓受信任的員工和服務提供者使用擁有者或授權擁有者帳戶的憑證下載擴充功能。

      對象 [!DNL Adobe Commerce] 在雲端基礎結構專案中，軟體安裝程式必須具備以下存取許可權： [!DNL Commerce] 例項：

      - 雲端專案的超級使用者存取權
      - 管理員存取特定環境
      - 一個 [!DNL Adobe Commerce] 具有存取Composer存放庫許可權的帳戶

      另請參閱 [管理使用者存取權](https://devdocs.magento.com/cloud/project/user-admin.html).


- **使用撰寫器和的體驗[!DNL Commerce CLI]** — 請參閱 [一般CLI安裝](https://devdocs.magento.com/extensions/install/){target="_blank"} 瞭解如何使用這些工具來安裝及管理擴充功能 [!DNL Adobe Commerce] 或 [!DNL Magento Open Source] 平台。

- **[[!DNL Amazon Sales Channel] 版本4.4.2或更新版本](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html)** — 若您已啟動 [!DNL Amazon Sales Channel] 您的 [!DNL Commerce] 網站，確認您的 [!DNL Commerce] 安裝之前，平台已安裝4.4.2版或更新版本 [!DNL Channel Manager].

- **[!DNL Inventory Management]Adobe Commerce和Magento Open Source的擴充功能**

   如果您計畫使用「通路管理員」進行存貨和訂單管理，則必須在Adobe Commerce和Magento Open Source執行個體上安裝並啟用Inventory management擴充功能。 一般而言，此擴充功能會依預設安裝在Adobe Commerce上並啟用， [!DNL Magento Open Source] 2.3.x和更新版本。

   如果您從2.2.x升級Commerce，或您已停用Inventory management，請更新您的安裝以包含必要的模組。 另請參閱 [安裝Inventory management](https://devdocs.magento.com/extensions/inventory-management/) (位於Adobe Commerce開發人員檔案中)。

### 系統需求

- [Adobe Commerce 2.4.x](https://devdocs.magento.com/release/released-versions.html)
- [PHP 7.3 / 7.4](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/php-settings.html)
- [Composer 1.x或更新版本](https://devdocs.magento.com/cloud/reference/cloud-composer.html)
- [[!DNL Amazon Sales Channel] 版本4.4.2或更新版本](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html) — 如果您已啟用 [!DNL Amazon Sales Channel] 您的 [!DNL Commerce] 網站，確認您的 [!DNL Commerce] 平台在安裝前已安裝4.4.2版 [!DNL Channel Manager].
- [[!DNL Inventory Management]](https://devdocs.magento.com/extensions/inventory-management/)

### 支援的平台

- 雲端上的Adobe Commerce (ECE) ：2.4.x
- Adobe Commerce內部部署(EE) ：2.4.x
- Magento Open Source2.4.x

## 入門步驟

1. [設定您的Walmart賣家帳戶](https://seller.walmart.com/signup?q=&amp;origin=solution_provider&amp;src=0014M00001zivMp).

1. [安裝 [!DNL Channel Manager] 擴充功能](install.md).

1. [連線至Commerce Services](connect.md) 將管道管理員與商務執行個體和其他支援服務整合。

1. [連線您的 [!DNL Commerce] 儲存至 [!DNL Walmart Marketplace]](connect-marketplace.md).

1. [完成商店設定](complete-sales-channel-store-setup.md).
