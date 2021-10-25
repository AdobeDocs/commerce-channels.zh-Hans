---
title: 添加或验证Amazon API密钥
description: 在您的商务配置中，已验证的Amazon API密钥允许您将商店与Amazon卖家帐户集成。
exl-id: 2257b64d-309d-4efd-ba79-6e0cdeed63cb
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 0%

---

# 添加或验证Amazon API密钥

访问Amazon销售渠道时， [!DNL Commerce] 自动检查并验证您在存储配置中添加的Amazon API密钥。 如果已验证，则可以继续执行下一步， [存储集成](./store-integration.md).

如果Amazon API密钥缺失、无效或过期，则必须更新密钥。 此时会显示一条消息，提示您获取API密钥并将其添加到Amazon销售渠道配置中。

## 根据提示获取并添加Amazon API密钥

每次访问Amazon销售渠道时，都会验证API密钥。

1. 登录 [!DNL Commerce] 管理员。

1. 在 _[!UICONTROL Admin]_侧栏，转到&#x200B;**[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**.

   如果您是首次访问Amazon销售渠道，或者如果您的API密钥需要更新，系统会提示您完成该过程。

   ![获取并添加Amazon API密钥提示](assets/amazon-api-verification-prompt.png)

1. 单击 **[!UICONTROL Sign in]** 访问 [!DNL Commerce] Web帐户。

   在新的浏览器选项卡中打开“商务帐户”页面。

   - 如果您已登录 [!DNL Commerce] 帐户， _[!UICONTROL API Portal]_部分_[!UICONTROL My Account]_ 页面时，会自动显示该页面。

   - 如果您未登录，系统会提示您输入 [!DNL Commerce] 帐户用户名和密码 _[!UICONTROL API Portal]_选项卡。

   - 如果您没有帐户，请访问 [the [!DNL Commerce] 帐户页面](https://account.magento.com/customer/account/login/){target=&quot;_blank&quot;}并注册。 此帐户应属于您的公司或业务。

1. 如果需要，您可以在 _[!UICONTROL API Portal]_选项卡 [!DNL Commerce] 帐户。

   要创建API密钥，请输入描述，如 `Amazon Sales Channel` 单击 **[!UICONTROL Add New]**. 将生成新键，并显示您输入的名称。 单击 **[!UICONTROL Copy]** 以复制新密钥。

   ![生成或复制API密钥](assets/amazon-add-api-key.png)

1. 生成并复制新密钥后，返回到 _[!UICONTROL Amazon Sales Channel]_选项卡。

1. 在 _[!UICONTROL Welcome to Amazon Sales Channel]_页面，单击&#x200B;**[!UICONTROL Add the key]**.

   浏览器退出Amazon销售渠道，并打开商店配置页面 _[!UICONTROL Api Keys]_页面 [!DNL Commerce] 管理员。 您可以在转到&#x200B;**[!UICONTROL Stores]**>_[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**，展开 **[!UICONTROL Services]** ，然后选择 **[!UICONTROL Magento Services]**.

1. 粘贴复制的键 **[!UICONTROL Production Api key]**.

1. 单击 **[!UICONTROL Save Config]**. 您现在可以返回Amazon销售渠道。

   ![在存储配置中添加API密钥](assets/config-magento-services-api-screen.png)

1. 在 _[!UICONTROL Admin]_侧栏，转到&#x200B;**[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**.

   重新访问Amazon销售渠道触发器 [!DNL Commerce] 验证和验证您的API密钥，并允许您继续。

   如果系统提示您再次验证密钥，请重复此步骤 _添加和验证_ 进程。

![下一个图标](assets/btn-next.png) [**继续存储集成**](./store-integration.md)
