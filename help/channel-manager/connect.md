---
title: 连接到Commerce Services
description: 将渠道管理器实例连接到 [!DNL Commerce services] 启用商务实例、渠道管理器和其他支持服务之间的数据同步和通信。
role: User
level: Intermediate
source-git-commit: ec950579a9b2220f9ec106b616779fc3503f3add
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 0%

---

# 连接到Commerce Services

Commerce Services Connector将Channel Manager服务与Adobe Commerce和Magento Open Source实例集成。 该连接器实现数据同步和在 [!DNL Commerce] 实例， [!DNL Channel Manager]，以及其他支持服务。

Commerce Services Connector设置是使用Adobe所需的一次性流程 [商务SaaS服务](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html)类似于{target=&quot;_blank&quot;} [!DNL Channel Manager], [!DNL Live Search]和 [!DNL Product Recommendations]. 如果已经为其他服务配置了连接器，则可以跳过此步骤。

## 先决条件

- **商务帐户 [管理员访问权限](https://docs.magento.com/user-guide/stores/admin.html){target=&quot;_blank&quot;}** 至您的商务实例** — 帐户所有者和管理员用户可以通过商务实例或命令行使用 [!DNL Commerce] CLI命令 `admin:user:create`.

- **Adobe Commerce [生产API密钥](https://docs.magento.com/user-guide/system/saas.html#apikey){target=&quot;_blank&quot;}** — 启用对渠道管理器所需服务的API访问

   要提供凭据，商务许可证持有者或帐户所有者可以选择
   [共享访问](https://docs.magento.com/user-guide/magento/magento-account-share.html){target=&quot;_blank&quot;}，或为 [API密钥](https://docs.magento.com/user-guide/system/saas.html#apikey){target=&quot;_blank&quot;}个凭据发送给受信任的开发人员。

## 配置Commerce Services连接器

1. 打开存储服务配置。

   - 在管理员中，选择 [!UICONTROL Stores].

   - 在 *设置*，选择 [!UICONTROL Configuration].

   - 在 [!UICONTROL Configuration] 页面，展开 [!UICONTROL Services] 选择 [!UICONTROL Commerce Services Connector].

1. 从您的Adobe Commerce帐户添加生产API密钥。

   ![[!DNL Commerce Service Connector] 服务 [!DNL Admin] 视图](assets/commerce-services-connector-admin-service-view.png)


   >[!NOTE]
   >
   > 如果 [!DNL Commerce] 实例具有其他 [!DNL Adobe Commerce] 服务类似 [!DNL Live Search] 或 [!DNL Product Recommendations] 安装后，界面中会显示凭据信息，无需进一步配置。

1. 配置SaaS项目和数据空间，以便Commerce Services可以将数据发送到Channel Manager服务。

   ![[!DNL Commerce Service Connector] SaaS标识符配置 [!DNL Admin] 视图](assets/commerce-services-connector-saas-config.png)

