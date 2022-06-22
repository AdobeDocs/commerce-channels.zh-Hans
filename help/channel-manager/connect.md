---
title: 连接到 [!DNL Commerce] 服务'
description: 将渠道管理器连接到 [!DNL Commerce] 服务，以实现数据同步和在 [!DNL Commerce] 实例、渠道管理器和其他支持服务。
role: User
level: Intermediate
exl-id: 97da2142-ecef-44dc-91d8-5dc55c713d31
source-git-commit: 7e7a3e854bbc6062e2d15c1962ddf787451e7275
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---


# 连接到 [!DNL Commerce] 服务

的 [!DNL Commerce Services Connector] 将渠道管理器服务与Adobe Commerce和Magento Open Source实例集成。 该连接器实现数据同步和在 [!DNL Commerce] 实例， [!DNL Channel Manager]，以及其他支持服务。

[!DNL Commerce Services Connector] 设置是使用的一次性流程 [Adobe Commerce SaaS服务](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html){target=&quot;_blank&quot;}，如 [!DNL Channel Manager], [!DNL Live Search]和 [!DNL Product Recommendations]. 如果已为其他服务配置连接器，请跳过此步骤。

## 要求

- **商务帐户** — 在上安装软件 [!DNL Commerce] 实例时，您必须拥有对 [!DNL Commerce] 平台。

   帐户所有者和超级用户可以通过 [!DNL Commerce] 实例或从命令行中使用 [!DNL Commerce] CLI命令 `admin:user:create`.

- **Adobe Commerce生产API密钥** — 此 [key](https://docs.magento.com/user-guide/system/saas.html#apikey){target=&quot;_blank&quot;}允许API访问渠道管理器所需的服务。 您需要此密钥的公共和私有凭据。

>[!TIP]
>
>要提供凭据，请 [!DNL Commerce] 许可证持有者或帐户拥有者有权选择 [共享访问](https://docs.magento.com/user-guide/magento/magento-account-share.html){target=&quot;_blank&quot;}，或为 [API密钥](https://docs.magento.com/user-guide/system/saas.html#apikey){target=&quot;_blank&quot;}个凭据发送给受信任的开发人员。

## 配置 [!DNL Commerce Services Connector]

1. 打开存储服务配置。

   - 在管理员中，选择 **[!UICONTROL Stores]**.

   - 在 *[!UICONTROL Settings]*，选择 **[!UICONTROL Configuration]**.

   - 展开 **[!UICONTROL Services]** 选择 **[!UICONTROL Commerce Services Connector]**.

1. 从您的Adobe Commerce帐户添加生产API密钥凭据。

   ![[!DNL Commerce Services Connector] 服务 [!DNL Admin] 视图](assets/commerce-services-connector-admin-service-view.png)


   >[!NOTE]
   >
   > 如果 [!DNL Commerce] 实例具有其他 [!DNL Adobe Commerce] 服务类似 [!DNL Live Search] 或 [!DNL Product Recommendations] 安装后，界面中会显示凭据信息，无需进一步配置。

1. 配置SaaS项目和数据空间，以便Commerce Services可以将数据发送到Channel Manager服务。

   ![[!DNL Commerce Services Connector] SaaS标识符配置 [!DNL Admin] 视图](assets/commerce-services-connector-saas-config.png)

