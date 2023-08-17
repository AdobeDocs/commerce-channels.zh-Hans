---
title: “简介 [!DNL Amazon Sales Channel]"
description: '"[!DNL Amazon Sales Channel] 使商家能够在以下位置无缝销售产品： [!DNL Amazon Marketplace]“'
redirect_from: /sales-channels/amazon/amazon-sales-channel.html
role: Admin, User, Leader
exl-id: a4a6f446-7029-4c92-bce3-5b857cc33056
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 0%

---

# 简介 [!DNL Amazon Sales Channel]

作为Adobe Commerce或Magento Open Source商家，您可以使用 [!DNL Amazon Sales Channel] 该扩展可将您的商店与世界上最大的全球Internet购物目的地相集成。 Amazon此扩展通过连接 [!DNL Commerce] 与您的 [!DNL Amazon Seller Central] 帐户，并提供目录和订单数据的自动化和同步。 完全管理所有Amazon列表，实施简单或智能的定价规则，并通过单一工具维护您的订单和库存 [!DNL Commerce] 仪表板。

之后 [入门](./amazon-onboarding-home.md)， [!DNL Commerce] 成为“中央指挥中心”，用于管理和控制Amazon列表、订单和库存以及Amazon商店的定价。 [存储集成](./store-integration.md) 连接您的 [!DNL Commerce] 实例和Amazon，以便在两个平台之间同步数据。 Amazon sales channel使您能够：

- [载入](./amazon-onboarding-home.md) 并集成一个或多个 [!DNL Amazon Seller Central] 具有Adobe Commerce或Magento Open Source的帐户。

- 导入并同步现有的Amazon列表，并与中的产品进行匹配 [!DNL Commerce] 目录，创建集中式产品目录。

- 创建和管理Amazon产品列表，以便 [!DNL Commerce] 目录。

- 查看和完成（发运）订单 [!DNL Commerce] 和Amazon，同步订单状态、付款和退款信息。

- 查看以下项的分析和错误日志 [有竞争力的价格](./competitive-price-analysis.md)， [列表更改](./listing-changes-log.md)、和 [沟通问题](./communication-errors-log.md).

访问您的Amazon商店，以便在Amazon销售渠道中查看和管理所有这些功能、帐户信息、清单、订单等 [主页](./amazon-sales-channel-home.md).

## 促销和定价

使用 [!DNL Amazon Sales Channel] 扩展上，您可以：

- 将Amazon列表定价同步到 [!DNL Commerce] 目录价格（或替代价格属性）。

- 启用MSRP [删除定价](./listing-price.md#configure-listing-price-settings) 在您的Amazon清单中增加客户价值主张。

- 启用和管理 [最低广告价格(MAP)](./listing-price.md#configure-listing-price-settings) 在Amazon列表中。

- 配置其他 [增值税](./listing-price.md#configure-listing-price-settings) (在您的Amazon定价中)。

- 在中为“可用数量”设置自定义值 [库存/数量设置](./stock-quantity.md#configure-stock--quantity-settings) 与您的Amazon清单一起显示，以增加购买者的紧迫感。

## 定价规则

使用 [!DNL Amazon Sales Channel] 扩展上，您可以：

- 创建可栈叠、灵活且复杂的 [定价规则](./pricing-products.md) 为日常销售或季节性促销活动管理Amazon定价。

- 创建 [floor](./floor-price.md) 和 [上限](./optional-ceiling-price.md) 价格保护您的最低和最高价格。

- 创建和管理 [智能重新定价规则](./intelligent-repricing-rules.md) 相对于其他Amazon竞争对手，自动调整产品定价([最低竞争对手](./lowest-competitor-pricing.md) 和 [Buy Box](./buy-box-competitor-pricing.md) 价格)。

## 目录信息源管理

使用 [!DNL Amazon Sales Channel] 扩展上，您可以：

- 导入现有的Amazon列表（产品），并与中的现有列表匹配或创建产品 [!DNL Commerce] 目录。

- 发布您的 [!DNL Commerce] “产品”到Amazon以创建Amazon列表。

- 创建 [覆盖](./creating-editing-overrides.md) 设置个人价格、处理时间、条件和卖方备注消息。

- 导入和映射产品 [属性](./attributes-view.md) 从您的Amazon列表中自动匹配您的产品 [!DNL Commerce] 目录。

- 设置多个搜索参数以将Amazon列表与您的 [!DNL Commerce] 目录。

- 定义 [上市规则](./listing-rules.md) 以确定 [!DNL Commerce] 产品有资格在Amazon上列出。

- 设置默认值 [处理时间](./product-listing-actions.md) 用于新的Amazon列表。

- 根据匹配列表条件 [!DNL Commerce] 属性。

- 为每种条件类型添加卖方备注（可选）。

- 将Amazon列表导入到您的中时实施数量阈值 [!DNL Commerce] 目录。

- 查看推荐的 [列表改进](./listing-improvements.md).

## 订单管理和客户服务

使用 [!DNL Amazon Sales Channel] 扩展上，您可以：

- 在Amazon中支持和处理订单，以及 [!DNL Commerce].

- [导入](./order-settings.md#configure-order-settings) 您的Amazon订单 [!DNL Commerce] 或者把它们留在Amazon里。

- 定义您的 [!DNL Commerce] 网站商店，以便与您的Amazon订单关联，从而导入和管理订单。

- 查看、取消和发货订单 [!DNL Commerce] 和/或Amazon，具体取决于您的 [履行设置](./fulfilled-by.md).

- 将您的Amazon订单状态映射到中的自定义状态 [!DNL Commerce] （可选）。

- 查看和管理订单错误以解决问题并与客户建立联系。

- 将订单跟踪数据发送至 [!DNL Amazon Seller Central] 帐户。

- [取消订单](./cancel-unshipped-order.md) 并选择原因响应。

- 查看 [最新订单](./amazon-store-dashboard.md) 有关Amazon订单的信息。

## 报表

使用 [!DNL Amazon Sales Channel] 扩展上，您可以查看有关以下各项的报告信息：

- 按活动、非活动、符合条件和未完成状态列出的列表。

- 等待装运的订单。

- 最近的订单。

- Amazon [列出更改日志](./listing-changes-log.md) 审阅产品/列表信息源更改（如价格和数量）。

- 产品 [Buy Box](./buy-box-competitor-pricing.md) 竞争对手定价数据。

- 产品 [最低竞争对手定价](./lowest-competitor-pricing.md) 数据。

## 支持全球销售

使用 [!DNL Amazon Sales Channel] 扩展上，您可以：

- 管理多个 [!DNL Amazon Marketplace] 区域（国家/地区）。

- 使用支持多种货币 [Commerce货币配置工具](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/currency/currency-configuration.html).

- 管理来自您的产品位置和Amazon履行中心的发运。

## 客户管理

构建 [!DNL Commerce] 客户数据库创建者 [导入客户数据](./order-settings.md#configure-order-settings) 与您的Amazon订单相关联。 通过扩展的客户列表，提升您的营销潜力 [!DNL Amazon Marketplace] 列表和 [!DNL Commerce] 店面。


入门很简单。 一个简短的入门培训流程可指导您创建 [!DNL Amazon Seller Central] 帐户并与Amazon sales channel store和 [!DNL Commerce] 用于管理Amazon列表、订单、库存和履行的catalog。 一个中央仪表板显示所有Amazon sales channel store集成和Amazon列表的状态更新。 接触全球的新客户 [!DNL Amazon Marketplace] 简化和自动化的流程 — 只需很少或完全不需要安装新系统的成本和人力。

集成您的 [!DNL Amazon Seller Central] 帐户， [!DNL Amazon Sales Channel] 扩展使您能够管理帐户并在以下位置同步数据： [!DNL Commerce] 和Amazon。 它使您能够通过创建清单、管理促销、设置价格以及直接管理库存和履行 [!DNL Commerce] 管理员。 这些选项包括定价规则，用于监控Amazon对同一项目的定价，并自动调整您的价格以提高竞争力。

