---
title: 板载 [!DNL Channel Manager]
description: 将您的实例连接到 [!DNL Channel Manager] 服务，方法是完成一些入门步骤。
role: User
level: Intermediate
exl-id: 7c4ccd9e-ae32-4511-8d1e-baa690604612
source-git-commit: f57c6db4c0314272d10bb5483d2c8a0ae396a9fc
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 0%

---

# 板载 [!DNL Channel Manager]

通过在您的 [!DNL Commerce] 实例和配置API连接。 这些连接支持您的商务实例与Walmart Marketplace之间的通信和数据同步。

完成入门后，请通过 [!UICONTROL Channel Manager] 选项 [!UICONTROL Commerce Admin Marketing] 菜单。

![[!DNL Channel Manager] 管理视图中的选项](assets/channel-manager-admin-view.png)

## 入门概述

1. [安装 [!DNL Channel Manager] 扩展](install.md).

1. [配置 [!DNL Commerce Services Connector]](connect.md) 将渠道管理器与商务实例及其他支持服务相集成。

1. [连接 [!DNL Commerce] 存储到 [!DNL Walmart Marketplace]](connect.md).

1. [完成商店设置](complete-store-setup.md).

## 先决条件

- 确认您具有 [Walmart Marketplace先决条件](walmart-prerequisites.md) 与渠道管理器集成。

- **商务帐户信息** — 下载和安装 [!DNL Channel Manager] 需要 [商务帐户](https://docs.magento.com/user-guide/magento/magento-account.html){target=&quot;_blank&quot;}。 您需要具有以下权限的帐户ID和凭据：拥有 [!DNL Adobe Commerce] 或 [!DNL Magento Open Source] 实例。

   - **图像ID**-[登录](https://account.magento.com/customer/account/login/) 到商务帐户，以从 **[!UICONTROL My Account - Magento settings]**. 您需要此ID才能注册 [!DNL Channel Manager] 服务测试版计划。

      ![[!DNL MAGEID] 商务帐户设置](assets/mageid-my-commerce-account.png)

   - **访问密钥 —** 获取身份验证密钥，以从商务编辑器存储库下载商务扩展 `([!DNL repo.magento.com]`)。

      ![[!UICONTROL Commerce Marketplace access keys]](assets/commerce-marketplace-access-keys.png)

      在Adobe Commerce和Magento Open Source项目中，所有者可以设置 [共享访问](https://docs.magento.com/user-guide/magento/magento-account-share.html) 允许受信任的员工和服务提供商使用所有者或许可证持有者帐户的凭据下载扩展。

      开 [!DNL Adobe Commerce] 在云基础架构项目上，软件安装程序必须具有以下访问权限 [!DNL Commerce] 实例：

      - 超级用户对云项目的访问权限
      - 对特定环境的管理员访问权限
      - an [!DNL Adobe Commerce] 或 [!DNL Magento Open Source] 具有访问编辑器存储库权限的帐户。

      请参阅 [管理用户访问权限](https://devdocs.magento.com/cloud/project/user-admin.html).


- **授权下载渠道管理器编辑器包** — 将用于管理服务的商务帐户中的MAGE ID提供给Adobe代表，该代表负责协调贵组织的测试版计划。
- **使用编辑器和[!DNL Commerce CLI]**  — 请参阅 [常规CLI安装](https://devdocs.magento.com/extensions/install/){target=&quot;_blank&quot;}以了解有关使用这些工具在上安装和配置扩展的信息 [!DNL Adobe Commerce] 或 [!DNL Magento Open Source] 平台。
- **[AmazonSales Channel版本4.4.2或更高版本](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html) — 如果已为商务网站激活AmazonSales Channel，请在安装渠道管理器之前，验证您的商务平台是否安装了版本4.42。


### 要求

- [Adobe Commerce 2.4.x](https://devdocs.magento.com/release/released-versions.html)
- [7.3菲律宾比索/7.4](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/php-settings.html)
- [编辑器1.x或更高版本](https://devdocs.magento.com/cloud/reference/cloud-composer.html)


### 支持的平台

- Adobe Commerce on Cloud(ECE):2.4.x
- Adobe Commerce on premise(EE):2.4.x
- Magento Open Source2.4.x
