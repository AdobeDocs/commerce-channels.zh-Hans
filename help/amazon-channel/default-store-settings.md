---
title: Amazon列表的默认商店设置
description: 修改默认的Commerce设置以自定义商店的AmazonSales Channel。
role: Admin
feature: Sales Channels, Integration, Configuration
exl-id: 368e5e8e-2bf9-4f9c-86c6-6d375f8a8720
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# Amazon列表的默认商店设置

在商店连接并设置了第一个列表规则后，即表示在Amazon和之间同步数据 [!DNL Commerce] 开始。 有多种类型的商店设置允许您根据自己的需求自定义商店。 可在存储上访问存储设置 [仪表板](./amazon-store-dashboard.md).

商店设置包括：

- [**[!UICONTROL Listing settings]**](./listing-settings.md)  — 控制产品目录与 [!DNL Amazon Marketplace].

- [**[!UICONTROL Order settings]**](./order-settings.md)  — 控制Amazon订单的管理方式。

- [**[!UICONTROL Listing rules]**](./listing-rules.md)  — 定义哪些目录产品有资格在Amazon上列出。

- [**[!UICONTROL Pricing rules]**](./pricing-products.md)  — 定义如何更改符合条件的列表的Amazon标价。

- **[!UICONTROL Store reports]** - [具有竞争力的价格分析](./competitive-price-analysis.md) 和 [列表改进](./listing-improvements.md).

- **[!UICONTROL Logs]** - [列表更改](./listing-changes-log.md) 和 [通信错误](./communication-errors-log.md).

- [**[!UICONTROL Store integration settings]**](./store-integration-settings.md)  — 在中查看电子邮件和Amazon销售渠道商店名称设置 [!DNL Commerce] 管理员。

## 一些重要的默认设置

| 设置 | 默认 | 描述 | 位置 |
|----------------------------------------|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [!UICONTROL Import Amazon Orders] | `Enabled` | 创建对应的 [!DNL Commerce] 订单在收到来自Amazon的新订单时，允许在 [[!DNL Commerce] 订购](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) 工作流。 时间 `Disabled`，Amazon订单导入订单信息以供审阅，但必须在您的网站中 [!DNL Amazon Seller Central] 帐户。 | [订单设置](./order-settings.md) |
| [!UICONTROL Customer Creation] | `No Customer Creation (guest)` | 来自Amazon订单的客户数据未导入到您的 [!DNL Commerce] 数据库。 导入的Amazon订单将作为访客结账处理。 如果您希望构建 [!DNL Commerce] 客户数据库，应将此设置更改为 `Build New Customer Account`. | [订单设置](./order-settings.md) |
| [!UICONTROL Automatic List Action] | `Automatically List Eligible Products` | [!DNL Commerce] 编录产品(符合Amazon的资格要求)以自动发布到Amazon并创建Amazon列表。 如果要手动查看和发布产品，则应将此设置更改为 `Do Not Automatically List Eligible Products`. 等待手动发布的产品会显示在 [_准备列出_](./ready-to-list.md) 选项卡。 | [产品列表操作](./product-listing-actions.md) |
| [!UICONTROL Magento Price Source] | `Price` | 定义用作Amazon列表基础的价格来源属性。 如果您不想使用 [!DNL Commerce] `Price` 作为定价规则所依据的基本价格，您应该将此设置更改为其他属性。 | [挂牌价](./listing-price.md) |
| [!UICONTROL Product Fulfilled By] | `Fulfilled by Merchant` | 商人履行所有的命令。 如果您使用“通过Amazon履行”或混合使用履行方法，则应当更改此设置。 | [履行者](./listing-price.md) |
| [!UICONTROL Listing Product Condition] | `New` | 如果所有产品条件相同，则可以选择一个Amazon条件选项来表示所有产品。 如果您的目录包含处于不同状态（如新建、已使用和已翻新）的产品，则必须将此设置更改为 `Assign Condition Using Product Attribute` 并映射您的 [!DNL Commerce] 条件属性对应于Amazon列表条件。 | [产品列表条件](./product-listing-condition.md) |
| [!UICONTROL Listing Rules] | 无 | 定义用于确定哪些产品已发布到Amazon的Amazon规则。 这些规则提供了许多选项，可用于创建简单到复杂的规则，以将产品作为列表进行包含或排除。 | [上市规则](./listing-rules.md) |
| 定价规则 | 无 | 定义您的Amazon列表价格属性，而不是定义的 _[!UICONTROL Magento Price Source]_在您的 [挂牌价](./listing-price.md). 若要根据您的报价调整您的挂牌价（涨价或跌价），请执行以下操作：_[!UICONTROL Magento Price Source]_ 设置，创建规则。 | [定价规则](./pricing-products.md) |

有关更多信息，请参阅 [商店设置](./ob-store-review.md).
