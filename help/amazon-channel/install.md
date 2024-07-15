---
title: 安装 [!DNL Amazon Sales Channel] 扩展
description: 要将 [!DNL Commerce] 目录与 [!DNL Amazon Seller Accounts] 集成并通过 [!DNL Amazon Marketplace]销售，请下载并安装AmazonSales Channel扩展。
role: Admin, Developer
feature: Sales Channels, Install, Integration, Tools and External Services
exl-id: ebf22e28-b6a2-420b-80ca-2d750839286c
source-git-commit: 010a95d7be29354515cf4dcbf5d557eebaa40ed6
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 0%

---

# 安装[!DNL Amazon Sales Channel]扩展

>[!IMPORTANT]
>
>Adobe Commerce和Magento Open Source 2.4.x版本仅支持[!DNL Amazon Sales Channel]扩展4.0+版本。 如果您运行的是2.3.x版本，请参阅有关[兼容的Amazon sales channel版本](https://docs.magento.com/user-guide/v2.3/sales-channels/amazon/amazon-sales-channel.html)的文档。 有关版本兼容性的详细信息，请参阅开发人员文档中的[可用性](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html)页面。

[!UICONTROL Amazon Sales Channel]扩展将安装并添加功能，以将您的Commerce目录与[!DNL Amazon Seller Accounts]集成以通过[!DNL Amazon Marketplace]销售。 若要查看其他信息，请参阅[!DNL Commerce Marketplace]中的[AmazonSales Channel](https://marketplace.magento.com/magento-module-amazon.html)页面和[发行说明](release-notes.md)。

## 要求

- **Commerce实例**： [!DNL Amazon Sales Channel]扩展可以安装在云基础架构版本2.3.x或更高版本上具有Magento Open Source、Adobe Commerce和Adobe Commerce的实例上。 2.1、2.2或1.x版本不再支持此功能。
- **Commerce Web帐户**：您应该拥有Commerce Web帐户，该帐户用于创建和跟踪API密钥。
- **API密钥**：通过您的Amazon Web帐户创建Commerce销售渠道API密钥。 以下说明包括这些步骤。

## 安装

有关在此过程中使用Composer的更多详细信息，请参阅开发人员文档中的[扩展安装](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html)说明。

1. 登录到[Commerce Marketplace](https://marketplace.magento.com/customer/account/)。

1. 单击&#x200B;**[!UICONTROL Marketplace]**&#x200B;选项卡，然后单击&#x200B;**[!UICONTROL My Purchases]**。

1. 找到并选择&#x200B;**[!UICONTROL Amazon Sales Channel]**。

1. 在扩展页面上，选择版本。

1. 对于组件名称和版本，单击&#x200B;**[!UICONTROL Technical Details]**。

1. 使用名称和版本信息更新`composer.json`文件中的服务连接器条目。

   - 将扩展名和版本添加到您的`composer.json`文件。

   - 导航到[!DNL Commerce]项目目录并更新`composer.json`文件。

   ```bash
   composer require magento/services-connector:~1.0.3
   ```

   - 输入您的[身份验证密钥](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html)。 您的公钥是您的用户名；您的私钥是您的密码。

   - 等待Composer完成项目依赖项的更新并确保没有错误。

1. [验证扩展](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html)。

## 添加Amazon sales channel API密钥

安装后，输入[API密钥](./amazon-verify-api-key.md)以完成配置。

## 设置Amazon渠道配置选项

您可以使用以下选项配置Amazon销售渠道。 您无需修改这些设置，即可开始在Amazon上进行载入和销售。 建议高级管理员考虑这些选项。

1. 登录管理员。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**商店** > _设置_ > **配置**。

1. 单击&#x200B;**Sales Channel**，然后单击&#x200B;**全局设置**。

1. 对于&#x200B;**清除日志历史记录**，定义清除收集日志的间隔。

   选项包括`Once Daily`、`Once Weekly`和`Once Monthly`（默认）。

1. （可选）对于&#x200B;**后台任务(CRON) Source**，将设置更改为`Command Line (CLI) CRON`。

   建议对&#x200B;**_高级用户/管理员_**&#x200B;使用此设置。

1. 单击&#x200B;**[!UICONTROL Save Config]**。

## 更新扩展

1. 登录到[Commerce Marketplace](https://marketplace.magento.com/customer/account/)。

1. 单击&#x200B;**[!UICONTROL Marketplace]**&#x200B;选项卡，然后单击&#x200B;**[!UICONTROL My Purchases]**。

1. 找到并选择&#x200B;**[!UICONTROL Amazon Sales Channel]**。

1. 在扩展页面上，选择版本。

1. 对于组件名称和版本，单击&#x200B;**[!UICONTROL Technical Details]**。

1. 完成&#x200B;_安装指南_&#x200B;中的[扩展升级说明](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html)。
