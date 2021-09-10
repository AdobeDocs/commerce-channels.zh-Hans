---
title: 存储集成
description: 在开始载入流程之前，您必须创建（添加）AmazonSales Channel商店，并将其连接到您的Amazon卖家帐户。
exl-id: ea79e91d-7d92-4992-a921-7ac7632a0519
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 0%

---

# 存储集成

要开始使用Amazon销售渠道，您必须创建（添加）Amazon销售渠道商店，并将其连接到您的Amazon卖家帐户。 这两个步骤将集成[!DNL Commerce]和Amazon帐户以共享数据、同步产品等。

_您需要帐户的主要登录凭据( [!DNL Amazon Seller Central] 用于创建卖家帐户的电子邮件或电话)来连接您的商店。_

>[!NOTE]
>
>首次集成商店后，系统将每年通过再次授予访问权限，提示您续订与Amazon的Amazon销售渠道连接。 您可以在销售中心帐户的&#x200B;**Settings** > **User Permissions**&#x200B;页面的&#x200B;_Amazon MWS开发人员权限_&#x200B;部分的&#x200B;_当前授权_&#x200B;表中续订或撤消此授权。

## 添加Amazon商店

1. 在&#x200B;_Admin_&#x200B;侧栏中，转到&#x200B;**Marketing** > _渠道_ > **AmazonSales Channel**。

   添加您的第一个Amazon销售渠道商店时，将显示&#x200B;_预设置任务_&#x200B;模式。 添加第一个商店后，可在左侧菜单&#x200B;_学习和准备_&#x200B;下的[Amazon销售渠道主页](./amazon-sales-channel-home.md)页面上访问预设设置任务。

1. 单击&#x200B;**[!UICONTROL Add Amazon Store]**。

   将打开&#x200B;_[!UICONTROL Add Amazon sales channel]_页面。

   ![添加Amazon销售渠道商店](assets/amazon-store-integration.png)

1. 对于&#x200B;**[!UICONTROL Magento Website to use for Amazon Listing]**，选择要为此Amazon销售渠道商店连接的[!DNL Commerce]网站。

   此设置还为[导入Amazon订单](./order-settings.md)定义默认的[!DNL Commerce]存储。

1. 对于&#x200B;**[!UICONTROL Email Address]**，输入首选联系人电子邮件地址。

1. 对于&#x200B;**[!UICONTROL New Store Name]**，为新的Amazon销售渠道商店输入一个描述性名称。

   >[!NOTE]
   >
   >此名称仅用作[!DNL Commerce]引用，用于标识[Amazon销售渠道主页](./amazon-sales-channel-home.md)页面上的商店。 你想让你的团队能轻松识别。 例如，您在美国地区销售的Amazon商店可能名为`Amazon Store USA`。

1. 对于&#x200B;**[!UICONTROL Amazon Marketplace Country]**，选择此Amazon销售渠道商店销售产品的地区/国家/地区。 选项：

   - 美国
   - 加拿大
   - 墨西哥
   - 英国

1. 在&#x200B;_[!UICONTROL Map your Magento attributes to Amazon]_部分中，执行以下操作：

   - 对于&#x200B;**[!UICONTROL Product ID on the Amazon market]**，选择要映射到下面选择的[!DNL Commerce]属性的Amazon属性。

      此ID有助于正确匹配[!DNL Commerce]目录中的相应产品。

   - 对于&#x200B;**[!UICONTROL Map a Magento attribute]**，选择要映射到上面选择的Amazon属性的[!DNL Commerce]产品属性。

      [映射](./ob-creating-magento-attributes.md) 属性可确保Amazon列表与目录中的相应产品正确 [!DNL Commerce] 匹配。

1. 单击&#x200B;**[!UICONTROL Connect]**。

   该对话框关闭，新商店显示在[Amazon销售渠道主页](./amazon-sales-channel-home.md)页面上，并显示确认消息。

## 将存储连接到[!DNL Amazon Seller Central]

1. 在存储仪表板上，单击存储卡上的&#x200B;**[!UICONTROL Connect store]** ，以在新选项卡中启动[!DNL Amazon Seller Central]。

1. 输入[!DNL Amazon Seller Central]帐户凭据并单击&#x200B;**[!UICONTROL Sign in]**。

   要完成此连接，您必须使用主用户的登录凭据（用于创建卖家帐户的电子邮件或电话）登录到您的[!DNL Amazon Seller Central]帐户。

1. 如果出现提示，请输入从Amazon收到的代码并单击&#x200B;**[!UICONTROL Sign in]**&#x200B;以完成Amazon双重授权(2FA)。

1. 在&#x200B;_[!UICONTROL Amazon Marketplace Web Service]_确认页面上，选中“[!UICONTROL I understand...]”复选框，然后单击&#x200B;**[!UICONTROL Next]**。

1. 在&#x200B;_[!UICONTROL You are almost done]_消息中，单击&#x200B;**[!UICONTROL Continue]**。

   您已授予Amazon销售渠道权限，可以与您的[!DNL Amazon Seller Central]帐户访问和共享数据。 此时将关闭Amazon页面，并显示一条确认消息。

   将打开[Amazon销售渠道主页](./amazon-sales-channel-home.md)页面，其中显示您的Amazon商店卡。

   要查看存储仪表板，请单击存储卡上的&#x200B;**[!UICONTROL View Store]**。

![Amazon销售渠道主页（带有新商店卡）](assets/asc-dashboard-after-2fa.png)

您的新Amazon销售渠道商店现已连接到您的[!DNL Amazon Seller Central]帐户。

![下一](assets/btn-next.png) [**个图标继续创建列表规则**](./ob-create-listing-rule.md)
