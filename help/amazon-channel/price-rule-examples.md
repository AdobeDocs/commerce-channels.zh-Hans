---
title: Amazon sales channel — 价格规则示例
description: 为了帮助您为Amazon列表设计定价规则，请根据常见方案查看这些示例。
feature: Sales Channels, Price Rules
exl-id: 4d9717ba-4ad6-468d-b4ca-99f8620b60b4
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '1026'
ht-degree: 1%

---

# 价格规则示例

## 标准价格规则示例

### 放弃后续规则

能够放弃后续规则是定价规则内的一项强大功能，可防止多个定价规则栈叠并提供意想不到的额外折扣。 要放弃后续规则，定价规则必须使用[定价规则常规设置](./pricing-rule-general-settings.md)的&#x200B;_[!UICONTROL Priority]_部分中设置的优先级。

如果&#x200B;**[!UICONTROL Discard Subsequent Rules]**&#x200B;设置为`Yes`，则优先级较低（数字较高）的规则不适用于符合条件的产品。

例如，假设有三个定价规则：

| 示例 | 规则名称 | 优先级 | 放弃后续规则 |
|---------|-----------------------|----------|-------------------------|
| 1 | 销售商品10%优惠 | 1 | 否 |
| 2 | 销售产品2美元优惠 | 2 | 是 |
| 3 | 所有产品5%优惠 | 3 | 否 |

在此方案中，规则#1和#2适用于符合条件的产品。 规则#3仅适用于规则#2中未包含的合格产品，因为其优先级低于示例#2，并且&#x200B;**[!UICONTROL Discard Subsequent Rules]**&#x200B;设置为`Yes`。 因此，符合条件的销售类别产品将获得10%的折扣，以及Amazon上市价格的2美元折扣。

### 应用两个标准价格规则

| 字段 | 设置 — 规则1 | 设置 — 规则2 |
|--------------------------------|---------------------|-----------------------|
| [!UICONTROL Rule Name] | 规则–1 | 规则–2 |
| [!UICONTROL Priority] | 1 | 2 |
| [!UICONTROL Rule Type] | 标准价格规则 | 标准价格规则 |
| [!UICONTROL Price action] | 减少方式 | 减少方式 |
| [!UICONTROL Apply] | 应用为百分比 | 申请为固定金额 |
| [!UICONTROL Adjustment Amount] | 10 | 10 |

#### 产品1

价格：45.49美元

适用规则1:45.49美元x(0.9) = 40.94美元

适用规则2：$40.94 - $10.00 = $30.94

应用规则1和规则2后的最终价格：$30.94

#### 产品2

价格：47.76美元

适用规则1:47.76美元x(0.9) = 42.98美元

适用规则2:42.98美元 — 10.00美元= 32.98美元

应用规则1和规则2后的最终价格：32.98美元

## 智能重新定价规则示例

### 具有底价的Buy Box价格Source =价格

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

来自Amazon的[Buy Box](./buy-box-competitor-pricing.md)价格： $10

由于[Buy Box](./buy-box-competitor-pricing.md)的价格低于原始价格，因此产品将按原始价格列出。

应用规则后的最终价格：15美元

#### 产品2

价格：5美元

来自Amazon的[Buy Box](./buy-box-competitor-pricing.md)价格： $10

由于[Buy Box](./buy-box-competitor-pricing.md)的价格高于原始价格，因此产品将以[Buy Box](./buy-box-competitor-pricing.md)的价格列出。

应用规则后的最终价格：10美元

### Buy Box价格（最低价） Source =价格和20%的价格降幅

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

来自Amazon的[Buy Box](./buy-box-competitor-pricing.md)价格： $15

由于[Buy Box](./buy-box-competitor-pricing.md)价格小于计算的[楼面价格](./floor-price.md)，因此产品将按计算的[楼面价格](./floor-price.md)列出。

应用规则后的最终价格：16美元

#### 产品2

价格：15美元

已计算[底价](./floor-price.md)： $12

来自Amazon的[Buy Box](./buy-box-competitor-pricing.md)价格： $15

由于[Buy Box](./buy-box-competitor-pricing.md)价格大于计算得出的[楼层价格](./floor-price.md)，因此产品将以[Buy Box](./buy-box-competitor-pricing.md)价格列出。

应用规则后的最终价格：15美元

#### 产品3

价格：17美元

计算出的底价：$13.60

来自Amazon的[Buy Box](./buy-box-competitor-pricing.md)价格： $15

由于[Buy Box](./buy-box-competitor-pricing.md)价格大于计算得出的[楼层价格](./floor-price.md)，因此产品将以[Buy Box](./buy-box-competitor-pricing.md)价格列出。

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
| 17美元 | 新建 |
| 15美元 | 新建 |
| 14美元 | 已使用；非常好 |
| 13美元 | 已使用；良好 |

#### 产品1

价格：10美元

条件：新建

由于新条件的最低竞争对手价格为15美元，因此产品上市时的价格为15美元。

应用规则后的最终价格：15美元

#### 产品2

价格：10美元

条件：已使用；可接受

由于“已使用”条件的[最低竞争对手价格](./lowest-competitor-pricing.md)为$13，因此产品将列为$13。

应用规则后的最终价格：13美元

### 结合了最高定价、货币兑换和增值税的智能重新定价规则

| 字段 | 设置 |
|-----------------------------------|---------------|
| [!UICONTROL VAT] | 10% |
| [!UICONTROL Ceiling price source] | 10美元 |
| [!UICONTROL Currency conversion] | 1.25欧元：1美元 |

[欧洲(VAT)市场中的最高价格](./optional-ceiling-price.md)：$10 x 1.25 = $12.50

当达到欧洲(VAT)市场中的[最高价格](./optional-ceiling-price.md)时，将计算并添加VAT。

增值税后最终价格：$12.50 x (1.1) = $13.75

### 组合多个定价规则、最高定价、货币折换和增值税

#### 智能定价规则（来自上一示例）

| 字段 | 设置 |
|----------------------|---------------|
| 优先级 | 1 |
| 增值税 | 10% |
| 最高价来源 | 10美元 |
| 货币换算 | 1.25欧元：1美元 |

[欧洲(VAT)市场中的最高价格](./optional-ceiling-price.md)：$10 x 1.25 = $12.50

增值税后最终价格：$12.50 x (1.1) = $13.75

#### 标准定价规则

| 字段 | 设置 |
|--------------------------------|-----------------------|
| [!UICONTROL Priority] | 2 |
| [!UICONTROL Price Action] | 增加方式 |
| [!UICONTROL Apply] | 申请为固定金额 |
| [!UICONTROL Adjustment Amount] | 5美元 |

当达到[最高价格](./optional-ceiling-price.md)时，标准定价规则将应用于智能定价规则之上。

应用标准定价规则后的最终价格：$13.75 + $5.00 = $18.75

### 价格调整

在此示例中，最具竞争力的价格是通过查看Amazon [竞争对手的最低价格](./lowest-competitor-pricing.md)确定的，该价格具有95%的正面反馈以及最低反馈计数，即1,000个商家评论。

![价格调整示例](assets/amazon-price-adjustment-example.png){width="600" zoomable="yes"}

基于这些参数运行该搜索后，竞争价格回落至25美元。

在此处，根据此最低价格有三个不同的[价格规则操作](./pricing-rule-actions.md)选择。

| 字段 | 描述 |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Price Action] | 选项：<ul><li>**[!UICONTROL Decrease By]** — 此选项会相对于[最低竞争对手价格](./lowest-competitor-pricing.md)降低您的上市价格。</li><li>**[!UICONTROL Increase By]** — 此选项会提高您的上市价格相对于[最低竞争对手价格](./lowest-competitor-pricing.md)的价格。</li><li>**[!UICONTROL Match Competitor Price]** — 此选项更改您的Amazon上市价格以根据参数匹配最低价格。 在示例中，Amazon的挂牌价为25美元。</li></ul> |
| [!UICONTROL Apply] | 选项：按百分比核销/按固定金额核销 |
| [!UICONTROL Adjustment Amount] | 用于定义要应用的折扣的百分比或固定金额的数值。 <br>这些选择导致采用最低价格，并将其设置为$0.01以下。 |

### 最低价

| 字段 | 设置 |
|--------------------------------------|---------------------|
| [!UICONTROL Floor Price Source] | 成本= 5美元 |
| [!UICONTROL Floor Price Action] | 增加方式 |
| [!UICONTROL Apply] | 应用为百分比 |
| [!UICONTROL Floor Adjustment Amount] | 5 |

[楼层价格](./floor-price.md)计算=楼层价格Source `$5` x楼层调整金额`5%` = $5.25

应用智能定价规则后，当成本为5美元时，此特定产品的上市价格将低于5.25 USD。
