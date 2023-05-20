---
title: 記錄檔和存放區報告
description: 使用記錄檔和商店報告來檢視Adobe Commerce或Magento Open Source商店的狀況，以及您的Amazon Marketplace清單。
exl-id: 4654f718-d15f-4c3b-b984-ac7b9c29e6c4
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---

# 記錄檔和存放區報告

Amazon Sales Channel擴充功能包括一些重要的記錄檔和商店報告，可讓您檢視影響Amazon清單和訂單的變更。 您可以使用這些報表來檢視商店中發生的事，並瞭解各種清單狀態。

記錄或存放區報告沒有可用的動作，因為它們是僅限檢閱的功能。

下列記錄檔可從 [存放區儀表板](./amazon-store-dashboard.md).

- 此 [列出變更記錄](./listing-changes-log.md) 顯示您的Amazon賣家帳戶所發生的變更，以反映您的Amazon銷售管道設定。

- 此 [通訊錯誤記錄](./communication-errors-log.md) 顯示與Amazon之間任何回報的通訊錯誤。

下列商店特定報表可從以下網址存取： [存放區儀表板](./amazon-store-dashboard.md).

- 此 [具競爭力的價格分析](./competitive-price-analysis.md) 報表顯示您的Amazon _到岸價格_ （上市價格加運費）與以下各項之比較： [Buy Box](./buy-box-competitor-pricing.md) 價格與 [最低競爭者](./lowest-competitor-pricing.md) 價格。

- 此 [清單改善](./listing-improvements.md) 報表會顯示Amazon針對選定商店所提供的所有建議清單改善。

>[!TIP]
>
>如需疑難排解的其他資訊，您也可以檢視記錄檔。 另請參閱 [sales channel管理設定](./sales-channel-settings.md). Amazon sales channel synchronization logging會寫入 `{Commerce Root}/var/log/channel_amazon.log` 檔案及檢視位置 [開發人員模式](https://docs.magento.com/user-guide/magento/installation-modes.html){target="_blank"}.
