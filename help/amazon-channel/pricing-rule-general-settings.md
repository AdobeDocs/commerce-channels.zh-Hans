---
title: 定价规则常规设置
description: 使用价格规则常规设置定义上市价格规则的主要特征。
redirect_from: /sales-channels/asc/ob-pricing-rules-general-settings.html
exl-id: 915b3eed-997e-4f94-a23f-0553a9dfe30c
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 0%

---

# 定价规则常规设置

定义规则的名称、描述、活动日期和优先级。

## 完成价格规则常规设置部分

1. 对于 **[!UICONTROL Rule Name]** （必需），输入规则的名称。

   此名称仅用于内部标识。 规则名称描述性越强，越好。

1. 对于 **[!UICONTROL Description]**，输入规则的详细描述。

   此描述可能包括有关符合条件的产品、有效日期、调整价格的计算公式的信息，或者您希望修改规则时发现有用的任何其他信息。

1. 对于 **[!UICONTROL Status]**，选择选项：

   - `Active`  — 如果您希望将定价规则应用于您的合格产品并调整列表定价，然后再发布到Amazon，请选择此选项。

   - `Inactive`  — 当您不希望将定价规则应用于您的合格产品时，请选择此选项。 在修改定价规则或在进行有限促销后将其关闭时，很可能会使用此选项。

1. 对于 **[!UICONTROL From]** 和 **[!UICONTROL To]**，为定价规则输入开始和结束日期。

   您还可以单击日历图标从动态日历中选择日期。 当设置具有确定开始和结束日期的有限时间或季节性促销活动时，此自动开始和停止选项非常有用。

1. 对于 **[!UICONTROL Priority]**，输入规则优先级的数值。

   优先级值等于 `1` 是最高优先级。 当您有多个有效定价规则时，您可以使用此优先级值来确定首先应用哪个规则。 此字段是使用 _[!UICONTROL Discard Subsequent Rules]_功能。

1. 对于 **[!UICONTROL Discard Subsequent Rules]**，选择选项：

   - `Yes`  — 当您不希望应用任何适用于产品的其他定价规则时，请选择此选项。 放弃后续规则意味着，如果多个定价规则应用于同一产品，则只有具有最高定义优先级值的定价规则才会应用于该产品。 此选项可防止多个定价规则堆叠并提供意外的额外折扣。

   - `No`  — 如果要允许将多个定价规则应用于同一产品，请选择此选项。 此选项可导致堆叠并提供要应用的多种折扣。

>[!NOTE]
>
>要放弃后续规则，定价规则必须具有定义 **优先级** 值。

![定价规则常规设置](assets/amazon-pricing-rule-general.png)

| 字段 | 描述 |
|---|---|
| [!UICONTROL Rule Name] | （必需）输入规则的名称，用于内部标识。 规则名称描述性越强，越好。 例如，“年末图书销售优惠25%”。 |
| [!UICONTROL Description] | 输入详细说明规则（也用于内部目的）的说明。 例如，“年终销售，图书类别中所有物品的折扣为25%”。 |
| [!UICONTROL Status] | 选项：<ul><li>**[!UICONTROL Inactive]**  — 定价规则不适用于您的列表。 在修改定价规则或在进行有限促销后将其关闭时，可能会使用此选项。</li><li>**[!UICONTROL Active]**  — 定价规则适用于您的列表，并在发布到Amazon之前调整您的列表定价。</li></ul> |
| [!UICONTROL From] | 输入定价规则开始的开始日期。 例如，要在一年的最后一个月进行销售，您需要将 `From` 日期至12月1日，以便定价规则自动适用于从12月1日开始的Amazon列表。 |
| [!UICONTROL To] | 输入定价规则结束的结束日期。 继续上一个示例，要将销售限制为一年的最后一个月，您应将 `To` 日期为12月31日，因此定价规则将在12月31日过期。 |
| [!UICONTROL Priority] | 输入定价规则优先级的值。 优先级值等于 `1` 是最高优先级。 当您有多个定价规则时，可以使用优先级值来确定首先应用哪个规则。 此字段是使用 **放弃后续规则** 功能。 |
| [!UICONTROL Discard Subsequent Rules] | 用于允许或阻止多个定价规则堆叠并提供额外折扣。 要放弃后续规则，定价规则必须为 **[!UICONTROL Priority]**. 选项：<ul><li>**[!UICONTROL Yes]**  — 选择您不希望应用任何适用于产品的其他定价规则的时间。 放弃后续规则意味着当多个定价规则应用于同一产品时，只应用具有最高定义优先级值的定价规则。</li><li>**[!UICONTROL No]**  — 选择您希望何时允许将多个定价规则应用于同一产品。 此选项可能导致对您的列表价格应用堆叠和多次折扣。</li></ul> |
