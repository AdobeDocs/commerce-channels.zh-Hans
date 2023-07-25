---
title: Amazon销售渠道 — 价格规则示例
description: 为了帮助您为Amazon列表设计定价规则，请根据常见方案查看这些示例。
feature: Sales Channels, Price Rules
exl-id: 4d9717ba-4ad6-468d-b4ca-99f8620b60b4
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '925'
ht-degree: 2%

---

# 价格规则示例

## 标准价格规则示例

### 放弃后续规则

能够放弃后续规则，是定价规则内的一项强大功能，可防止多个定价规则栈叠在一起并提供意想不到的额外折扣。 要放弃后续规则，定价规则必须使用 _[!UICONTROL Priority]_部分 [定价规则常规设置](./pricing-rule-general-settings.md).

如果 **[!UICONTROL Discard Subsequent Rules]** 设置为 `Yes`，优先级较低（数字较高）的规则不适用于符合条件的产品。

例如，假设有三个定价规则：

| 示例 | 规则名称 | 优先级 | 放弃后续规则 |
|---------|-----------------------|----------|-------------------------|
| 1 | 优惠季10%优惠 | 1 | 否 |
| 2 | 销售产品优惠$2 | 2 | 是 |
| 3 | 所有产品现享5%优惠 | 3 | 否 |

在此方案中，规则#1和#2适用于符合条件的产品。 规则#3仅适用于规则#2中未包含的合格产品，因为其优先级低于示例#2和 **[!UICONTROL Discard Subsequent Rules]** 设置为 `Yes`. 因此，符合条件的销售类别产品将获得10%的折扣，以及Amazon上市价的2美元折扣。

### 应用两个标准价格规则

| 字段 | 设置 — 规则1 | 设置 — 规则2 |
|--------------------------------|---------------------|-----------------------|
| [!UICONTROL Rule Name] | 规则–1 | 规则–2 |
| [!UICONTROL Priority] | 1 | 2 |
| [!UICONTROL Rule Type] | 标准价格规则 | 标准价格规则 |
| [!UICONTROL Price action] | 减少方式 | 减少方式 |
| [!UICONTROL Apply] | 以百分比应用 | 应用为固定金额 |
| [!UICONTROL Adjustment Amount] | 10 | 10 |

#### 产品1

价格：45.49美元

适用细则1:45.49美元x(0.9) = 40.94美元

适用规则2:40.94美元 — 10.00美元= 30.94美元

适用规则1和规则2后的最终价格：30.94美元

#### 产品2

价格：47.76美元

适用规则1:47.76美元x(0.9) = 42.98美元

适用规则2:42.98美元 — 10.00美元= 32.98美元

应用规则1和规则2后的最终价格：32.98美元

## 智能重新定价规则示例

### 具有底价来源的Buy Box价格=价格

| 字段 | 设置 |
|--------------------------------------|----------------------------|
| [!UICONTROL Rule Name] | 规则–1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | 智能重新定价规则 |
| [!UICONTROL Competitor Price Source] | 使用“Buy Box”价格 |
| [!UICONTROL Price Action] | 匹配竞争对手价格 |
| [!UICONTROL Floor Price Source] | 价格 |
| [!UICONTROL Floor Price Action] | 匹配 |

#### 产品1

价格：15美元

[Buy Box](./buy-box-competitor-pricing.md) Amazon价格：10美元

因为 [Buy Box](./buy-box-competitor-pricing.md) 价格低于原价，按原价列示。

应用规则后的最终价格：15美元

#### 产品2

价格：5美元

[Buy Box](./buy-box-competitor-pricing.md) Amazon价格：10美元

因为 [Buy Box](./buy-box-competitor-pricing.md) 价格高于原价，则产品将列在 [Buy Box](./buy-box-competitor-pricing.md) 价格。

应用规则后的最终价格：10美元

### 具有底价来源的Buy Box价格=价格和20%的价格下降

| 字段 | 设置 |
|--------------------------------------|----------------------------|
| [!UICONTROL Rule Name] | 规则–1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | 智能重新定价规则 |
| [!UICONTROL Competitor Price Source] | 使用“Buy Box”价格 |
| [!UICONTROL Price Action] | 匹配竞争对手价格 |
| [!UICONTROL Floor Price Source] | 价格 |
| [!UICONTROL Floor Price Action] | 减少方式 |
| [!UICONTROL Apply] | 按百分比应用 |
| [!UICONTROL Floor Adjustment Amount] | 20 |

#### 产品1

价格：20美元

计算出的底价：$16

[Buy Box](./buy-box-competitor-pricing.md) Amazon价格：15美元

因为 [Buy Box](./buy-box-competitor-pricing.md) 价格小于计算得出的值 [底价](./floor-price.md)，则计算得出的值中会列出产品 [底价](./floor-price.md).

应用规则后的最终价格：16美元

#### 产品2

价格：15美元

已计算 [底价](./floor-price.md)：12美元

[Buy Box](./buy-box-competitor-pricing.md) Amazon价格：15美元

因为 [Buy Box](./buy-box-competitor-pricing.md) 价格大于计算值 [底价](./floor-price.md)，则产品将列在 [Buy Box](./buy-box-competitor-pricing.md) 价格。

应用规则后的最终价格：15美元

#### 产品3

价格：17美元

计算的最低价格：$13.60

[Buy Box](./buy-box-competitor-pricing.md) Amazon价格：15美元

因为 [Buy Box](./buy-box-competitor-pricing.md) 价格大于计算值 [底价](./floor-price.md)，则产品将列在 [Buy Box](./buy-box-competitor-pricing.md) 价格。

应用规则后的最终价格：15美元

### 最低价格（包含所有竞争对手的价格并使用所有竞争对手的产品条件）

| 字段 | 设置 |
|----------------------------------------|-----------------------------------------|
| [!UICONTROL Rule Name] | 规则–1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | 智能重新定价规则 |
| [!UICONTROL Competitor Price Source] | 使用最低竞争者价格 |
| [!UICONTROL Minimum Positive Feedback] | 所有竞争对手价格 |
| [!UICONTROL Conditional Variance] | 使用所有竞争对手的产品条件 |
| [!UICONTROL Price Action] | 匹配竞争对手价格 |
| [!UICONTROL Floor Price Source] | 价格 |
| [!UICONTROL Floor Price Action] | 匹配 |

| 价格 | 条件 |
|-------|-----------------|
| $17 | 新 |
| $15 | 新 |
| $14 | 已使用；非常好 |
| $13 | 已使用；良好 |

#### 产品1

价格：10美元

条件：新建

由于新条件的最低竞争对手价格是15美元，因此产品上市时为15美元。

应用规则后的最终价格：15美元

#### 产品2

价格：10美元

条件：已使用；可接受

因为 [最低竞争对手价格](./lowest-competitor-pricing.md) 对于“已使用”条件为$13，则产品列为$13。

应用规则后的最终价格：13美元

### 结合了最高价格、货币兑换和VAT的智能重新定价规则

| 字段 | 设置 |
|-----------------------------------|---------------|
| [!UICONTROL VAT] | 10% |
| [!UICONTROL Ceiling price source] | $10 |
| [!UICONTROL Currency conversion] | 1.25欧元：1美元 |

[最高价格](./optional-ceiling-price.md) 欧洲(VAT)市场：$10 x 1.25 = $12.50

当 [最高价格](./optional-ceiling-price.md) 在欧洲的(VAT)市场受到冲击，增值税被计算并增加。

增值税后最终价格：$12.50 x (1.1) = $13.75

### 组合多个定价规则、最高价格、货币折换和增值税

#### 智能定价规则（来自上一个示例）

| 字段 | 设置 |
|----------------------|---------------|
| 优先级 | 1 |
| 增值税 | 10% |
| 最高价来源 | $10 |
| 货币换算 | 1.25欧元：1美元 |

[最高价格](./optional-ceiling-price.md) 欧洲(VAT)市场：$10 x 1.25 = $12.50

增值税后最终价格：$12.50 x (1.1) = $13.75

#### 标准定价规则

| 字段 | 设置 |
|--------------------------------|-----------------------|
| [!UICONTROL Priority] | 2 |
| [!UICONTROL Price Action] | 增加方式 |
| [!UICONTROL Apply] | 应用为固定金额 |
| [!UICONTROL Adjustment Amount] | $5.00 |

当 [最高价格](./optional-ceiling-price.md) 之后，在智能定价规则之上应用标准定价规则。

应用标准定价规则后的最终价格：$13.75 + $5.00 = $18.75

### 价格调整

在本例中，最具竞争力的价格是通过查看Amazon来定义的 [竞争对手的最低价格](./lowest-competitor-pricing.md) 95%的正面反馈，最低反馈数量为1,000个商家评论。

![价格调整示例](assets/amazon-price-adjustment-example.png){width="600" zoomable="yes"}

运行基于这些参数的搜索后，竞争性价格回升至25美元。

从这里，有三种不同的 [价格规则操作](./pricing-rule-actions.md) 基于此最低价格进行选择。

| 字段 | 描述 |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Price Action] | 选项：<ul><li>**[!UICONTROL Decrease By]**  — 此选项会降低您的上市价格相对于 [最低竞争对手价格](./lowest-competitor-pricing.md).</li><li>**[!UICONTROL Increase By]**  — 此选项会提高您的上市价格相对于 [最低竞争对手价格](./lowest-competitor-pricing.md).</li><li>**[!UICONTROL Match Competitor Price]**  — 此选项会根据参数更改您的Amazon上市价格以匹配最低价格。 在示例中，Amazon的挂牌价为25美元。</li></ul> |
| [!UICONTROL Apply] | 选项：按百分比核销/按固定金额核销 |
| [!UICONTROL Adjustment Amount] | 用于定义要应用的折扣的百分比或固定金额的数值。 <br>选择这些选项后，定价最低，且可以降低0.01 USD。 |

### 底价

| 字段 | 设置 |
|--------------------------------------|---------------------|
| [!UICONTROL Floor Price Source] | 成本= 5美元 |
| [!UICONTROL Floor Price Action] | 增加方式 |
| [!UICONTROL Apply] | 以百分比应用 |
| [!UICONTROL Floor Adjustment Amount] | 5 |

[底价](./floor-price.md) 计算=最低价格来源 `$5` x下限调整金额 `5%` = 5.25美元

应用智能定价规则后，当成本为5美元时，此特定产品的挂牌价将低于5.25美元。
