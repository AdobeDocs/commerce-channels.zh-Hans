---
title: 添加或验证Amazon API密钥
description: 在您的Commerce配置中，通过验证的Amazon API密钥可将您的商店与Amazon卖方帐户集成。
role: Admin, Developer
feature: Sales Channels, Integration, Tools and External Services
exl-id: 2257b64d-309d-4efd-ba79-6e0cdeed63cb
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 0%

---

# 添加或验证Amazon API密钥

访问Amazon销售渠道时，[!DNL Commerce]会自动检查并验证您在商店配置中添加的Amazon API密钥。 如果已验证，则可以继续下一步操作，[存储集成](./store-integration.md)。

如果Amazon API密钥缺失、无效或过期，您必须更新密钥。 系统会显示一条消息，提示您获取API密钥并将其添加到您的Amazon销售渠道配置中。

## 根据提示获取并添加Amazon API密钥

每次访问Amazon销售渠道时，系统都会验证API密钥。

1. 登录到[!DNL Commerce]管理员。

1. 在&#x200B;_[!UICONTROL Admin]_侧边栏上，转到&#x200B;**[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**。

   如果您是首次访问Amazon销售渠道，或者API密钥需要更新，系统将会提示您完成该过程。

   ![获取并添加Amazon API密钥提示](assets/amazon-api-verification-prompt.png){width="500"}

1. 单击&#x200B;**[!UICONTROL Sign in]**&#x200B;以访问您的[!DNL Commerce] Web帐户。

   Commerce帐户页面将在新的浏览器选项卡中打开。

   - 如果您已登录到您的[!DNL Commerce]帐户，_[!UICONTROL My Account]_页面的_[!UICONTROL API Portal]_&#x200B;部分会自动显示。

   - 如果您未登录，则系统会提示您输入[!DNL Commerce]帐户用户名和密码，然后才会显示&#x200B;_[!UICONTROL API Portal]_选项卡。

   - 如果您没有帐户，请访问[ [!DNL Commerce] 帐户页](https://account.magento.com/customer/account/login/){target="_blank"}并注册。 此帐户应该是您公司或业务的一部分。

1. 如果需要，您可以在帐户[!DNL Commerce]的&#x200B;_[!UICONTROL API Portal]_选项卡上查看和生成API密钥。

   要创建API密钥，请输入诸如`Amazon Sales Channel`之类的描述，然后单击&#x200B;**[!UICONTROL Add New]**。 将生成新的密钥，并显示您输入的名称。 单击&#x200B;**[!UICONTROL Copy]**&#x200B;以复制新密钥。

   ![生成或复制API密钥](assets/amazon-add-api-key.png){width="500" zoomable="yes"}

1. 生成并复制新密钥后，返回到浏览器中的&#x200B;_[!UICONTROL Amazon Sales Channel]_选项卡。

1. 在&#x200B;_[!UICONTROL Welcome to Amazon Sales Channel]_页面上，单击&#x200B;**[!UICONTROL Add the key]**。

   浏览器退出Amazon销售渠道，商店配置页面在[!DNL Commerce]管理员中打开&#x200B;_[!UICONTROL Api Keys]_页面。 当您转到&#x200B;**[!UICONTROL Stores]**>_[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**，展开左侧面板中的&#x200B;**[!UICONTROL Services]**，然后选择&#x200B;**[!UICONTROL Magento Services]**&#x200B;时，可以手动打开此页面。

1. 粘贴&#x200B;**[!UICONTROL Production Api key]**&#x200B;的复制密钥。

1. 单击&#x200B;**[!UICONTROL Save Config]**。 您现在可以返回到Amazon销售渠道。

   ![在商店配置中添加API密钥](assets/config-magento-services-api-screen.png){width="600" zoomable="yes"}

1. 在&#x200B;_[!UICONTROL Admin]_侧边栏上，转到&#x200B;**[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**。

   重新访问Amazon sales channel触发器[!DNL Commerce]验证并验证您的API密钥，并允许您继续。

   如果系统提示您再次验证密钥，请重复此&#x200B;_添加并验证_&#x200B;过程。

![下一个图标](assets/btn-next.png) [**继续存储集成**](./store-integration.md)
