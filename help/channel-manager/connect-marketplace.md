---
title: '''连接 [!DNL Channel Manager] to [!DNL Walmart Marketplace]'''
description: “将商务商店视图连接到 [!DNL Walmart Marketplace] 创建销售渠道以管理Walmart Marketplace销售的商务产品清单、库存、价格和订单。”
exl-id: 8c78c582-7b57-4f73-894e-134ba0ba3640
source-git-commit: 8146be1c94ffb1c8abd0d28e53d3476fd78f2c62
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 0%

---

# 连接 [!DNL Channel Manager] to [!DNL Walmart Marketplace]

在上安装Channel Manager后 [!DNL Commerce] 实例中，在渠道管理器中创建销售渠道并配置要连接的凭据 [!DNL Channel Manager] to [!DNL Walmart Marketplace].

1. [创建销售渠道](#create-the-sales-channel) 选择 [!DNL Commerce] 存储以获取产品清单。

1. [将渠道连接到 [!DNL Walmart Marketplace] 通过添加 [!UICONTROL Walmart API credentials]](#connect-the-channel-to-walmart-marketplace).

1. [完成销售渠道设置](#complete-store-setup) 管理列表、库存、定价和订单 [!DNL Walmart Marketplace] 产品分类。

>[!NOTE]
>
>渠道经理要求在沃尔玛帐户和 [!DNL Commerce] 存储视图。 您无法将同一商店视图连接到多个沃尔玛帐户。

## 创建销售渠道

1. 在管理员中，打开 [!DNL Channel Manager] 选择 **[!UICONTROL Marketing** > _渠道&#x200B;_> **渠道管理器]**.

1. 在 **[!UICONTROL Marketplaces available to connect]** 选择 **[!UICONTROL Get Started]**.

   ![连接新 [!DNL Walmart] 存储到 [!DNL Channel Manager]](assets/channel-manager-home.png)

1. 如果需要，请设置 [!DNL Walmart Marketplace Seller] 帐户。

1. 配置存储和连接：

   - 选择 **[!UICONTROL Add Credentials]**.

   - 选择 [!DNL Commerce] 提供要在市场上销售的产品的商店视图。

      ![配置之间的连接 [!DNL Commerce] 和 [!DNL Walmart Marketplace] 从 [!DNL Channel Manager]](assets/configure-commerce-to-marketplace-connection.png)

   - 输入唯一 **[!UICONTROL store name]**.

   - 选择 **[!UICONTROL Adobe [!DNL Commerce] site]** 用于产品清单和订单处理。

   - 接收与 [!DNL Channel Manager]，添加 **[!UICONTROL email address]**.

1. 将渠道连接到 [!DNL Walmart Marketplace].

   - 添加的凭据 [[!DNL Walmart Marketplace Adobe Production API key]](walmart-requirements.md#generate-a-walmart-marketplace-production-api-key) 从 [!DNL Walmart Marketplace Seller] 帐户。

   - 如果您没有凭据，请从 [!DNL Walmart Marketplace Developer Portal] 选择 **[!UICONTROL Get API credentials]**.

      在开发人员门户上，选择您所在的地区（美国和加拿大），然后登录。

      ![[!DNL Walmart Marketplace] 帐户登录](assets/walmart-marketplace-login-page.png)

   - 在API密钥表单中，复制并保存 **[!UICONTROL Client ID]** 和 **[!UICONTROL Client Secret]** 值 [!UICONTROL Adobe Inc Production API key] 到安全位置。

      ![[!DNL Walmart Marketplace API key] 配置页面](assets/walmart-api-key-management-form.png)

      >[!NOTE]
      >
      >如果 [!DNL Adobe Inc] 键未在开发人员门户中列出，请选择 **[!UICONTROL Add New Key for a Solution Provider]** 以配置权限并生成密钥。 有关配置详细信息，请参阅 [生成 [!DNL Walmart Marketplace API Key]](walmart-requirements.md#generate-a-walmart-marketplace-api-key).

   - 返回 [!DNL Channel Manager] 将凭据添加到 **[!UICONTROL Walmart Connection]** 信息。

      添加凭据时，Adobe会隐藏客户端密钥并将值存储在安全电子仓库中。

1. 选择 **[!UICONTROL Save Store]** 应用配置并连接到 [!DNL Walmart marketplace].

1. 成功连接后， [完整商店设置](complete-store-setup.md) 从 **[!UICONTROL Channel Manager]** 存储页面。

![设置第一个商店](assets/channel-manager-setup-first-store.png)

### 连接问题疑难解答

如果与 [!DNL Walmart] 失败，查看 [Walmart Marketplace常见问题解答](https://developer.walmart.com/faq/us/faq-auth/){target=&quot;_blank&quot;}以了解疑难解答提示。

- 从 [!DNL Walmart Developer Portal]，确认您复制了 [!UICONTROL Adobe Inc.]

- 验证的访问配置 [!UICONTROL Walmart Adobe API key] 具有正确的权限。 请参阅 [[!DNL Walmart Requirements]](walmart-requirements.md##generate-a-walmart-marketplace-api-key).

- 确认 [!DNL Walmart API] 服务可从 [Walmart API状态页面](https://developer.walmart.com/us/whats-new/new-api-status-information-now-available/){target=&quot;_blank&quot;}。
