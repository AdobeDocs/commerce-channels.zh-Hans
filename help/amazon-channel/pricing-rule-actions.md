---
title: Amazon sales channel — 价格规则操作
description: 使用价格规则操作可定义应用于价格来源的调整计算，以确定Amazon的上市价格。
feature: Sales Channels, Price Rules
exl-id: c46bd5c2-7994-45b4-ae0c-9e473372c73a
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---

# 价格规则操作

价格规则活动定义应用于价格来源的调整计算，以确定上市价格。

## 标准价格规则

A [标准价格规则](./standard-price-rules.md) 允许您按特定百分比或相对于以下项的固定美元金额增加或减少Amazon上市价格： [!DNL Commerce] 目录价格（或价格来源）。

| 部分 | 描述 |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [[!UICONTROL Select Rule Type]](./standard-price-rules.md) | 将规则类型设置为 `Standard price rule`. |
| [[!UICONTROL Price Adjustment]](./standard-price-rules.md) | 定义应用于价格来源的调整计算，以确定上市价格 |

## 智能重新定价规则

An [智能重新定价规则](./intelligent-repricing-rules.md) 使用Amazon竞争对手的定价来确定您的上市价格。 竞争对手是其他销售商，与您在Amazon上列出的产品相同。

| 部分 | 描述 |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md) | 将规则类型设置为 `Intelligent repricing rule` 以及您的竞争对手价格来源和反馈要求。 |
| [[!UICONTROL Competitor Conditional Variances]](./competitor-conditional-variances.md) | 定义竞争对手销售的相同产品的条件的差异。 |
| [[!UICONTROL Price Adjustment]](./price-adjustment.md) | 定义应用于价格来源的调整计算，以确定上市价格 |
| [[!UICONTROL Floor Price]](./floor-price.md) | 定义产品的最低价格，以防止多个定价规则将挂牌价格设置得过低。 |
| [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md) | 定义产品的最高价格，以确保您的定价具有竞争力。 |
