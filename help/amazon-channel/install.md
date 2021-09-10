---
title: 安装扩展
description: 要集成 [!DNL Commerce] catalog with [!DNL Amazon Seller Accounts] 并通过 [!DNL Amazon Marketplace]销售，请下载并安装AmazonSales Channel扩展。
exl-id: ebf22e28-b6a2-420b-80ca-2d750839286c
source-git-commit: 8d12a839bbdf77f27c732507b5b776729e252a9f
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---

# 安装扩展

>[!IMPORTANT]
>
>Adobe商务和Magento Open Source2.4.x版本仅支持[!DNL Amazon Sales Channel]扩展4.0及更高版本。 如果您运行的是2.3.x版本，请参阅[兼容的Amazon销售渠道版本](https://docs.magento.com/user-guide/v2.3/sales-channels/amazon/amazon-sales-channel.html){target=&quot;_blank&quot;}的文档。 有关版本兼容性的更多信息，请参阅开发人员文档中的[可用性](https://devdocs.magento.com/release/availability.html){target=&quot;_blank&quot;}页面。

[!UICONTROL Amazon Sales Channel]扩展安装并添加了一些功能，用于将您的Commerce目录与[!DNL Amazon Seller Accounts]集成，以通过[!DNL Amazon Marketplace]销售。 要查看其他信息，请参阅开发人员文档中的[!DNL Commerce Marketplace]中的[AmazonSales Channel](https://marketplace.magento.com/magento-module-amazon.html)页面和[发行说明](https://devdocs.magento.com/extensions/amazon-sales/release-notes/)。

## 要求

- **商务实例**:该扩 [!DNL Amazon Sales Channel] 展可以安装在云基础架构版本2.3.x或更高版本上包含Magento Open Source、Adobe商务和Adobe商务的实例上。2.1、2.2或1.x版本不再支持此功能。
- **商务Web帐户**:您应具有Commerce Web帐户，用于创建和跟踪API密钥。
- **API密钥**:通过您的Commerce Web帐户创建Amazon销售渠道API密钥。以下说明包括这些步骤。

## 安装

有关使用此过程使用编辑器的详细信息，请参阅开发人员文档中的[扩展安装](https://devdocs.magento.com/extensions/install/){target=&quot;_blank&quot;}说明。

1. 登录到[Commerce Marketplace](https://marketplace.magento.com/customer/account/){target=&quot;_blank&quot;}。

1. 单击&#x200B;**[!UICONTROL Marketplace]**&#x200B;选项卡，然后单击&#x200B;**[!UICONTROL My Purchases]**。

1. 找到并选择&#x200B;**[!UICONTROL Amazon Sales Channel]**。

1. 在扩展页面上，选择版本。

1. 对于组件名称和版本，单击&#x200B;**[!UICONTROL Technical Details]**。

1. 使用名称和版本信息更新`composer.json`文件中的服务连接器条目。

   - 将扩展的名称和版本添加到`composer.json`文件中。

   - 导航到[!DNL Commerce]项目目录并更新`composer.json`文件。

   ```bash
   composer require magento/services-connector:~1.0.3
   ```

   - 输入[身份验证密钥](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/connect-auth.html){target=&quot;_blank&quot;}。 您的公钥是您的用户名；您的私钥是您的密码。

   - 等待编辑器完成项目依赖项的更新，并确保没有错误。


1. [验证扩展](https://devdocs.magento.com/extensions/install/#verify-the-extension){target=&quot;_blank&quot;}。

## 添加Amazon销售渠道API密钥

安装后，输入[API密钥](./amazon-verify-api-key.md)以完成配置。

## 设置Amazon渠道配置选项

您可以使用以下选项来配置Amazon销售渠道。 您无需修改这些设置，即可开始在Amazon上投放和销售。 建议高级管理员考虑这些选项。

1. 登录管理员。

1. 在&#x200B;_Admin_&#x200B;侧栏中，转到&#x200B;**存储** > _设置_ > **配置**。

1. 单击&#x200B;**Sales Channel**，然后单击&#x200B;**全局设置**。

1. 对于&#x200B;**清除日志历史记录**，定义清除收集日志的间隔。

   选项包括`Once Daily`、`Once Weekly`和`Once Monthly`（默认）。

1. （可选）对于&#x200B;**后台任务(CRON)源**，将设置更改为`Command Line (CLI) CRON`。

   建议&#x200B;**_高级用户/管理员_**&#x200B;使用此设置。

1. 单击&#x200B;**[!UICONTROL Save Config]**。

## 更新扩展

1. 登录到[Commerce Marketplace](https://marketplace.magento.com/customer/account/){target=&quot;_blank&quot;}。

1. 单击&#x200B;**[!UICONTROL Marketplace]**&#x200B;选项卡，然后单击&#x200B;**[!UICONTROL My Purchases]**。

1. 找到并选择&#x200B;**[!UICONTROL Amazon Sales Channel]**。

1. 在扩展页面上，选择版本。

1. 对于组件名称和版本，单击&#x200B;**[!UICONTROL Technical Details]**。

1. 完成开发人员文档中的[扩展升级说明](https://devdocs.magento.com/extensions/install/#upgrade-an-extension){target=&quot;_blank&quot;}。
