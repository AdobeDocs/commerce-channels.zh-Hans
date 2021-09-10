---
title: Sales Channel设置
description: 要管理Amazon销售渠道功能的日志记录、cron源和同步，请更新商务配置。
exl-id: 69f83774-41de-4fde-a357-f100d1bcd9f0
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---

# Sales Channel设置

安装[!DNL Amazon Sales Channel]扩展后，会在“Amazon销售渠道的管理员”中设置默认值。 可以在Amazon存储的配置设置中修改这些设置。 这些设置包括：

- 清除活动日志历史记录的间隔
- Cron源选择
- 日志同步选项

## 修改商务渠道设置

1. 在&#x200B;_Admin_&#x200B;侧栏中，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales Channels]**&#x200B;并选择&#x200B;**[!UICONTROL Global Settings]**。

1. 对于&#x200B;**[!UICONTROL Clear Log History]**，选择一个选项：

   - `Once Daily`  — 选择每天清除一次您的商店活动历史记录。

   - `Once Weekly`  — 选择每周清除一次您的商店活动历史记录。

   - `Once Monthly`  — （默认）选择每月清除一次您的商店活动历史记录。

1. 对于&#x200B;**[!UICONTROL Background Tasks (CRON) Source]**，选择`Magento CRON`。

   此选项允许Amazon销售渠道使用[!DNL Commerce] [Cron](https://docs.magento.com/user-guide/system/cron.html)设置来确定与[!DNL Amazon Seller Central]的通信和数据同步间隔。

1. 对于&#x200B;**[!UICONTROL Enable Debug Logging]**，选择`Enabled`以在需要进行故障排除时收集其他同步数据。

   Amazon销售渠道日志记录将写入`{Commerce Root}/var/log/channel_amazon.log`文件，并可在[developer mode](https://docs.magento.com/user-guide/magento/installation-modes.html){:target=&quot;_blank&quot;}中查看。 在故障排除期间，日志记录应该只为`Enabled`，在故障排除完成时，日志记录应该为`Disabled`。

1. 单击&#x200B;**[!UICONTROL Save Config]**。

![Sales Channel配置设置](assets/config-sales-channel-global-settings.png)
