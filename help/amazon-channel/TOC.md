---
user-guide-title: AmazonSales Channel使用手冊
user-guide-description: 將Adobe Commerce或Magento Open Source與您的整合，透過Amazon產生銷售 [!DNL Amazon Seller Central] 帳戶。
breadcrumb-title: Amazon sales channel
source-git-commit: 193f7bfc0c2373f9a79f9cdb7d01877971f31083
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 0%

---


# Amazon sales channel - [!DNL channel manager] 適用於Adobe Commerce {#amazon}

- [指南概述](guide-overview.md)
- [Amazon銷售管道簡介](overview.md)
- [發行說明](release-notes.md)
- 快速入門 {#getting-started}
   - [關於Amazon sales channel](about-amazon-sales-channel.md)
   - [關於Amazon Marketplace](about-amazon-marketplace.md)
   - [關於Amazon和您的Commerce目錄](about-listings-and-catalog.md)
   - [最佳作法和限制](amazon-best-practices.md)
   - [安裝擴充功能](install.md)
- 入門 {#onboarding}
   - [上線Amazon銷售管道](amazon-onboarding-home.md)
   - [預先設定任務](amazon-pre-setup-tasks.md)
   - [建立 [!DNL Commerce] Amazon的屬性](ob-creating-magento-attributes.md)
   - [驗證Amazon API金鑰](amazon-verify-api-key.md)
   - [存放區整合](store-integration.md)
   - [建立清單規則](ob-create-listing-rule.md)
   - [預設商店設定](default-store-settings.md)
- 管理銷售管道 {#manage}
   - [首頁](amazon-sales-channel-home.md)
   - [Amazon商店](managing-stores.md)
   - [工作區控制項](workspace-controls.md)
   - [學習與準備](learning-preparation.md)
   - 屬性 {#attributes}
      - [檢視屬性](attributes-view.md)
      - [管理屬性](managing-attributes.md)
      - [建立和編輯屬性](creating-attributes.md)
      - [檢視屬性對應](amazon-matching-attributes-values.md)
   - [Sales Channel管理設定](sales-channel-settings.md)
   - [Amazon商店控制面板](amazon-store-dashboard.md)
   - [商店設定](ob-store-review.md)
- 清單設定 {#listing-settings}
   - [檢視清單設定](listing-settings.md)
   - [產品清單動作](product-listing-actions.md)
   - [協力廠商清單](third-party-listing-settings.md)
   - [上市價格](listing-price.md)
   - [(B2B)商業定價](business-pricing.md)
   - [存貨/數量](stock-quantity.md)
   - [履行者](fulfilled-by.md)
   - [目錄搜尋](catalog-search.md)
   - [產品清單條件](product-listing-condition.md)
   - [更新的產品](renewed-products.md)
- [訂單設定](order-settings.md)
- [存放區整合設定](store-integration-settings.md)
- 清單與定價規則 {#rules}
   - [清單規則](listing-rules.md)
   - 定價規則 {#pricing-rules}
      - [管理定價](pricing-products.md)
      - [新增新的定價規則](add-pricing-rule.md)
      - [價格規則一般設定](pricing-rule-general-settings.md)
      - [價格規則條件](pricing-rule-conditions.md)
      - [價格規則動作](pricing-rule-actions.md)
      - [標準價格規則](standard-price-rules.md)
      - [智慧型重新訂價規則](intelligent-repricing-rules.md)
      - [競爭者條件差異](competitor-conditional-variances.md)
      - [價格調整](price-adjustment.md)
      - [底價](floor-price.md)
      - [選擇性最高價格](optional-ceiling-price.md)
      - [價格範圍](price-scope.md)
      - [價格優先順序邏輯](price-priority-logic.md)
      - [Buy Box競爭者定價](buy-box-competitor-pricing.md)
      - [最低競爭者價格](lowest-competitor-pricing.md)
   - 範例 {#rules-examples}
      - [定義條件](ob-define-condition-example.md)
      - [價格規則範例](price-rule-examples.md)
- 報告和記錄 {#reports-logs}
   - [記錄並儲存報告](amazon-logs-reports.md)
   - 存放區報告 {#store-reports}
      - [具競爭力的價格分析](competitive-price-analysis.md)
      - [清單改善](listing-improvements.md)
   - 記錄檔 {#logs}
      - [列出變更記錄](listing-changes-log.md)
      - [通訊錯誤記錄](communication-errors-log.md)
- 管理清單 {#admin-listings}
   - [管理Amazon清單](managing-product-listings.md)
   - 依狀態/標籤 {#status-tab}
      - [按狀態/標籤管理](managing-listings-by-tab.md)
      - [清單不完整](incomplete-listings.md)
      - [新的協力廠商清單](new-third-party-listings.md)
      - [準備列出](ready-to-list.md)
      - [非使用中清單](inactive-listings.md)
      - [作用中的清單](active-listings.md)
      - [覆寫](overrides.md)
      - [不符合資格的清單](ineligible-listings.md)
      - [已結束的清單](ended-listings.md)
   - 依動作 {#actions}
      - [依動作管理](managing-listings-by-action.md)
      - [建立和指派目錄產品](creating-assigning-catalog-products.md)
      - [建立和編輯覆寫](creating-editing-overrides.md)
      - [建立別名賣家SKU](create-alias-seller-sku.md)
      - [編輯指派的ASIN](edit-assigned-asin.md)
      - [結束Amazon清單](end-listings-manually.md)
      - [發佈Amazon清單](publish-listings-manually.md)
      - [更新必要資訊](amazon-manually-update-incomplete-listing.md)
      - [檢視詳細資料](product-listing-details.md)
- 管理訂單 {#admin-orders}
   - [管理訂單](managing-orders.md)
   - [檢視Amazon訂單](amazon-orders-all.md)
   - [檢視Amazon訂單詳細資料](amazon-order-details.md)
   - [常見訂單處理任務](common-order-processing.md)
   - [履行工作流程](fulfillment-workflows.md)
   - [取消未出貨的訂單](cancel-unshipped-order.md)
