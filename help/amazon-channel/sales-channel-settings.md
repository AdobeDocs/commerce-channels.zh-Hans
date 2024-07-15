---
title: Sales channel设置
description: 要管理Amazon销售渠道功能的日志记录、cron源和同步，请更新Commerce配置。
exl-id: 69f83774-41de-4fde-a357-f100d1bcd9f0
role: Admin, Developer
feature: Sales Channels, Configuration, Logs
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# Sales channel设置

安装[!DNL Amazon Sales Channel]扩展后，将在Amazon销售渠道的管理员中设置默认值。 可以在Amazon应用商店的配置设置中修改这些设置。 这些设置包括：

- 清除活动日志历史记录的时间间隔
- Cron源选择
- 日志同步选项

## 修改Commerce渠道设置

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales Channels]**&#x200B;并选择&#x200B;**[!UICONTROL Global Settings]**。

1. 对于&#x200B;**[!UICONTROL Clear Log History]**，请选择一个选项：

   - `Once Daily` — 选择每天清除一次商店活动历史记录。

   - `Once Weekly` — 选择每周清除一次您的商店活动历史记录。

   - `Once Monthly` — （默认）选择每月清除一次商店活动历史记录。

1. 对于&#x200B;**[!UICONTROL Background Tasks (CRON) Source]**，请选择`Magento CRON`。

   此选项允许Amazon销售渠道使用您的[!DNL Commerce] [Cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html)设置来确定与[!DNL Amazon Seller Central]的通信和数据同步间隔。

1. 对于&#x200B;**[!UICONTROL Enable Debug Logging]**，选择`Enabled`以在需要故障排除时收集其他同步数据。

   Amazon sales channel日志记录已写入`{Commerce Root}/var/log/channel_amazon.log`文件，可以在[开发人员模式](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/developer-tools.html#operation-modes)中查看。 疑难解答期间日志记录只应为`Enabled`，疑难解答完成时日志记录应为`Disabled`。

1. 对于&#x200B;**[!UICONTROL Read-Only Mode]**，选择`Enabled`以阻止所有传出状态更改的API请求。

   使用此设置，在禁用[!UICONTROL Read-Only Mode]之前，可能会保存更改，但不会发送更改。 必须清除配置缓存，才能启用只读模式。 要再次开始数据传输，请选择`Disabled`。

   >[!IMPORTANT]
   >
   >[!UICONTROL Read-Only Mode]专为生产实例的副本（如暂存或QA）而设计，不应在生产实例上使用。
   >
   >将数据库迁移到实例的新副本时（当存储的URL在配置中更改时检测到），[!UICONTROL Read-Only Mode]将自动启用。

1. 单击&#x200B;**[!UICONTROL Save Config]**。

![Sales Channel配置设置](assets/config-sales-channel-global-settings.png){width="600" zoomable="yes"}
