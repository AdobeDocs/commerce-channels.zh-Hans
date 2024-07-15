---
title: '连接 [!DNL Channel Manager] 到 [!DNL Walmart Marketplace]'
description: “将Commerce商店视图连接到 [!DNL Walmart Marketplace] 以创建销售渠道，以管理Commerce产品列表、库存、价格和沃尔玛商店的订单。”
exl-id: 8c78c582-7b57-4f73-894e-134ba0ba3640
role: Admin, Developer
feature: Sales Channels, Install, Integration
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# 将[!DNL Channel Manager]连接到[!DNL Walmart Marketplace]

在您的[!DNL Commerce]实例上安装渠道管理器后，在渠道管理器中创建销售渠道并配置凭据以将[!DNL Channel Manager]连接到[!DNL Walmart Marketplace]。

1. [通过为产品列表选择[!DNL Commerce]商店来创建销售渠道](#create-the-sales-channel)。

1. [通过添加[!UICONTROL Walmart API credentials]](#connect-the-channel-to-walmart-marketplace)将该渠道连接到 [!DNL Walmart Marketplace] 。

1. [完成销售渠道设置](#complete-sales-channel-store-setup)以管理[!DNL Walmart Marketplace]产品分类的列表、库存、定价和订单。

>[!NOTE]
>
>渠道管理器要求在Walmart帐户和[!DNL Commerce]商店视图之间建立一对一连接。 不能将同一商店视图连接到多个Walmart帐户。

## 创建销售渠道

1. 从管理员中，选择&#x200B;**[!UICONTROL Marketing** > _渠道&#x200B;_> {渠道管理器]**以打开**0}。[!DNL Channel Manager]

1. 在&#x200B;**[!UICONTROL Marketplaces available to connect]**&#x200B;部分中，选择&#x200B;**[!UICONTROL Get Started]**。

   ![将新[!DNL Walmart]存储连接到[!DNL Channel Manager]](assets/channel-manager-home.png){width="700" zoomable="yes"}

1. 如果需要，请设置您的[!DNL Walmart Marketplace Seller]帐户。

1. 配置存储和连接：

   - 选择&#x200B;**[!UICONTROL Add Credentials]**。

   - 选择[!DNL Commerce]商店视图，该视图提供您要在Marketplace上销售的产品。

     ![从[!DNL Channel Manager]](assets/configure-commerce-to-marketplace-connection.png){width="500" zoomable="yes"}配置[!DNL Commerce]和[!DNL Walmart Marketplace]之间的连接

   - 输入唯一的&#x200B;**[!UICONTROL store name]**。

   - 为产品清单和订单处理选择&#x200B;**[!UICONTROL Adobe [!DNL Commerce] site]**。

   - 若要接收与[!DNL Channel Manager]相关的通知，请添加&#x200B;**[!UICONTROL email address]**。

1. 将渠道连接到[!DNL Walmart Marketplace]。

   - 从您的[!DNL Walmart Marketplace Seller]帐户添加[[!DNL Walmart Marketplace Adobe Production API key]](walmart-requirements.md#generate-a-walmart-marketplace-production-api-key)的凭据。

   - 如果您没有凭据，请选择&#x200B;**[!UICONTROL Get API credentials]**&#x200B;以从[!DNL Walmart Marketplace Developer Portal]中获取凭据。

     在开发人员门户上，选择您所在的地区（美国和加拿大），然后登录。

     ![[!DNL Walmart Marketplace]帐户登录](assets/walmart-marketplace-login-page.png){width="600"}

   - 在API密钥表单上，将[!UICONTROL Adobe Inc Production API key]的&#x200B;**[!UICONTROL Client ID]**&#x200B;和&#x200B;**[!UICONTROL Client Secret]**&#x200B;值复制并保存到安全位置。

     ![[!DNL Walmart Marketplace API key]配置页面](assets/walmart-api-key-management-form.png){width="600" zoomable="yes"}

     >[!NOTE]
     >
     >如果[!DNL Adobe Inc]密钥未在开发人员门户中列出，请选择&#x200B;**[!UICONTROL Add New Key for a Solution Provider]**&#x200B;以配置权限并生成密钥。 有关配置详细信息，请参阅[生成 [!DNL Walmart Marketplace API Key]](walmart-requirements.md#generate-a-walmart-marketplace-api-key)。

   - 返回到[!DNL Channel Manager]以将凭据添加到&#x200B;**[!UICONTROL Walmart Connection]**&#x200B;信息。

     添加凭据时，Adobe会隐藏客户端密码并将该值存储在安全保管库中。

1. 选择&#x200B;**[!UICONTROL Save Store]**&#x200B;以应用配置并连接到[!DNL Walmart marketplace]。

1. 成功连接后，从&#x200B;**[!UICONTROL Channel Manager]**&#x200B;商店页面[完成商店设置](complete-sales-channel-store-setup.md)。

![设置第一个存储](assets/channel-manager-setup-first-store.png){width="500" zoomable="yes"}

### 连接问题疑难解答

如果与[!DNL Walmart]的连接失败，请参阅[Walmart Marketplace常见问题解答](https://developer.walmart.com/faq/us/faq-auth/){target="_blank"}以获取疑难解答提示。

- 从[!DNL Walmart Developer Portal]中，验证您是否为[!UICONTROL Adobe Inc.]复制了生产API密钥的正确凭据

- 验证[!UICONTROL Walmart Adobe API key]的访问配置是否具有正确的权限。 请参阅[[!DNL Walmart Requirements]](walmart-requirements.md##generate-a-walmart-marketplace-api-key)。

- 从[Walmart API状态页](https://developer.walmart.com/us/whats-new/new-api-status-information-now-available/){target="_blank"}确认[!DNL Walmart API]服务可用。
