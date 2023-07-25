---
title: 存储与的集成 [!DNL Amazon Seller Account]
description: 在开始载入流程之前，您必须创建（添加）一个AmazonSales Channel商店，并将其连接到您的Amazon卖方帐户。
role: Admin, Developer
feature: Sales Channels, Configuration, Integration, Tools and External Services
exl-id: ea79e91d-7d92-4992-a921-7ac7632a0519
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 0%

---

# 存储与的集成 [!DNL Amazon Seller Account]

要开始使用Amazon sales channel，您必须创建（添加） Amazon sales channel store并将其连接到您的 [!DNL Amazon Seller Account]. 这两个步骤集成了您的 [!DNL Commerce] 和Amazon帐户共享数据、同步产品等。

_您需要的主要登录凭据用于 [!DNL Amazon Seller Central] 帐户（用于创建卖方帐户的电子邮件或电话）以连接您的商店。_

>[!NOTE]
>
>在首次进行商店集成后，系统每年会提示您通过再次授予访问权限来续订Amazon销售渠道与Amazon的连接。 您可以在以下位置续订或撤消此授权： _当前授权_ 中的表 _Amazon MWS开发人员权限_ 部分 **设置** > **用户权限** “销售中心”帐户的页面。

## 添加Amazon商店

1. 在 _管理员_ 侧栏，转到 **营销** > _渠道_ > **AmazonSales Channel**.

   添加您的第一个Amazon sales channel商店时， _预设置任务_ 此时将显示模式窗口。 添加第一个商店后，可在 [Amazon sales channel home](./amazon-sales-channel-home.md) 页面位于 _学习和准备_ 左侧菜单中的。

1. 单击 **[!UICONTROL Add Amazon Store]**.

   此 _[!UICONTROL Add Amazon sales channel]_页面打开。

   ![添加Amazon sales channel store](assets/amazon-store-integration.png){width="500" zoomable="yes"}

1. 对象 **[!UICONTROL Magento Website to use for Amazon Listing]**，选择您的 [!DNL Commerce] 要为此Amazon sales channel商店连接的网站。

   此设置还定义默认值 [!DNL Commerce] 存储对象 [导入Amazon订单](./order-settings.md).

1. 对象 **[!UICONTROL Email Address]**，输入首选联系人的电子邮件地址。

1. 对象 **[!UICONTROL New Store Name]**，为您的新Amazon sales channel store输入一个描述性名称。

   >[!NOTE]
   >
   >此名称用作 [!DNL Commerce] 仅引用并标识上的商店 [Amazon sales channel home](./amazon-sales-channel-home.md) 页面。 您希望让您的团队能够轻松识别它。 例如，您在美国地区销售的Amazon商店可能会被命名为 `Amazon Store USA`.

1. 对象 **[!UICONTROL Amazon Marketplace Country]**，选择此Amazon销售渠道商店销售产品的区域/国家/地区。 选项：

   - 美国
   - 加拿大
   - 墨西哥
   - 英国

1. 在 _[!UICONTROL Map your Magento attributes to Amazon]_部分，请执行以下操作：

   - 对象 **[!UICONTROL Product ID on the Amazon market]**&#x200B;中，选择要映射到的Amazon属性 [!DNL Commerce] 属性处于选中状态。

     此ID有助于正确匹配中的相应产品 [!DNL Commerce] 目录。

   - 对象 **[!UICONTROL Map a Magento attribute]**，选择 [!DNL Commerce] 产品属性，以映射到上面选择的Amazon属性。

     [映射属性](./ob-creating-magento-attributes.md) 有助于确保列出的Amazon与中的相应产品正确匹配。 [!DNL Commerce] 目录。

1. 单击 **[!UICONTROL Connect]**.

   对话框关闭，新存储出现在 [Amazon sales channel home](./amazon-sales-channel-home.md) 页包含确认消息。

## 将商店连接到 [!DNL Amazon Seller Central]

1. 在商店功能板上，单击 **[!UICONTROL Connect store]** 在要启动的存储卡上 [!DNL Amazon Seller Central] 在新选项卡中。

1. 输入您的 [!DNL Amazon Seller Central] 帐户凭据，然后单击 **[!UICONTROL Sign in]**.

   要完成此连接，您必须登录到 [!DNL Amazon Seller Central] 使用主要用户的登录凭据的帐户（用于创建卖方帐户的电子邮件或电话）。

1. 如果出现提示，请输入您从Amazon收到的代码并单击，以完成Amazon双重授权(2FA) **[!UICONTROL Sign in]**.

1. 在 _[!UICONTROL Amazon Marketplace Web Service]_确认页面，选择“[!UICONTROL I understand...]”复选框，然后单击&#x200B;**[!UICONTROL Next]**.

1. 在 _[!UICONTROL You are almost done]_消息，请单击&#x200B;**[!UICONTROL Continue]**.

   您已授予Amazon销售渠道访问数据并与您共享数据的权限 [!DNL Amazon Seller Central] 帐户。 Amazon页面将关闭，并显示一条确认消息。

   此 [Amazon sales channel home](./amazon-sales-channel-home.md) 页面打开，其中显示您的Amazon商店信息卡。

   要查看商店功能板，请单击 **[!UICONTROL View Store]** 在商店卡上。

![带有新商店卡的Amazon sales channel home](assets/asc-dashboard-after-2fa.png){width="600" zoomable="yes"}

您的新Amazon销售渠道商店现已连接到您的 [!DNL Amazon Seller Central] 帐户。

![“下一步”图标](assets/btn-next.png) [**继续创建列表规则**](./ob-create-listing-rule.md)
