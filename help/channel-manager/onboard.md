---
title: 板载 [!DNL Channel Manager]
description: 将您的实例连接到 [!DNL Channel Manager] 服务，只需完成几个入门步骤。
role: User
level: Intermediate
exl-id: 7c4ccd9e-ae32-4511-8d1e-baa690604612
source-git-commit: 638ba8c595652e66aa5f15f5207855c6d2b872d7
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 0%

---


# 板载 [!DNL Channel Manager]

完成入门后，请通过 [!UICONTROL Channel Manager] 选项 [!UICONTROL Commerce Admin Marketing] 菜单。

![[!DNL Channel Manager] 管理视图中的选项](assets/channel-manager-admin-view.png)

## 入门概述

1. [安装 [!DNL Channel Manager] 扩展](install.md).

1. [配置 [!DNL Commerce Services Connector]](connect.md) 将渠道管理器与商务实例及其他支持服务相集成。

1. [连接 [!DNL Commerce] 存储到 [!DNL Walmart Marketplace]](connect.md).

1. [完成商店设置](complete-store-setup.md).

## 要求

- 确认您满足 [Walmart Marketplace要求](walmart-requirements.md) 与渠道管理器集成。

- **商务帐户信息** — 下载和安装 [!DNL Channel Manager] 需要 [商务帐户](https://docs.magento.com/user-guide/magento/magento-account.html){target=&quot;_blank&quot;}。 您需要具有以下权限的帐户ID和凭据：拥有 [!DNL Adobe Commerce] 或 [!DNL Magento Open Source] 实例。

   - **图像ID**-[登录](https://account.magento.com/customer/account/login/) 到 [!DNL Commerce] 从获取ID的帐户 **[!UICONTROL My Account - Magento settings]**.

      ![[!DNL MAGEID] on [!DNL Commerce] 帐户设置](assets/mageid-my-commerce-account.png)

   - **访问密钥 —** 获取要下载的身份验证密钥 [!DNL Commerce] 扩展 [!DNL Commerce] 编辑器存储库 `([!DNL repo.magento.com]`)。

      ![[!UICONTROL Commerce Marketplace access keys]](assets/commerce-marketplace-access-keys.png)

      在Adobe Commerce和Magento Open Source项目中，所有者可以设置 [共享访问](https://docs.magento.com/user-guide/magento/magento-account-share.html) 允许受信任的员工和服务提供商使用所有者或许可证持有者帐户的凭据下载扩展。

      对于 [!DNL Adobe Commerce] 在云基础架构项目上，软件安装程序必须具有以下访问 [!DNL Commerce] 实例：

      - 超级用户对云项目的访问权限
      - 对特定环境的管理员访问权限
      - an [!DNL Adobe Commerce] 或 [!DNL Magento Open Source] 具有访问编辑器存储库权限的帐户

      请参阅 [管理用户访问权限](https://devdocs.magento.com/cloud/project/user-admin.html).


- **使用编辑器和[!DNL Commerce CLI]**  — 请参阅 [常规CLI安装](https://devdocs.magento.com/extensions/install/){target=&quot;_blank&quot;}以了解有关使用这些工具在上安装和配置扩展的信息 [!DNL Adobe Commerce] 或 [!DNL Magento Open Source] 平台。

- [[!DNL Amazon Sales Channel] 版本4.4.2或更高版本](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html) — 如果您已激活 [!DNL Amazon Sales Channel] , [!DNL Commerce] 站点，验证 [!DNL Commerce] 在安装之前，平台已安装版本4.4.2 [!DNL Channel Manager].

- [!DNL Inventory Management] Adobe Commerce和Magento Open Source的扩展

   如果您计划使用渠道管理器进行库存和订单管理，则必须在Adobe Commerce和Magento Open Source实例上安装并启用Inventory management扩展。 通常，此扩展默认安装并在Adobe Commerce和Magento Open Source2.3.x及更高版本上启用。

   如果您已从2.2.x升级了Commerce，或者如果您已禁用Inventory management，则必须更新安装以包含所需的模块。 有关更多信息，请参阅 [安装Inventory management](https://devdocs.magento.com/extensions/inventory-management/) ，位于Adobe Commerce开发人员文档中。

### 系统要求

- [Adobe Commerce 2.4.x](https://devdocs.magento.com/release/released-versions.html)
- [7.3菲律宾比索/7.4](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/php-settings.html)
- [编辑器1.x或更高版本](https://devdocs.magento.com/cloud/reference/cloud-composer.html)
- [[!DNL Amazon Sales Channel] 版本4.4.2或更高版本](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html) — 如果您已激活 [!DNL Amazon Sales Channel] , [!DNL Commerce] 站点，验证 [!DNL Commerce] 在安装之前，平台已安装版本4.4.2 [!DNL Channel Manager].
- [[!DNL Inventory Management]](https://devdocs.magento.com/extensions/inventory-management/)

### 支持的平台

- Adobe Commerce on Cloud(ECE):2.4.x
- Adobe Commerce on premise(EE):2.4.x
- Magento Open Source2.4.x
