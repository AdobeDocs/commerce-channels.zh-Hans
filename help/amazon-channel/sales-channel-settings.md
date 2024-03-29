---
title: Sales channel设置
description: 要管理Amazon Sales Channel功能的日志记录、cron源和同步，请更新Commerce配置。
exl-id: 69f83774-41de-4fde-a357-f100d1bcd9f0
role: Admin, Developer
feature: Sales Channels, Configuration, Logs
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# Sales channel设置

当 [!DNL Amazon Sales Channel] 扩展已安装，在Amazon sales channel的Admin中设置默认值。 可以在Amazon应用商店的配置设置中修改这些设置。 这些设置包括：

- 清除活动日志历史记录的时间间隔
- Cron源选择
- 日志同步选项

## 修改Commerce渠道设置

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Sales Channels]** 并选择 **[!UICONTROL Global Settings]**.

1. 对象 **[!UICONTROL Clear Log History]**，选择一个选项：

   - `Once Daily`  — 选择每天清除一次商店活动历史记录。

   - `Once Weekly`  — 选择每周清除一次商店活动历史记录。

   - `Once Monthly`  — （默认）选择每月清除一次商店活动历史记录。

1. 对象 **[!UICONTROL Background Tasks (CRON) Source]**，选择 `Magento CRON`.

   此选项允许Amazon sales channel使用 [!DNL Commerce] [Cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html) 用于确定通信和数据同步间隔的设置 [!DNL Amazon Seller Central].

1. 对象 **[!UICONTROL Enable Debug Logging]**，选择 `Enabled` 在需要故障排除时收集其他同步数据。

   Amazon sales channel日志记录将写入 `{Commerce Root}/var/log/channel_amazon.log` 文件并可在 [开发者模式](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/developer-tools.html#operation-modes). 日志记录只应 `Enabled` 进行故障排除期间，应该 `Disabled` 故障排除完成后。

1. 对象 **[!UICONTROL Read-Only Mode]**，选择 `Enabled` 阻止所有传出状态更改的API请求。

   使用此设置，可能会保存的更改不会被发送，直到 [!UICONTROL Read-Only Mode] 已禁用。 必须清除配置缓存，才能启用只读模式。 要再次开始数据传输，请选择 `Disabled`.

   >[!IMPORTANT]
   >
   >[!UICONTROL Read-Only Mode] 专门为生产实例的副本（如暂存或QA）而设计，不应在生产实例上使用。
   >
   >将数据库迁移到实例的新副本时（当存储的URL在配置中更改时检测到）， [!UICONTROL Read-Only Mode] 将自动启用。

1. 单击 **[!UICONTROL Save Config]**.

![Sales Channel配置设置](assets/config-sales-channel-global-settings.png){width="600" zoomable="yes"}
