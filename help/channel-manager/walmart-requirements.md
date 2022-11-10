---
title: '[!DNL Walmart] 要求'
description: '''验证您是否具有 [!DNL Walmart Marketplace]与渠道管理器集成的信息和资源。'
exl-id: c4f247e8-280a-4595-a6c8-cf8b732d7aab
source-git-commit: fd60c8917e4b4e155fb2897ade6e1d96aff2de9d
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---

# [!DNL Walmart] 要求

[!DNL Channel Manager] 需要以下资源和信息才能配置 [!DNL Commerce] 销售渠道 [!DNL Walmart Marketplace.]

* 批准在 [!DNL Walmart] 和凭据登录到注册的Marketplace卖家帐户

* 用于将Adobe Commerce或Magento Open Source连接到的API密钥 [!DNL Walmart Marketplace]

   的 [!DNL Walmart Marketplace] API密钥支持在 [!DNL Channel Manager] Adobe [!DNL Commerce] 或者Magento Open Source和沃尔玛市场。 在启动Channel Manager载入过程之前，在Seller Central中设置API密钥。

## 设置 [!DNL Walmart Seller] 帐户

1. [提交您的Walmart销售商申请](https://marketplace-apply.walmart.com/apply?id=0014M00001zivMpQAI).
1. 获得 [!DNL Walmart], [设置沃尔玛卖家账户](https://seller.walmart.com/signup?q=&amp;origin=solution_provider&amp;src=0014M00001zivMp).

## 生成 [!DNL Walmart Marketplace] 生产API密钥

1. 转到 [!DNL Walmart Marketplace] 生成 [解决方案提供商生产API密钥，用于Adobe](https://developer.walmart.com/#preloginModal?redirectUri=https%3A%2F%2Fdeveloper.walmart.com%2Faccount%2FgenerateKey).

1. 创建密钥并配置权限：

   * 选择Adobe作为解决方案提供商。

   * 如下表所示，设置权限。 有关详细信息，请参阅 [API凭据](https://sellerhelp.walmart.com/seller/s/guide?article=000006422) 在 _沃尔玛销售商帮助_.

   **AdobeWalmart的API密钥配置**

   | **权限** | **设置** |
   |----------------|-------------|
   | 内容 | 完全访问 |
   | 获取信息源 | 仅查看 |
   | 库存 | 完全访问 |
   | 项目 | 完全访问 |
   | 滞后时间 | 完全访问 |
   | 订购 | 完全访问 |
   | 价格 | 完全访问 |
   | 报告 | 仅查看 |
   | 返回结果 | 完全访问 |
   | 规则 | 完全访问 |
   | 装运 | 完全访问 |

## [!DNL Walmart Marketplace] 存储状态

将产品连接到市场时，列出的可用性取决于 [!DNL Walmart Marketplace] 商店：

* 对于实时商店，您的产品选件将列出并在匹配操作完成时可供销售。

* 对于不处于实时状态的商店，您的产品选件会进行暂存，且客户不可见。 当 [!DNL Walmart Marketplace] 存储会上线，暂存列表会自动推送到实时存储。

![[!DNL Walmart Seller Central] 暂存产品](assets/walmart-seller-central-staged.png)

>[!IMPORTANT]
>
>之后 [!DNL Channel Manager] 已安装并配置，则所有库存、价格和订单更新都会自动同步。 不连接 [!DNL Channel Manager] 直到您禁用任何其他更新产品和订单数据的集成，才会将其添加到Walmart Marketplace实时商店。 如果您配置了其他集成，请验证 [!DNL Commerce] 匹配 [!DNL Walmart Marketplace] 连接到实时商店之前。

