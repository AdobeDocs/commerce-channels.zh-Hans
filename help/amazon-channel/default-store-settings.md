---
title: 默认商店设置
description: 修改默认的商务设置，以自定义商店的AmazonSales Channel。
exl-id: 368e5e8e-2bf9-4f9c-86c6-6d375f8a8720
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# 默认存储设置

在您的存储连接并设置了第一个列表规则后，将在Amazon和 [!DNL Commerce] 开始。 存储设置有多种类型，允许您根据需要自定义存储。 在商店中访问商店设置 [仪表板](./amazon-store-dashboard.md).

商店设置包括：

- [**[!UICONTROL Listing settings]**](./listing-settings.md)  — 控制产品目录与 [!DNL Amazon Marketplace].

- [**[!UICONTROL Order settings]**](./order-settings.md)  — 控制Amazon订单的管理方式。

- [**[!UICONTROL Listing rules]**](./listing-rules.md)  — 定义哪些目录产品有资格在Amazon上列出。

- [**[!UICONTROL Pricing rules]**](./pricing-products.md)  — 定义如何为符合条件的列表更改Amazon价目表价格。

- **[!UICONTROL Store reports]** - [竞争性价格分析](./competitive-price-analysis.md) 和 [列表改进](./listing-improvements.md).

- **[!UICONTROL Logs]** - [列出更改](./listing-changes-log.md) 和 [通信错误](./communication-errors-log.md).

- [**[!UICONTROL Store integration settings]**](./store-integration-settings.md)  — 在 [!DNL Commerce] 管理员。

## 一些重要的默认设置

| 设置 | 默认 | 描述 | 位置 |
|--- |--- |--- |--- |
| [!UICONTROL Import Amazon Orders] | `Enabled` | 创建对应的 [!DNL Commerce] 从Amazon接收新订单时发出的订单，允许在 [[!DNL Commerce] 订单数](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}工作流。 When `Disabled`,Amazon将订单导入订单信息以供审核，但订单必须在 [!DNL Amazon Seller Central] 帐户。 | [订单设置](./order-settings.md) |
| [!UICONTROL Customer Creation] | `No Customer Creation (guest)` | 来自Amazon订单的客户数据不会导入您的 [!DNL Commerce] 数据库。 导入的Amazon订单将作为来宾结帐处理。 如果您想要构建 [!DNL Commerce] 客户数据库，您应将此设置更改为 `Build New Customer Account`. | [订单设置](./order-settings.md) |
| [!UICONTROL Automatic List Action] | `Automatically List Eligible Products` | [!DNL Commerce] 目录产品(满足Amazon的资格要求)以自动发布到Amazon并创建Amazon列表。 如果要手动查看和发布产品，应将此设置更改为 `Do Not Automatically List Eligible Products`. 等待手动发布的产品显示在 [_准备列表_](./ready-to-list.md) 选项卡。 | [产品列表操作](./product-listing-actions.md) |
| [!UICONTROL Magento Price Source] | `Price` | 定义用作Amazon列表基础的价格源属性。 如果您不想使用 [!DNL Commerce] `Price` 属性作为定价规则所依据的基本价格，您应将此设置更改为其他属性。 | [上市价格](./listing-price.md) |
| [!UICONTROL Product Fulfilled By] | `Fulfilled by Merchant` | 商人履行了所有的命令。 如果您使用“通过Amazon履行”或使用多种履行方法，则应更改此设置。 | [履行者](./listing-price.md) |
| [!UICONTROL Listing Product Condition] | `New` | 如果您的所有产品都是相同的条件，则可以选择一个Amazon条件选项来表示您的所有产品。 如果目录包含不同条件（如“新建”、“已用”和“已翻新”）的产品，则必须将此设置更改为 `Assign Condition Using Product Attribute` 映射 [!DNL Commerce] 条件属性添加到Amazon列表条件。 | [产品列表条件](./product-listing-condition.md) |
| [!UICONTROL Listing Rules] | 无 | 定义用于确定Amazon销售渠道发布到Amazon的产品的规则。 这些规则提供了许多选项，可用于创建简单到复杂的规则，以将产品作为列表包含或排除。 | [上市规则](./listing-rules.md) |
| 定价规则 | 无 | 定义与定义的Amazon列表价格属性不同的 _[!UICONTROL Magento Price Source]_在 [上市价格](./listing-price.md). 根据您的_[!UICONTROL Magento Price Source]_ 设置，创建规则。 | [定价规则](./pricing-products.md) |

有关更多信息，请参阅 [存储设置](./ob-store-review.md).
