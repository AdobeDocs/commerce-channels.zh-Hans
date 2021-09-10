---
title: 价格规则操作
description: 使用价格规则活动定义应用于价格源的调整计算，以确定Amazon上市价格。
redirect_from: /sales-channels/asc/ob-pricing-rules-actions.html: 
exl-id: c46bd5c2-7994-45b4-ae0c-9e473372c73a
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: 211
ht-degree: 0%

---

# 价格规则操作

价格规则活动定义应用于价格来源以确定上市价格的调整计算。

## 标准价格规则

[标准价格规则](./standard-price-rules.md)允许您相对于[!DNL Commerce]目录价格（或价格来源），将Amazon列表价格增加或减少特定百分比或固定美元金额。

| 区域 | 描述 |
|--- |--- |
| [[!UICONTROL Select Rule Type]](./standard-price-rules.md) | 将规则类型设置为`Standard price rule`。 |
| [[!UICONTROL Price Adjustment]](./standard-price-rules.md) | 定义应用于价格来源以确定上市价格的调整计算 |

## 智能重定价规则

[智能重定价规则](./intelligent-repricing-rules.md)使用Amazon竞争者的定价来确定您的上市价格。 竞争对手是列出您在Amazon上列出的相同产品的其他销售商。

| 区域 | 描述 |
|--- |--- |
| [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md) | 将规则类型设置为`Intelligent repricing rule`，并同时设置竞争者价格来源和反馈要求。 |
| [[!UICONTROL Competitor Conditional Variances]](./competitor-conditional-variances.md) | 定义竞争对手销售的相同产品的条件差异。 |
| [[!UICONTROL Price Adjustment]](./price-adjustment.md) | 定义应用于价格来源以确定上市价格的调整计算 |
| [[!UICONTROL Floor Price]](./floor-price.md) | 定义产品的最低价格，以防止多个定价规则将上市价格设置得过低。 |
| [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md) | 为产品定义最高价格，以确保定价保持竞争力。 |
