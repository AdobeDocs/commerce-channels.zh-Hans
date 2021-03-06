---
title: 价格规则示例
description: 为帮助您设计Amazon列表的定价规则，请根据常见情况查看这些示例。
exl-id: 4d9717ba-4ad6-468d-b4ca-99f8620b60b4
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '922'
ht-degree: 2%

---

# 价格规则示例

## 标准价格规则示例

### 放弃后续规则

放弃后续规则是定价规则中的一项强大功能，可阻止多个定价规则堆叠并提供意外的额外折扣。 要放弃后续规则，定价规则必须使用 _[!UICONTROL Priority]_部分 [定价规则常规设置](./pricing-rule-general-settings.md).

如果 **[!UICONTROL Discard Subsequent Rules]** 设置为 `Yes`，则优先级较低（数字较高）的规则不适用于符合条件的产品。

例如，假设有三个定价规则：

| 示例 | 规则名称 | 优先级 | 放弃后续规则 |
|----------|----|----|----|
| 1 | 销售产品优惠10% | 1 | 否 |
| 2 | $2的销售产品 | 2 | 是 |
| 3 | 占所有产品的5% | 3 | 否 |

在此方案中，规#1和#2适用于符合条件的产品。 规则#3仅适用于规则中未包含的符合条#2的产品，因为它的优先级低于示例#2和 **[!UICONTROL Discard Subsequent Rules]** 设置为 `Yes`. 因此，属于销售类别的合格产品将享受10%的折扣，并享受Amazon上市价格的2美元优惠。

### 应用两个标准价格规则

| 字段 | 设置 — 规则1 | 设置 — 规则2 |
|----------|----|----|
| [!UICONTROL Rule Name] | 规则1 | 规则2 |
| [!UICONTROL Priority] | 1 | 2 |
| [!UICONTROL Rule Type] | 标准价格规则 | 标准价格规则 |
| [!UICONTROL Price action] | 减少方式 | 减少方式 |
| [!UICONTROL Apply] | 按百分比应用 | 作为固定金额应用 |
| [!UICONTROL Adjustment Amount] | 10 | 10 |

#### 产品1

价格：US$45.49

应用规则1:45.49美元x(0.9)= 40.94美元

应用规则2:40.94美元 — 10.00美元= 30.94美元

应用规则1和规则2之后的最终价格：US$30.94

#### 产品2

价格：US$47.76

应用规则1:47.76美元x(0.9)= 42.98美元

应用规则2:42.98美元 — 10.00美元= 32.98美元

应用规则1和规则2之后的最终价格：US$32.98

## 智能重定价规则示例

### 具有最低价格来源的Buy Box价格=价格

| 字段 | 设置 |
|----------|----|
| [!UICONTROL Rule Name] | 规则1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | 智能重定价规则 |
| [!UICONTROL Competitor Price Source] | 使用“Buy Box”价格 |
| [!UICONTROL Price Action] | 匹配竞争者价格 |
| [!UICONTROL Floor Price Source] | 价格 |
| [!UICONTROL Floor Price Action] | 匹配 |

#### 产品1

价格：15美元

[Buy Box](./buy-box-competitor-pricing.md) Amazon价格：10美元

因为 [Buy Box](./buy-box-competitor-pricing.md) 价格低于原价，产品按原价上市。

应用规则后的最终价格：15美元

#### 产品2

价格：$5

[Buy Box](./buy-box-competitor-pricing.md) Amazon价格：10美元

因为 [Buy Box](./buy-box-competitor-pricing.md) 价格高于原价，则产品按 [Buy Box](./buy-box-competitor-pricing.md) 价格。

应用规则后的最终价格：10美元

### 具有最低价格来源的Buy Box价格=价格和20%的降价

| 字段 | 设置 |
|----------|----|
| [!UICONTROL Rule Name] | 规则1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | 智能重定价规则 |
| [!UICONTROL Competitor Price Source] | 使用“Buy Box”价格 |
| [!UICONTROL Price Action] | 匹配竞争者价格 |
| [!UICONTROL Floor Price Source] | 价格 |
| [!UICONTROL Floor Price Action] | 减少方式 |
| [!UICONTROL Apply] | 以百分比形式应用 |
| [!UICONTROL Floor Adjustment Amount] | 20 |

#### 产品1

价格：20美元

计算底价：16美元

[Buy Box](./buy-box-competitor-pricing.md) Amazon价格：15美元

因为 [Buy Box](./buy-box-competitor-pricing.md) 价格小于计算价格 [最低价格](./floor-price.md)，则产品将列在 [最低价格](./floor-price.md).

应用规则后的最终价格：16美元

#### 产品2

价格：15美元

已计算 [最低价格](./floor-price.md):12美元

[Buy Box](./buy-box-competitor-pricing.md) Amazon价格：15美元

因为 [Buy Box](./buy-box-competitor-pricing.md) 价格大于已计算 [最低价格](./floor-price.md)，则产品将列在 [Buy Box](./buy-box-competitor-pricing.md) 价格。

应用规则后的最终价格：15美元

#### 产品3

价格：17美元

计算底价：US$13.60

[Buy Box](./buy-box-competitor-pricing.md) Amazon价格：15美元

因为 [Buy Box](./buy-box-competitor-pricing.md) 价格大于已计算 [最低价格](./floor-price.md)，则产品将列在 [Buy Box](./buy-box-competitor-pricing.md) 价格。

应用规则后的最终价格：15美元

### 所有竞争者价格的最低价格和使用所有竞争者的产品条件

| 字段 | 设置 |
|----------|-----|
| [!UICONTROL Rule Name] | 规则1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | 智能重定价规则 |
| [!UICONTROL Competitor Price Source] | 使用最低竞争者价格 |
| [!UICONTROL Minimum Positive Feedback] | 所有竞争者的价格 |
| [!UICONTROL Conditional Variance] | 使用所有竞争者的产品条件 |
| [!UICONTROL Price Action] | 匹配竞争者价格 |
| [!UICONTROL Floor Price Source] | 价格 |
| [!UICONTROL Floor Price Action] | 匹配 |

| 价格 | 条件 |
|----------|----|
| 17美元 | 新建 |
| 15美元 | 新建 |
| 14美元 | 已使用；非常好 |
| 13美元 | 已使用；好 |

#### 产品1

价格：10美元

条件：新建

由于“新条件”的最低竞争者价格为$15，因此产品的标价为$15。

应用规则后的最终价格：15美元

#### 产品2

价格：10美元

条件：已使用；可接受

因为 [最低竞争者价格](./lowest-competitor-pricing.md) 对于“已用”条件为$13，则产品将列为$13。

应用规则后的最终价格：13美元

### 结合最高价格、货币兑换和增值税的智能重定价规则

| 字段 | 设置 |
|----------|-----|
| [!UICONTROL VAT] | 10% |
| [!UICONTROL Ceiling price source] | 10美元 |
| [!UICONTROL Currency conversion] | 1.25欧元：1美元 |

[最高价格](./optional-ceiling-price.md) 在欧洲(VAT)市场中：10美元x 1.25 = 12.50美元

当 [最高价格](./optional-ceiling-price.md) 在欧洲(VAT)市场中，计算并添加VAT。

增值税后最终价格：$12.50 x(1.1)= $13.75

### 组合多个定价规则、最高价格、货币折算和增值税

#### 智能定价规则（来自上一个示例）

| 字段 | 设置 |
|----------|----|
| 优先级 | 1 |
| 增值税 | 10% |
| 最高价格来源 | 10美元 |
| 货币兑换 | 1.25欧元：1美元 |

[最高价格](./optional-ceiling-price.md) 在欧洲(VAT)市场中：10美元x 1.25 = 12.50美元

增值税后最终价格：$12.50 x(1.1)= $13.75

#### 标准定价规则

| 字段 | 设置 |
|----------|-----|
| [!UICONTROL Priority] | 2 |
| [!UICONTROL Price Action] | 增加方式 |
| [!UICONTROL Apply] | 作为固定金额应用 |
| [!UICONTROL Adjustment Amount] | $5.00 |

当 [最高价格](./optional-ceiling-price.md) 命中，则会在智能定价规则的顶部应用标准定价规则。

应用标准定价规则后的最终价格：13.75美元+ 5.00美元= 18.75美元

### 价格调整

在本例中，最具竞争力的价格是通过查看Amazon [竞争对手的最低价格](./lowest-competitor-pricing.md) 有95%的正面反馈，最少有1,000个商家评论。

![价格调整示例](assets/amazon-price-adjustment-example.png)

根据这些参数运行此搜索后，竞争价格可返回25美元。

这里有三种不同 [价格规则操作](./pricing-rule-actions.md) 基于最低价格的选择。

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Price Action] | 选项：<ul><li>**[!UICONTROL Decrease By]**  — 此选项可降低贵公司与 [最低竞争者价格](./lowest-competitor-pricing.md).</li><li>**[!UICONTROL Increase By]**  — 此选项可提高贵公司相对于 [最低竞争者价格](./lowest-competitor-pricing.md).</li><li>**[!UICONTROL Match Competitor Price]**  — 此选项会更改您的Amazon上市价格，以根据参数匹配最低价格。 在本例中，Amazon的上市价格为$25。</li></ul> |
| [!UICONTROL Apply] | 选项：以百分比形式应用/以固定金额应用 |
| [!UICONTROL Adjustment Amount] | 用于定义要应用的折扣的百分比或固定金额的数值。 <br>这些选择会导致获得最低价格，并将其设置为较低$0.01。 |

### 最低价格

| 字段 | 设置 |
|----------|----|
| [!UICONTROL Floor Price Source] | 成本= 5美元 |
| [!UICONTROL Floor Price Action] | 增加方式 |
| [!UICONTROL Apply] | 按百分比应用 |
| [!UICONTROL Floor Adjustment Amount] | 5 |

[最低价格](./floor-price.md) 计算=最低价格来源 `$5` x底调整金额 `5%` = $5.25

应用智能定价规则时，它确实允许此特定产品的上市价格低于$5.25（当成本为$5时）。
