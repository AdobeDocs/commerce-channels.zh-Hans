---
title: Amazon销售渠道 —  [!UICONTROL Listing Price]
description: 使用“列表价格”设置确定Amazon列表的价格来源和基本（默认）价格值。
redirect_from: sales-channels/asc/ob-listing-price.html
exl-id: d97d81fa-c298-423f-9072-050ee72e707e
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '1503'
ht-degree: 0%

---

# [!UICONTROL Listing Price]

[!UICONTROL Listing Price] 设置是商店列表设置的一部分。 列表设置可从以下位置访问： [存储仪表板](./amazon-store-dashboard.md).

这些设置定义 [!DNL Commerce] 用作价格来源的定价属性，价格来源是您的Amazon列表的基底（默认）价格值。 这些设置由您的 [定价规则](./pricing-rule-general-settings.md) 自动调整相对于值集的Amazon挂牌价 _[!UICONTROL Magento Price Source]_.

您可以配置 [定价范围](./price-scope.md) 作为全球或网站。 如果将定价范围设置为 `Global`，您的所有商店/网站只有一个价格来源。 如果将定价范围设置为 `Website`，价格来源使用网站价格的回退逻辑（如果可用），后跟默认（全局）价格。

如果上市规则设为适用于多个网站，则网站价格的使用顺序由 [列表规则](./listing-rules.md). 这些规则允许您跨目录定义产品定价。 要查看您是否使用网站价格范围，请参阅 [目录价格范围](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/catalog-price-scope.html).

中列出的选项 _[!UICONTROL Magento Price Source]_，_[!UICONTROL Minimum Advertised Price (Map)]_、和 _[!UICONTROL Strike Through Price (MSRP)]_包括您配置的定价属性。 定价属性为 [!DNL Commerce] “商店所有者”值设置为的目录输入类型的产品属性 `Price`. 参见 [属性输入类型](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/attributes-input-types.html).

## 配置列表价格设置 {#configure-listing-price-settings}

1. 单击 **[!UICONTROL Listing Settings]** 在商店仪表板上。

1. 展开 _[!UICONTROL Listing Price]_部分。

1. 对象 **[!UICONTROL Magento Price Source]** （必需），选择一个选项。

   默认为 `Price`. 此设置确定用于Amazon清单的价格来源。 如果您创建 [定价规则](./pricing-products.md)，则规则将应用于为此处选择的属性定义的值。 您可以选择任何已配置的定价属性。 但是，如果没有为产品填写选定属性，则产品的价格来源将默认返回到 `Price` 时，确定已发布的Amazon上市价格。

1. 对于**[!UICONTROL Minimum Advertised Price (MAP)**]，选择一个选项。

   默认选项为无选项。 此设置允许产品的最低广告价格(MAP)。 当您定义定价属性并且产品的上市价格低于您确定的最低价格（根据定价来源和规则）时，此值将成为上市的MAP。 此设置允许您实施 [定价规则](./pricing-products.md)，同时仍控制产品的最低价格。 要防止挂牌价过低，请选择一个要用作MAP的定价属性。 但是，如果没有为产品定义选定的定价字段，则不会使用MAP。

1. 对象 **[!UICONTROL Strike Through Price (MSRP)]**，选择一个选项。

   默认选项为无选项。 此设置确定将哪个定价属性用作产品的制造商建议零售价(MSRP)。 如果您的上市价格低于定义的MSRP，则显示您的Amazon上市时，会以较低上市价格的MSRP价格删除线，以及计算的“您保存”金额和百分比。 但是，如果没有为产品定义选定的定价字段，则不会计算MSRP。

   >[!NOTE]
   >
   >此设置仅适用于已获得 [Buy Box](./buy-box-competitor-pricing.md) 位置。 Buy Box由Amazon授予销售者，销售者通常以最佳价格列出产品，同时考虑其他因素，例如提供的FBA/Prime运费、可用性和销售者的表现。

1. 对象 **应用增值税(VAT)**，选择一个选项：

   - `Disabled`  — （默认）选择您不希望向上市价格应用增值税的时间。

   - `Enabled`  — 选择您何时要将增值税应用于您的列表价格。 在欧洲国家/地区，VAT通常用作销售税，并添加到Amazon中的最终定价。 VAT不适用于智能定价规则中使用的列表的最终价格，除非 [底价](./floor-price.md) 点击。
   >[!NOTE]
   >
   >欧盟(EU)企业需要将发票发送给商业采购员，以便客户可以汇款。 您可以自行生成这些发票并计算税款，也可以使用计税服务(如Amazon的增值税计算服务)。 Amazon建议注册 [Amazon增值税计算服务](https://sell.amazon.co.uk/learn/vat-resources?ref_=asuk_soa_rd&amp;). 如果选择其他方法，则由您负责符合VAT规定。>
   >
   >Amazon可能需要10-14天才能验证并激活您的增值税计算服务帐户。

1. 对象 **[!UICONTROL VAT Percentage]**&#x200B;中，输入增值税率的值。

   默认为 `0.00`. 此值用于计算要添加到列表价格的增值税金额。 如果 `10.2` 在输入时，您输入的标价需缴纳10.20%的增值税。 当“应用增值税(VAT)”字段设置为时，此字段被禁用 `Disabled`.

1. **（仅限英国商店）** 对象 **[!UICONTROL Amazon Product Tax Code (PTC)]**，选择一个选项：

   - `Do Not Manage PTC`  — （默认）选择是使用第三方计税服务还是已经在 [!DNL Amazon Seller Central] 帐户。 选中后，Amazon销售渠道不会向您的发送产品税码信息 [!DNL Amazon Seller Central] 帐户。

   - `Set Default PTC`  — 选择您是否希望对所有产品使用通用产品税码(PTC)。 选择后，您必须完成 _[!UICONTROL Default PTC]_.

      - 对象 **[!UICONTROL Default PTC]**，输入用于所有符合条件的Amazon列表的默认PTC。 如果默认PTC是在 [!DNL Amazon Seller Central] 帐户，将此字段留空。 对此字段所做的更改不会影响现有Amazon列表。 要更改现有列表的“默认PTC”，该列表必须是 [已结束](./end-listings-manually.md) 并创建了一个新列表。
   >[!NOTE]
   >
   >如果您使用Amazon的增值税计算服务，则必须知道您产品的税种。 PTC是Amazon在欧盟购买B2B的税类ID代码。 参见 [Amazon的产品税码](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target="_blank"}.

1. 对象 **[!UICONTROL Currency Conversion]**，选择一个选项。

   默认为 `Disabled`. 这些选项取决于 [!DNL Commerce] [货币](https://experienceleague.adobe.com/docs/commerce-admin/config/general/currency-setup.html) 设置。 如果没有可用选项，请设置您的货币设置。

1. 完成后，单击 **[!UICONTROL Save listing settings]**.

![挂牌价](assets/amazon-listing-price.png){width="500" zoomable="yes"}

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Magento Price Source] | 确定在创建Amazon列表时使用的价格来源。 默认为 `Price`. 如果您选择其他属性，例如 `Amazon Price` 或 `Special Price`，属性的定义值用于您的Amazon列表。 但是，如果所选属性未定义， `Price` 已使用。 |
| [!UICONTROL Minimum Advertised Price (MAP)] | 此 [!DNL Commerce] MAP定价的属性。 如果选择MAP选项，则在上市价格低于MAP价格时，您的Amazon上市会自动设置为MAP价格。 |
| [!UICONTROL Strike Through Price (MSRP)] | 此 [!DNL Commerce] 表示MSRP定价的属性。 如果您的Amazon上市价格低于MSRP，则会显示MSRP价格和上市价格的删除线。 此设置还用于计算“您保存”的金额和百分比，但此功能仅适用于已获得 [Buy Box](./buy-box-competitor-pricing.md) 位置。 |
| [!UICONTROL Apply Value Added Tax (VAT)] | 增值税由欧盟的卖方使用。<br><br>选择 `Disabled` 如果您不希望将增值税添加到列表价格中。<br><br>选择 `Enabled` 然后，输入用于根据列表价格应用增值税的增值税百分比。 |
| [!UICONTROL VAT Percentage] | 定义用于计算要添加到Amazon列表价中的增值税税额的百分比。 <br><br>如果您输入 `5`，则在应用所有定价规则后，最终上市价格将收取5%的增值税。 增值税不适用于在智能定价规则中使用的列表的最终价格，除非 [floor](./floor-price.md) 或 [上限](./optional-ceiling-price.md) 点击。 |
| [!UICONTROL Amazon Product Tax Code (PTC)] | （仅针对英国商店显示）确定Amazon销售渠道是否将产品税码信息发送给您的 [!DNL Amazon Seller Central] 帐户。 <br><br>选择 **不管理PTC** 如果您使用第三方计税服务或已在以下项目中设置所有计税服务： [!DNL Amazon Seller Central] 帐户。 当设置为此选项时，Amazon销售渠道不会将产品税码信息发送给您的 [!DNL Amazon Seller Central] 帐户。<br><br>选择 **设置默认PTC** 如果您有通用产品税码，那么您要将其用于所有产品。<br><br>参见 [Amazon的产品税码](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target="_blank"}. |
| [!UICONTROL Default PTC] | 仅出现于 **Amazon产品税码(PTC)** 设置为 `Set Default PTC`. 输入用于所有符合条件的Amazon列表的默认PTC。 如果默认PTC是在 [!DNL Amazon Seller Central] 帐户，将此字段留空。 <br><br>对此字段所做的更改不会影响现有列表。 列表必须为 [已结束](./end-listings-manually.md) 以及为更改生效而创建的新列表。 |
| [!UICONTROL Currency Conversion] | 允许您的 [!DNL Commerce] storefront默认货币，以便准确地转换为您的默认Amazon货币，从而以适当的货币发布您的挂牌价格。 货币兑换始终基于 [!DNL Commerce] 默认货币。<br><br>您仍然可以查看默认值 [!DNL Commerce] 和Amazon货币。 如果您的默认 [!DNL Commerce] 货币与您的默认Amazon货币匹配，请将“货币换算”保留为禁用。<br><br>例如，如果您的 [!DNL Commerce] 默认货币为CAD（加元），而Amazon的默认货币为USD，您必须启用“货币换算”并选择“兑换率CAD至USD”。 提供的选项基于内置 [!DNL Commerce] 货币换算。 如果您看不到正在查找的选项， [在中设置货币 [!DNL Commerce]](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/currency/currency-configuration.html). |

**快速访问** - [!UICONTROL Listing Settings] 区域

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
