---
title: 存储与 [!DNL Amazon Seller Account]的集成
description: 在开始载入流程之前，您必须创建（添加）一个AmazonSales Channel商店，并将其连接到您的Amazon卖方帐户。
role: Admin, Developer
feature: Sales Channels, Configuration, Integration, Tools and External Services
exl-id: ea79e91d-7d92-4992-a921-7ac7632a0519
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 0%

---

# 存储与[!DNL Amazon Seller Account]的集成

要开始使用Amazon sales channel，您必须创建（添加）一个Amazon sales channel应用商店并将其连接到您的[!DNL Amazon Seller Account]。 这两个步骤集成了您的[!DNL Commerce]和Amazon帐户以共享数据、同步产品等。

_您需要您的[!DNL Amazon Seller Central]帐户（用于创建卖方帐户的电子邮件或电话）的主要登录凭据才能连接您的商店。_

>[!NOTE]
>
>在首次整合商店后，您将每年通过再次授予访问权限来提示您续订与Amazon的Amazon销售渠道连接。 您可以在Seller Central帐户的&#x200B;**设置** > **用户权限**&#x200B;页面的&#x200B;_Amazon MWS开发人员权限_&#x200B;部分的&#x200B;_当前授权_&#x200B;表中续订或撤消此授权。

## 添加Amazon store

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**营销** > _渠道_ > **AmazonSales Channel**。

   添加您的第一个Amazon Sales Channel商店时，出现&#x200B;_预安装任务_&#x200B;模式。 添加第一个商店后，可在左侧菜单的&#x200B;_学习与准备_&#x200B;下的[Amazon销售渠道主页](./amazon-sales-channel-home.md)页面上访问预设置任务。

1. 单击&#x200B;**[!UICONTROL Add Amazon Store]**。

   将打开&#x200B;_[!UICONTROL Add Amazon sales channel]_页面。

   ![添加Amazon sales channel store](assets/amazon-store-integration.png){width="500" zoomable="yes"}

1. 对于&#x200B;**[!UICONTROL Magento Website to use for Amazon Listing]**，选择要为此Amazon销售渠道商店连接的[!DNL Commerce]网站。

   此设置还为[导入Amazon订单](./order-settings.md)定义了默认[!DNL Commerce]存储。

1. 对于&#x200B;**[!UICONTROL Email Address]**，输入首选联系人电子邮件地址。

1. 对于&#x200B;**[!UICONTROL New Store Name]**，为您的新Amazon销售渠道商店输入一个描述性名称。

   >[!NOTE]
   >
   >此名称仅用作[!DNL Commerce]引用，并在[Amazon销售渠道主页](./amazon-sales-channel-home.md)页面上标识该商店。 您希望让您的团队能够轻松识别它。 例如，您在美国地区销售的Amazon商店可能名为`Amazon Store USA`。

1. 对于&#x200B;**[!UICONTROL Amazon Marketplace Country]**，选择此Amazon销售渠道商店销售产品的国家/地区。 选项：

   - 美国
   - 加拿大
   - 墨西哥
   - 英国

1. 在&#x200B;_[!UICONTROL Map your Magento attributes to Amazon]_部分中，执行以下操作：

   - 对于&#x200B;**[!UICONTROL Product ID on the Amazon market]**，选择要映射到下面选定的[!DNL Commerce]属性的Amazon属性。

     此ID有助于正确匹配[!DNL Commerce]目录中的相应产品。

   - 对于&#x200B;**[!UICONTROL Map a Magento attribute]**，选择要映射到上面所选Amazon属性的[!DNL Commerce]产品属性。

     [映射属性](./ob-creating-magento-attributes.md)有助于确保您的Amazon列表与[!DNL Commerce]目录中的相应产品正确匹配。

1. 单击&#x200B;**[!UICONTROL Connect]**。

   对话框关闭，新商店出现在[Amazon销售渠道主页](./amazon-sales-channel-home.md)页面上，并显示一条确认消息。

## 将存储连接到[!DNL Amazon Seller Central]

1. 在商店仪表板上，单击商店信息卡上的&#x200B;**[!UICONTROL Connect store]**&#x200B;以在新选项卡中启动[!DNL Amazon Seller Central]。

1. 输入您的[!DNL Amazon Seller Central]帐户凭据，然后单击&#x200B;**[!UICONTROL Sign in]**。

   要完成此连接，必须使用主要用户的登录凭据（用于创建卖方帐户的电子邮件或电话）登录到[!DNL Amazon Seller Central]帐户。

1. 如果出现提示，请输入您从Amazon收到的代码并单击&#x200B;**[!UICONTROL Sign in]**&#x200B;以完成Amazon双重授权(2FA)。

1. 在&#x200B;_[!UICONTROL Amazon Marketplace Web Service]_确认页面上，选中“[!UICONTROL I understand...]”复选框，然后单击&#x200B;**[!UICONTROL Next]**。

1. 在&#x200B;_[!UICONTROL You are almost done]_消息上，单击&#x200B;**[!UICONTROL Continue]**。

   您已授予Amazon销售渠道权限来访问数据并与您的[!DNL Amazon Seller Central]帐户共享数据。 Amazon页面将关闭，并显示一条确认消息。

   此时将打开[Amazon销售渠道主页](./amazon-sales-channel-home.md)页面，其中显示您的Amazon商店信息卡。

   要查看商店信息板，请单击商店信息卡上的&#x200B;**[!UICONTROL View Store]**。

![Amazon销售渠道主页，带有新商店卡](assets/asc-dashboard-after-2fa.png){width="600" zoomable="yes"}

您新的Amazon销售渠道商店现已连接到您的[!DNL Amazon Seller Central]帐户。

![下一个图标](assets/btn-next.png) [**继续创建列表规则**](./ob-create-listing-rule.md)
