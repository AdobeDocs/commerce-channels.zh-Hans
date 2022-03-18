---
title: Sales Channel设置
description: To manage logging, cron source, and synchronization for Amazon sales channel functions, update the Commerce configuration.
exl-id: 69f83774-41de-4fde-a357-f100d1bcd9f0
source-git-commit: 5508fe6e6b2193eaaebc78f485aae972504554cc
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 0%

---

# Sales Channel设置

当 [!DNL Amazon Sales Channel] 扩展中，默认值在Amazon销售渠道的管理员中设置。 可以在Amazon存储的配置设置中修改这些设置。 These settings include:

- 清除活动日志历史记录的间隔
- Cron源选择
- 日志同步选项

## 修改商务渠道设置

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Sales Channels]** and choose **[!UICONTROL Global Settings]**.

1. For **[!UICONTROL Clear Log History]**, choose an option:

   - `Once Daily` - Choose to clear your store activity history once daily.

   - `Once Weekly`  — 选择每周清除一次您的商店活动历史记录。

   - `Once Monthly`  — （默认）选择每月清除一次您的商店活动历史记录。

1. 对于 **[!UICONTROL Background Tasks (CRON) Source]**，选择 `Magento CRON`.

   此选项允许Amazon销售渠道使用 [!DNL Commerce] [克龙](https://docs.magento.com/user-guide/system/cron.html) 确定通信和数据同步间隔的设置 [!DNL Amazon Seller Central].

1. 对于 **[!UICONTROL Enable Debug Logging]**，选择 `Enabled` 以在需要进行故障诊断时收集其他同步数据。

   Amazon销售渠道日志记录会写入 `{Commerce Root}/var/log/channel_amazon.log` 文件，并可在 [开发人员模式](https://docs.magento.com/user-guide/magento/installation-modes.html){target=&quot;_blank&quot;}。 Logging should only be `Enabled` during troubleshooting and should be `Disabled` when troubleshooting is complete.

1. 对于 **[!UICONTROL Read-Only Mode]**，选择 `Enabled` 以阻止所有传出状态更改API请求。

   使用此设置，在保存潜在更改后，才会发送潜在更改 [!UICONTROL Read-Only Mode] 已禁用。 必须清除配置缓存才能启用只读模式。 要再次开始数据传输，请选择 `Disabled`.

   >[!IMPORTANT]
   >
   >[!UICONTROL Read-Only Mode] 专为生产实例的副本（如暂存或QA）设计，不应在生产实例上使用。
   >
   >将数据库迁移到实例的新副本时（在配置中存储的URL发生更改时检测到）， [!UICONTROL Read-Only Mode] 自动启用。

1. 单击 **[!UICONTROL Save Config]**.

![Sales Channel配置设置](assets/config-sales-channel-global-settings.png)
