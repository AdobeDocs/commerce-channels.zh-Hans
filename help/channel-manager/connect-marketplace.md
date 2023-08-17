---
title: '''连接 [!DNL Channel Manager] 到 [!DNL Walmart Marketplace]’'
description: 将Commerce商店视图连接到 [!DNL Walmart Marketplace] 创建销售渠道以管理Commerce产品列表、库存、价格和沃尔玛商店的订单。”
exl-id: 8c78c582-7b57-4f73-894e-134ba0ba3640
role: Admin, Developer
feature: Sales Channels, Install, Integration
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%

---

# 连接 [!DNL Channel Manager] 到 [!DNL Walmart Marketplace]

在上安装渠道管理器后 [!DNL Commerce] 实例，在Channel Manager中创建一个sales channel并配置要连接的凭据 [!DNL Channel Manager] 到 [!DNL Walmart Marketplace].

1. [创建销售渠道](#create-the-sales-channel) 通过选择 [!DNL Commerce] 存储产品列表。

1. [将渠道连接到 [!DNL Walmart Marketplace] 通过添加 [!UICONTROL Walmart API credentials]](#connect-the-channel-to-walmart-marketplace).

1. [完成销售渠道设置](#complete-sales-channel-store-setup) 管理您的清单、库存、定价和订单 [!DNL Walmart Marketplace] 产品分类。

>[!NOTE]
>
>“渠道管理器”要求沃尔玛帐户与 [!DNL Commerce] 商店视图。 不能将同一商店视图连接到多个Walmart帐户。

## 创建销售渠道

1. 从管理员中，打开 [!DNL Channel Manager] 通过选择 **[!UICONTROL Marketing** > _渠道&#x200B;_> **渠道管理器]**.

1. 在 **[!UICONTROL Marketplaces available to connect]** 部分，选择 **[!UICONTROL Get Started]**.

   ![连接新的 [!DNL Walmart] 存储到 [!DNL Channel Manager]](assets/channel-manager-home.png){width="700" zoomable="yes"}

1. 如果需要，请设置 [!DNL Walmart Marketplace Seller] 帐户。

1. 配置存储和连接：

   - 选择 **[!UICONTROL Add Credentials]**.

   - 选择 [!DNL Commerce] 商店视图，提供您要在Marketplace上销售的产品。

     ![配置之间的连接 [!DNL Commerce] 和 [!DNL Walmart Marketplace] 从 [!DNL Channel Manager]](assets/configure-commerce-to-marketplace-connection.png){width="500" zoomable="yes"}

   - 输入唯一值 **[!UICONTROL store name]**.

   - 选择 **[!UICONTROL Adobe [!DNL Commerce] site]** 用于产品列表和订单处理。

   - 接收与相关的通知 [!DNL Channel Manager]，添加 **[!UICONTROL email address]**.

1. 将渠道连接到 [!DNL Walmart Marketplace].

   - 添加凭据 [[!DNL Walmart Marketplace Adobe Production API key]](walmart-requirements.md#generate-a-walmart-marketplace-production-api-key) 来自您的 [!DNL Walmart Marketplace Seller] 帐户。

   - 如果您没有凭据，请从 [!DNL Walmart Marketplace Developer Portal] 通过选择 **[!UICONTROL Get API credentials]**.

     在开发人员门户上，选择您所在的地区（美国和加拿大），然后登录。

     ![[!DNL Walmart Marketplace] 帐户登录](assets/walmart-marketplace-login-page.png){width="600"}

   - 在API密钥表单中，复制并保存 **[!UICONTROL Client ID]** 和 **[!UICONTROL Client Secret]** 的值 [!UICONTROL Adobe Inc Production API key] 到一个安全的地方。

     ![[!DNL Walmart Marketplace API key] 配置页面](assets/walmart-api-key-management-form.png){width="600" zoomable="yes"}

     >[!NOTE]
     >
     >如果 [!DNL Adobe Inc] 密钥未在开发人员门户中列出，请选择 **[!UICONTROL Add New Key for a Solution Provider]** 以配置权限并生成密钥。 有关配置详细信息，请参阅 [生成 [!DNL Walmart Marketplace API Key]](walmart-requirements.md#generate-a-walmart-marketplace-api-key).

   - 返回到 [!DNL Channel Manager] 将凭据添加到 **[!UICONTROL Walmart Connection]** 信息。

     添加凭据时，Adobe会隐藏客户端密码并将该值存储在安全保管库中。

1. 选择 **[!UICONTROL Save Store]** 以应用配置并连接到 [!DNL Walmart marketplace].

1. 成功连接后， [完成商店设置](complete-sales-channel-store-setup.md) 从 **[!UICONTROL Channel Manager]** 商店页面。

![设置第一个商店](assets/channel-manager-setup-first-store.png){width="500" zoomable="yes"}

### 连接问题疑难解答

如果与 [!DNL Walmart] 失败，请参见 [沃尔玛商城常见问题解答](https://developer.walmart.com/faq/us/faq-auth/){target="_blank"} 以获取疑难解答提示。

- 从 [!DNL Walmart Developer Portal]，确认您为的生产API密钥复制了正确的凭据 [!UICONTROL Adobe Inc.]

- 验证访问配置 [!UICONTROL Walmart Adobe API key] 具有正确的权限。 请参阅 [[!DNL Walmart Requirements]](walmart-requirements.md##generate-a-walmart-marketplace-api-key).

- 确认 [!DNL Walmart API] 服务可从以下位置获取： [Walmart API状态页面](https://developer.walmart.com/us/whats-new/new-api-status-information-now-available/){target="_blank"}.
