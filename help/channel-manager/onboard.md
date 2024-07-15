---
title: 板载 [!DNL Channel Manager]
description: '通过完成一些入门培训步骤，将您的实例连接到 [!DNL Channel Manager] 服务。'
level: Intermediate
role: Leader, Admin, Developer
feature: Sales Channels, Install
exl-id: 7c4ccd9e-ae32-4511-8d1e-baa690604612
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 0%

---


# 载入[!DNL Channel Manager]

完成渠道经理新用户引导流程后，您可以从Adobe Commerce访问、配置和管理Walmart Marketplace渠道销售操作。 通过[!UICONTROL Commerce Admin Marketing]菜单中的[!UICONTROL Channel Manager]选项可以使用渠道管理器。

管理员视图中的![[!DNL Channel Manager]选项](assets/channel-manager-admin-view.png){width="500"}

## 要求

查看使用渠道管理器的要求，并收集下载、安装和配置扩展所需的帐户信息和凭据。

- **[Walmart Marketplace要求](walmart-requirements.md)** — 验证您是否满足与渠道管理器集成的要求，包括[设置您的卖方帐户](https://sellerhelp.walmart.com/seller/s/guide?article=000008219)并生成API密钥以启用集成。

- **Commerce帐户信息** — 下载和安装[!DNL Channel Manager]需要[Commerce帐户](https://experienceleague.adobe.com/docs/commerce-admin/start/commerce-account/commerce-account-create.html)。 您需要具有对[!DNL Adobe Commerce]或[!DNL Magento Open Source]实例的所有者或管理员访问权限的帐户ID和凭据。

   - **图像ID**-[登录](https://account.magento.com/customer/account/login/)到[!DNL Commerce]帐户以从&#x200B;**[!UICONTROL My Account - Magento settings]**&#x200B;获取ID。

     [!DNL Commerce]帐户设置上的![[!DNL MAGEID]](assets/mageid-my-commerce-account.png){width="250"}

   - **访问密钥 —**&#x200B;获取身份验证密钥以从[!DNL Commerce]编辑器存储库`([!DNL repo.magento.com]`下载[!DNL Commerce]扩展。

     ![[!UICONTROL Commerce Marketplace access keys]](assets/commerce-marketplace-access-keys.png){width="400"}

     在Adobe Commerce和Magento Open Source项目中，所有者可以设置[共享访问](https://experienceleague.adobe.com/docs/commerce-admin/start/commerce-account/commerce-account-share.html)，以允许受信任的员工和服务提供商使用所有者或许可证持有人帐户的凭据下载扩展。

     对于云基础架构项目上的[!DNL Adobe Commerce]，软件安装程序必须对[!DNL Commerce]实例具有以下访问权限：

      - 超级用户对云项目的访问权限
      - 管理员访问特定环境
      - 具有访问Composer存储库权限的[!DNL Adobe Commerce]帐户

     请参阅《云基础架构上的Commerce *指南*&#x200B;中的[管理用户访问权限](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html)。

- **使用编辑器和[!DNL Commerce CLI]**&#x200B;的体验 — 请参阅&#x200B;*安装指南*&#x200B;中的[安装扩展](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html)，了解有关使用这些工具在[!DNL Adobe Commerce]或[!DNL Magento Open Source]平台上安装和管理扩展的信息。

- **[[!DNL Amazon Sales Channel] 版本4.4.2或更高版本](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html)** — 如果您为[!DNL Commerce]站点激活了[!DNL Amazon Sales Channel]，请在安装[!DNL Channel Manager]之前验证您的[!DNL Commerce]平台是否安装了4.4.2或更高版本。

- Adobe Commerce和Magento Open Source的&#x200B;**[!DNL Inventory Management]扩展**

  如果您计划使用Channel Manager进行库存和订单管理，则必须在Adobe Commerce和Magento Open Source实例上安装并启用Inventory management扩展。 通常，此扩展已安装并在Adobe Commerce和[!DNL Magento Open Source] 2.3.x及更高版本上默认启用。

  如果从2.2.x升级Commerce，或者已禁用Inventory management，请更新安装以包含所需的模块。 请参阅&#x200B;*Inventory management指南*&#x200B;中的[安装Inventory management](https://experienceleague.adobe.com/docs/commerce-admin/inventory/get-started/install-update.html)。

### 系统要求

- [Adobe Commerce 2.4.x](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html)
- [PHP 7.3 / 7.4](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html)
- [Composer 1.x或更高版本](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/overview.html)
- [[!DNL Amazon Sales Channel] 版本4.4.2或更高版本](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html) — 如果您已经为[!DNL Commerce]站点激活了[!DNL Amazon Sales Channel]，请在安装[!DNL Channel Manager]之前验证您的[!DNL Commerce]平台是否已安装版本4.4.2。
- [[!DNL Inventory Management]](https://experienceleague.adobe.com/docs/commerce-admin/inventory/get-started/install-update.html)

### 支持的平台

- Adobe Commerce on Cloud (ECE) ：2.4.x
- Adobe Commerce内部部署(EE)：2.4.x
- Magento Open Source2.4.x

## 载入步骤

1. [设置你的沃尔玛卖家帐户](https://seller.walmart.com/signup?q=&amp;origin=solution_provider&amp;src=0014M00001zivMp)。

1. [安装 [!DNL Channel Manager] 扩展](install.md)。

1. [连接到Commerce服务](connect.md)以将渠道管理器与Commerce实例以及其他支持服务集成。

1. [将你的 [!DNL Commerce] 存储连接到 [!DNL Walmart Marketplace]](connect-marketplace.md)。

1. [完成商店设置](complete-sales-channel-store-setup.md)。
