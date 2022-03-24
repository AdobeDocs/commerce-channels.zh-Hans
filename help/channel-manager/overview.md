---
title: 关于 [!DNL Channel Manager]
description: 了解如何安装和使用 [!DNL Channel Manager] 将Adobe Commerce和Magento Open Source商店与第三方市场集成，并创建销售渠道，从您的商务管理员无缝地管理市场列表、定价、库存和销售。
role: User
level: Intermediate
exl-id: 91265973-d2ad-4925-aa10-260d7e186f20
source-git-commit: 8f07b215c20cc28aa9a6862bcb2b00da30a1ed84
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 0%

---

# 概述

Adobe Commerce和Magento Open Source的渠道管理器在管理员中提供了一个便捷的工作区，用于管理第三方市场(如沃尔玛、Amazon和eBay)上的渠道销售。 增加销售并拓展到新市场，同时从商务管理员处无缝管理销售渠道操作。

![[!DNL Channel Manager] 扩展管理员视图](assets/channel-manager-admin-entry-page.png)

## 测试版版本概述

渠道管理器测试版支持希望在Walmart Marketplace上提供产品的Adobe Commerce或Magento Open Source销售商。

此版本支持以下功能来管理销售渠道操作：

* 在Adobe Commerce或Magento Open Source与Walmart Marketplace之间建立API连接

* 使用产品匹配将产品从Channel Manager发布到Walmart

* 例如，在渠道管理器中查看产品列表状态 *草稿*, *处理*, *匹配*, *错误*.

* 将匹配产品的库存数量从Commerce同步到Walmart

* 从Commerce到Walmart的匹配产品的同步目录定价

* 从Walmart Marketplace接收订单，并在 [!DNL Commerce] 订单仪表板

### Channel Manager操作的预期滞后

数据同步在 [!DNL Channel Manager] 和链接 [!DNL Walmart Marketplace] 存储需要一些时间才能完成。 查看 [!DNL Channel Manager] 操作以帮助计划销售渠道操作。

**Channel Manager操作的预计延迟**
| **操作**                              | **描述**                                                                                                                               | **预期延迟**                                                                                                        | |—|—|—| |将产品添加到渠道管理器 |从商务产品目录中选择产品，然后将它们导入渠道管理器。                                                       | **最多5分钟** — 如果您选择了许多产品（例如整个产品目录），则导入过程会花费更长的时间。 | |在Walmart Marketplace上匹配产品 |在渠道管理器中选择产品清单，然后发送到沃尔玛进行匹配。                                                                  | **最多30分钟** — 如果选择多个产品，则根据所选数量，匹配过程将花费更长的时间。   | |库存更新 |商务中库存数量发生更改时。 渠道管理器同步更新到Walmart。                                                         | **最多10分钟**                                                                                                      | |价格更新 |当产品价格发生更改时，渠道管理器会将更新同步到Walmart。                                                                    | **最多5分钟**                                                                                                       | |从Walmart到Commerce的订单同步 |客户在Walmart Marketplace上订购商务产品。 沃尔玛将订单发给渠道经理。 顺序显示在订单仪表板中。 | **最多30分钟**                                                                                                      | |在Oracle Commerce Order Management中创建的订单 |渠道管理器从沃尔玛订单中创建商务订单，并更新订单仪表板以包含商务订单编号。       | **最多5分钟**                                                                                                       |

## 沃尔玛先决条件

您需要Walmart提供以下信息才能将Commerce与Walmart Marketplace集成：

* 批准在沃尔玛销售，并凭证登录注册的Marketplace销售商帐户

* 用于将Adobe Commerce或Magento Open Source连接到Walmart Marketplace的API密钥

   Walmart Marketplace API密钥支持Adobe Commerce或Magento Open Source的渠道管理器与Walmart Marketplace之间的集成。 在启动Channel Manager载入过程之前，在Seller Central中设置API密钥。

### 设置Marketplace卖家帐户

1. [提交您的Walmart销售商申请](https://marketplace-apply.walmart.com/apply?id=0014M00001zivMpQAI)
2. 在获得沃尔玛的批准后， [设置沃尔玛卖家账户](https://sellerhelp.walmart.com/seller/s/guide?article=000008219).

### 生成Walmart Marketplace API密钥

1. 转到Walmart Marketplace以生成 [解决方案提供商生产API密钥，用于Adobe](https://developer.walmart.com/#preloginModal?redirectUri=https%3A%2F%2Fdeveloper.walmart.com%2Faccount%2FgenerateKey).

1. 创建密钥并配置权限：

   * 选择Adobe作为解决方案提供商。

   * 如下表所示，设置权限。 有关详细信息，请参阅 [API凭据](https://sellerhelp.walmart.com/seller/s/guide?article=000006422) 在 *沃尔玛销售商帮助*.

|    **AdobeWalmart的API密钥配置**
| **权限** | **设置** | |—|—| |内容 |完全访问 | |获取信息源 |仅查看 | |清单 |完全访问 | |项目 |完全访问 | |滞后时间 |完全访问 | |顺序 |完全访问 | |价格 |完全访问 | |报表 |仅查看 | |返回 |完全访问 | |规则 |完全访问 | |装运 |完全访问 |

## 沃尔玛商店状态

当您向Walmart Marketplace发布产品时，上市的可用性取决于您的Walmart Marketplace商店的状态：

* 对于实时商店，您的产品选件将在匹配操作完成后立即列出并可供销售。

* 对于不处于实时状态的商店，您的产品选件会进行暂存，且客户不可见。 商店一上线，就会自动将分阶段的列表推送到实时商店。


![[!DNL Walmart Seller Central] 暂存产品](assets/walmart-seller-central-staged.png)
