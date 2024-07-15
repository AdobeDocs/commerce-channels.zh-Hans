---
title: '连接到 [!DNL Commerce] 服务'
description: '将渠道管理器连接到 [!DNL Commerce] 服务，以启用 [!DNL Commerce] 实例、渠道管理器和其他支持服务之间的数据同步和通信。'
role: Admin, Developer
level: Intermediate
feature: Sales Channels, Install, Integration
exl-id: 97da2142-ecef-44dc-91d8-5dc55c713d31
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---


# 连接到[!DNL Commerce]服务

[!DNL Commerce Services Connector]将渠道管理器服务与Adobe Commerce和Magento Open Source实例集成。 连接器启用[!DNL Commerce]实例[!DNL Channel Manager]与其他支持服务之间的数据同步和通信。

[!DNL Commerce Services Connector]安装程序是使用[Adobe Commerce SaaS服务](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html)（如[!DNL Channel Manager]、[!DNL Live Search]和[!DNL Product Recommendations]）所需的一次性进程。 如果已为其他服务配置了连接器，请跳过此步骤。

## 要求

- **Commerce帐户** — 若要在[!DNL Commerce]实例上安装软件，您必须拥有对[!DNL Commerce]平台具有所有者或管理员访问权限的帐户。

  帐户所有者和超级用户可以使用[!DNL Commerce] CLI命令`admin:user:create`从[!DNL Commerce]实例或命令行创建管理员帐户。

- **Adobe Commerce生产API密钥** — 此[密钥](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html#genapikey)允许API访问渠道管理器所需的服务。 您需要此密钥的公共和私有凭据。

>[!TIP]
>
>若要提供凭据，[!DNL Commerce]许可证持有人或帐户所有者可以选择将[共享访问](https://experienceleague.adobe.com/docs/commerce-admin/start/commerce-account/commerce-account-share.html)，或将[API密钥](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html)凭据提供给受信任的开发人员。

## 配置[!DNL Commerce Services Connector]

1. 打开存储服务配置。

   - 从管理员中，选择&#x200B;**[!UICONTROL Stores]**。

   - 在&#x200B;*[!UICONTROL Settings]*&#x200B;下，选择&#x200B;**[!UICONTROL Configuration]**。

   - 展开&#x200B;**[!UICONTROL Services]**&#x200B;并选择&#x200B;**[!UICONTROL Commerce Services Connector]**。

1. 从您的Adobe Commerce帐户添加生产API密钥凭据。

   [!DNL Admin]视图中的![[!DNL Commerce Services Connector]服务](assets/commerce-services-connector-admin-service-view.png){width="600" zoomable="yes"}


   >[!NOTE]
   >
   > 如果您的[!DNL Commerce]实例已安装其他[!DNL Adobe Commerce]服务（如[!DNL Live Search]或[!DNL Product Recommendations]），则凭据信息将显示在界面中，无需进一步配置。

1. 配置SaaS项目和数据空间，以便Commerce服务能够将数据发送到渠道管理器服务。

   [!DNL Admin]视图](assets/commerce-services-connector-saas-config.png){width="600" zoomable="yes"}中的![[!DNL Commerce Services Connector] SaaS标识符配置

