---
title: Amazon列表的默认商店设置
description: 修改默认的Commerce设置以自定义应用商店的AmazonSales Channel。
role: Admin
feature: Sales Channels, Integration, Configuration
exl-id: 368e5e8e-2bf9-4f9c-86c6-6d375f8a8720
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# Amazon列表的默认商店设置

在商店连接并设置了第一个列表规则后，Amazon与[!DNL Commerce]之间的数据同步将开始。 有多种类型的商店设置允许您根据自己的需求自定义商店。 在商店[仪表板](./amazon-store-dashboard.md)上访问商店设置。

商店设置包括：

- [**[!UICONTROL Listing settings]**](./listing-settings.md) — 控制产品目录与[!DNL Amazon Marketplace]的交互方式。

- [**[!UICONTROL Order settings]**](./order-settings.md) — 控制Amazon订单的管理方式。

- [**[!UICONTROL Listing rules]**](./listing-rules.md) — 定义哪些目录产品有资格在Amazon上列出。

- [**[!UICONTROL Pricing rules]**](./pricing-products.md) — 定义如何更改符合条件的列表的Amazon标价。

- **[!UICONTROL Store reports]** - [竞争性价格分析](./competitive-price-analysis.md)和[列表改进](./listing-improvements.md)。

- **[!UICONTROL Logs]** - [正在列出更改](./listing-changes-log.md)和[通信错误](./communication-errors-log.md)。

- [**[!UICONTROL Store integration settings]**](./store-integration-settings.md) — 在[!DNL Commerce]管理员中查看电子邮件和Amazon销售渠道商店名称设置。

## 一些重要的默认设置

| 设置 | 默认 | 描述 | 位置 |
|----------------------------------------|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [!UICONTROL Import Amazon Orders] | `Enabled` | 在从Amazon收到新订单时创建相应的[!DNL Commerce]订单，从而允许在[[!DNL Commerce] 订单](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html)工作流中管理订单。 当`Disabled`时，Amazon订单导入订单信息以供审核，但订单必须在您的[!DNL Amazon Seller Central]帐户中进行管理。 | [订单设置](./order-settings.md) |
| [!UICONTROL Customer Creation] | `No Customer Creation (guest)` | 来自Amazon订单的客户数据未导入到[!DNL Commerce]数据库中。 导入的Amazon订单将作为访客结账处理。 如果要构建[!DNL Commerce]客户数据库，应将此设置更改为`Build New Customer Account`。 | [订单设置](./order-settings.md) |
| [!UICONTROL Automatic List Action] | `Automatically List Eligible Products` | [!DNL Commerce]目录产品(符合Amazon的资格要求)以自动发布到Amazon并创建Amazon列表。 如果要手动查看和发布产品，则应将此设置更改为`Do Not Automatically List Eligible Products`。 等待手动发布的产品出现在&#x200B;[_准备列出_](./ready-to-list.md)&#x200B;选项卡上。 | [产品列表操作](./product-listing-actions.md) |
| [!UICONTROL Magento Price Source] | `Price` | 定义用作Amazon列表基础的价格来源属性。 如果您不想使用[!DNL Commerce] `Price`属性作为您的定价规则所依据的基本价格，则应将此设置更改为其他属性。 | [列表价格](./listing-price.md) |
| [!UICONTROL Product Fulfilled By] | `Fulfilled by Merchant` | 商人履行所有的命令。 如果您使用“通过Amazon履行”或混合使用履行方法，则应当更改此设置。 | [履行者：](./listing-price.md) |
| [!UICONTROL Listing Product Condition] | `New` | 如果所有产品条件相同，则可以选择一个Amazon条件选项来表示所有产品。 如果您的目录包含不同条件的产品（例如“新建”、“已使用”和“已翻新”），则必须将此设置更改为`Assign Condition Using Product Attribute`，并将[!DNL Commerce]条件属性映射到Amazon列表条件。 | [产品列表条件](./product-listing-condition.md) |
| [!UICONTROL Listing Rules] | 无 | 定义用于确定哪些产品已发布到Amazon的Amazon规则。 这些规则提供了许多选项，可用于创建简单到复杂的规则，以将产品作为列表进行包含或排除。 | [列表规则](./listing-rules.md) |
| 定价规则 | 无 | 定义您的Amazon列表价格属性而不是[列表价格](./listing-price.md)中定义的&#x200B;_[!UICONTROL Magento Price Source]_。 若要根据_[!UICONTROL Magento Price Source]_&#x200B;设置调整您的挂牌价（涨价或跌价），请创建规则。 | [定价规则](./pricing-products.md) |

有关详细信息，请参阅[存储设置](./ob-store-review.md)。
