---
title: Sales Channel設定
description: 若要管理Amazon銷售管道功能的記錄、cron來源和同步，請更新Commerce設定。
exl-id: 69f83774-41de-4fde-a357-f100d1bcd9f0
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---

# Sales Channel設定

當 [!DNL Amazon Sales Channel] 已安裝擴充功能，預設值是在Amazon sales channel的「管理員」中設定。 您可以在Amazon商店的組態設定中修改這些設定。 這些設定包括：

- 清除活動記錄記錄的間隔
- Cron來源選擇
- 記錄同步選項

## 修改Commerce管道設定

1. 於 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Sales Channels]** 並選擇 **[!UICONTROL Global Settings]**.

1. 對象 **[!UICONTROL Clear Log History]**，選擇一個選項：

   - `Once Daily`  — 選擇每天清除一次商店活動歷史記錄。

   - `Once Weekly`  — 選擇每週清除一次商店活動歷史記錄。

   - `Once Monthly` - （預設）選擇每月清除一次商店活動歷史記錄。

1. 對象 **[!UICONTROL Background Tasks (CRON) Source]**，選擇 `Magento CRON`.

   此選項可讓Amazon銷售管道使用您的 [!DNL Commerce] [Cron](https://docs.magento.com/user-guide/system/cron.html) 用來決定通訊和資料同步間隔的設定 [!DNL Amazon Seller Central].

1. 對象 **[!UICONTROL Enable Debug Logging]**，選擇 `Enabled` 以便在需要疑難排解時收集其他同步處理資料。

   Amazon sales channel logging會寫入 `{Commerce Root}/var/log/channel_amazon.log` 檔案及檢視位置 [開發人員模式](https://docs.magento.com/user-guide/magento/installation-modes.html){target="_blank"}. 記錄只應為 `Enabled` 進行疑難排解期間，應該 `Disabled` 疑難排解完成時。

1. 對象 **[!UICONTROL Read-Only Mode]**，選取 `Enabled` 以封鎖所有外寄狀態變更API要求。

   使用此設定時，可能會儲存變更，但直到 [!UICONTROL Read-Only Mode] 已停用。 必須清除設定快取，才能啟用唯讀模式。 若要再次開始資料傳輸，請選取「 」 `Disabled`.

   >[!IMPORTANT]
   >
   >[!UICONTROL Read-Only Mode] 是專為生產執行個體的副本而設計，例如中繼或QA，不應在生產執行個體上使用。
   >
   >當資料庫移轉至執行個體的新復本時（當存放區的URL在設定中變更時偵測到）， [!UICONTROL Read-Only Mode] 會自動啟用。

1. 按一下 **[!UICONTROL Save Config]**.

![Sales Channel組態設定](assets/config-sales-channel-global-settings.png)
