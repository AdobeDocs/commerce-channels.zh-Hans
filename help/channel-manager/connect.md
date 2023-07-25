---
title: '''连接到 [!DNL Commerce] 服务'
description: '''将渠道管理器连接到 [!DNL Commerce] 服务以启用数据同步和 [!DNL Commerce] 实例、渠道经理和其他支持服务。”'
role: Admin, Developer
level: Intermediate
feature: Sales Channels, Install, Integration
exl-id: 97da2142-ecef-44dc-91d8-5dc55c713d31
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 0%

---


# 连接到 [!DNL Commerce] 服务

此 [!DNL Commerce Services Connector] 将Channel Manager服务与Adobe Commerce和Magento Open Source实例集成。 该连接器实现了数据同步和以下对象之间的通信： [!DNL Commerce] 实例， [!DNL Channel Manager]和其他支持服务。

[!DNL Commerce Services Connector] 设置需要一次性使用 [Adobe Commerce SaaS服务](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html) 例如 [!DNL Channel Manager]， [!DNL Live Search]、和 [!DNL Product Recommendations]. 如果已为其他服务配置了连接器，请跳过此步骤。

## 要求

- **Commerce帐户** — 安装软件 [!DNL Commerce] 实例中，您必须拥有对具有访问权限的所有者或管理员的帐户 [!DNL Commerce] 平台。

  帐户所有者和超级用户可以从中创建管理员帐户 [!DNL Commerce] 实例或从命令行中使用 [!DNL Commerce] CLI命令 `admin:user:create`.

- **Adobe Commerce生产API密钥**-This [键](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html#genapikey) 允许通过API访问渠道管理器所需的服务。 您需要此密钥的公共和专用凭据。

>[!TIP]
>
>要提供凭据，请 [!DNL Commerce] 许可证持有人或帐户所有者可以选择 [共享访问](https://experienceleague.adobe.com/docs/commerce-admin/start/commerce-account/commerce-account-share.html)，或给出 [API密钥](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html) 凭据发送给受信任的开发人员。

## 配置 [!DNL Commerce Services Connector]

1. 打开存储服务配置。

   - 在管理员中，选择 **[!UICONTROL Stores]**.

   - 下 *[!UICONTROL Settings]*，选择 **[!UICONTROL Configuration]**.

   - 展开 **[!UICONTROL Services]** 并选择 **[!UICONTROL Commerce Services Connector]**.

1. 从您的Adobe Commerce帐户添加生产API密钥凭据。

   ![[!DNL Commerce Services Connector] 中的服务 [!DNL Admin] 视图](assets/commerce-services-connector-admin-service-view.png){width="600" zoomable="yes"}


   >[!NOTE]
   >
   > 如果您的 [!DNL Commerce] 实例具有其他 [!DNL Adobe Commerce] 服务如 [!DNL Live Search] 或 [!DNL Product Recommendations] 安装，界面中会显示凭据信息，无需进一步配置。

1. 配置SaaS项目和数据空间，以便Commerce Services能够向渠道管理器服务发送数据。

   ![[!DNL Commerce Services Connector] 中的SaaS标识符配置 [!DNL Admin] 视图](assets/commerce-services-connector-saas-config.png){width="600" zoomable="yes"}

