---
title: '将Sales Channel连接到 [!DNL Walmart Marketplace] '
description: 配置销售渠道并连接到Walmart Marketplace。
source-git-commit: ff87f31fec7a689385a93b8cab260fd93ff15f90
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---

# 连接到 [!DNL Walmart Marketplace]

在上安装Channel Manager后 [!DNL Commerce] 例如，将商务商店连接到Walmart Marketplace。

1. 通过 [为产品清单选择商务商店](#select-the-commerce-store-for-the-sales-channel).

1. [将渠道连接到 [!DNL Walmart Marketplace] 通过添加Walmart API凭据](#connect-the-channel-to-walmart-marketplace).

1. [完成销售渠道设置](#complete-store-setup) 以便您能够从渠道管理器管理列表、库存、定价和销售。

## 创建销售渠道

1. 打开渠道管理器。

   - 在管理员中，选择 **[!UICONTROL Marketing** > _渠道&#x200B;_> **渠道管理器]**.

   - 选择 **[!UICONTROL Connect New Store]**.

      ![将Commerce商店连接到 [!DNL Walmart Marketplace] 从 [!DNL Channel Manager]](assets/connect-commerce-store-to-marketplace.png)


1. 配置存储和连接：

   - 输入唯一 **[!UICONTROL store name]**.

   - 选择 **[!UICONTROL Adobe Commerce site]** （对于产品列表）。

   - 添加 **[!UICONTROL email address]** 接收与 [!DNL Channel Manager].

      ![配置商务与 [!DNL Walmart Marketplace] 从 [!DNL Channel Manager]](assets/configure-commerce-to-marketplace-connection.png)


## 将渠道连接到Walmart Marketplace

1. 添加的凭据 [!DNL Walmart Marketplace Adobe Production API key] 从 [!DNL Walmart Marketplace Seller] 帐户。

   - 如果您没有凭据，请选择 **[!UICONTROL Get API credentials]** 从 [!DNL Walmart Marketplace Developer Portal].

      如果出现提示，请选择您所在的地区（美国和加拿大），然后登录。

      ![[!DNL Walmart Marketplace] 帐户登录](assets/walmart-marketplace-login-page.png)

   - 在API密钥表单中，复制并保存 **[!UICONTROL Client ID]** 和 **[!UICONTROL Client Secret]** 值 [!UICONTROL Adobe Inc Production API key] 到安全位置。

      ![[!DNL Walmart Marketplace API key] 配置页面](assets/walmart-api-key-management-form.png)

      >[!NOTE]
      >
      >如果您没有看到 [!DNL Adobe Inc] 键，请选择 **[!UICONTROL Add New Key for a Solution Provider]** 以配置权限并生成密钥。 有关配置详细信息，请参阅 [生成 [!DNL Walmart Marketplace API Key]](overview.md#generate-a-walmart-marketplace-api-key).

   - 返回 [!DNL Channel Manager] 将凭据添加到 **[!UICONTROL Walmart Connection]** 信息。

      将凭据添加到时 [!DNL Channel Manager]，则Adobe会隐藏客户端密钥并将值存储在安全电子仓库中。

1. [!UICONTROL Save] 用于建立连接的配置。

   成功连接后，从 **[!UICONTROL Channel Manager > Marketplace Stores]**.

   ![[!DNL Walmart Marketplace API key] 配置页面](assets/manage-connected-stores.png)


### 连接问题疑难解答

如果与沃尔玛的连接失败，请查看 [Walmart Marketplace常见问题解答](https://developer.walmart.com/faq/us/faq-auth/){target=&quot;_blank&quot;}以了解疑难解答提示。

- 从 [!DNL Walmart Developer Portal]，确认您复制了 [!UICONTROL Adobe Inc.]

- 验证WalmartAdobeAPI密钥的访问配置是否具有正确的权限。 请参阅 [沃尔玛先决条件](overview.md#walmart-prerequisites).

- 确认Walmart API服务可从 [Walmart API状态页面](https://developer.walmart.com/us/whats-new/new-api-status-information-now-available/){target=&quot;_blank&quot;}。


## 完成商店设置

将Commerce商店连接到 [!DNL Walmart Marketplace]，则可以通过 [!DNL Channel Manager Stores] 中。

要完成存储设置，请执行以下操作：

1. 从管理员中，选择**[!UICONTROL Marketing** > **渠道管理器**].

   ![[!DNL Walmart Marketplace API key] 配置页面](assets/connect-commerce-store-config.png)

1. 通过选择商店登入行中的铅笔图标，打开连接的销售渠道。

1. 开始销售渠道操作。

   - 将商务目录中的产品添加到渠道管理器

   - 使用产品匹配将产品发布到沃尔玛

   - 查看和管理库存和定价

   - 从商务管理员查看和管理Walmart订单
