---
title: 上市价格
description: 使用“列表价格”设置可确定您的Amazon列表的价格来源和基本（默认）价格值。
redirect_from: sales-channels/asc/ob-listing-price.html
exl-id: d97d81fa-c298-423f-9072-050ee72e707e
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '1509'
ht-degree: 0%

---

# 上市价格

[!UICONTROL Listing Price] 设置是商店列表设置的一部分。 列表设置可从 [存储仪表板](./amazon-store-dashboard.md).

这些设置定义了 [!DNL Commerce] 定价属性，用作您的价格来源，这是您的Amazon列表的基本（默认）价格值。 这些设置由 [定价规则](./pricing-rule-general-settings.md) ，以自动调整您的Amazon列表价格(相对于 _[!UICONTROL Magento Price Source]_.

您可以配置 [定价范围](./price-scope.md) 作为全球或网站。 如果您的定价范围设置为 `Global`，则所有商店/网站都有一个单一的价格来源。 如果您的定价范围设置为 `Website`，价格来源使用网站价格（如果可用）的回退逻辑，后跟默认（全球）价格。

如果将上市规则设置为应用于多个网站，则网站价格的使用顺序由 [列表规则](./listing-rules.md). 利用这些规则，可定义整个目录的产品定价。 要查看您是否在使用网站价格范围，请参阅 [目录价格范围](https://docs.magento.com/user-guide/catalog/catalog-price-scope.html){target=&quot;_blank&quot;}。

中列出的选项 _[!UICONTROL Magento Price Source]_,_[!UICONTROL Minimum Advertised Price (Map)]_&#x200B;和 _[!UICONTROL Strike Through Price (MSRP)]_包括您配置的定价属性。 定价属性包括 [!DNL Commerce] 将“商店所有者”值的“目录输入类型”设置为 `Price`. 请参阅 [属性输入类型](https://docs.magento.com/user-guide/stores/attributes-input-types.html){target=&quot;_blank&quot;}。

## 配置列表价格设置 {#configure-listing-price-settings}

1. 单击 **[!UICONTROL Listing Settings]** 在商店仪表板上。

1. 展开 _[!UICONTROL Listing Price]_中。

1. 对于 **[!UICONTROL Magento Price Source]** （必需），选择一个选项。

   默认值为 `Price`. 此设置可确定用于Amazon列表的价格源。 如果您创建 [定价规则](./pricing-products.md)，则规则将应用于为此处选择的属性定义的值。 您可以选择任何已配置的定价属性。 但是，如果未为产品填写选定属性，则产品的价格来源将默认回 `Price` 定价规则确定已发布的Amazon上市价格时。

1. 对于**[!UICONTROL Minimum Advertised Price (MAP)**]，选择一个选项。

   默认为无选择。 此设置为产品启用最低广告价格(MAP)。 当您定义定价属性，并且产品的上市价格低于您确定的最低价格（基于您的定价来源和规则）时，此值将成为上市的MAP。 此设置允许您实施 [定价规则](./pricing-products.md)，同时仍控制产品的最低价格。 要防止上市价格过低，请选择要用作MAP的定价属性。 但是，如果未为产品定义选定的定价字段，则不会使用MAP。

1. 对于 **[!UICONTROL Strike Through Price (MSRP)]**，选择一个选项。

   默认为无选择。 此设置确定哪个定价属性用作制造商建议的产品零售价(MSRP)。 如果您的上市价格低于定义的MSRP，则您的Amazon上市将显示MSRP价格的点进，并且上市价格较低，以及计算的“您节省”金额和百分比。 但是，如果未为产品定义所选定价字段，则不计算MSRP。

   >[!NOTE]
   >
   >此设置仅适用于已赢得 [Buy Box](./buy-box-competitor-pricing.md) 位置。 该Buy Box由Amazon授予产品以最佳价格上市的销售者，以及FBA/Prime送货、供货情况和销售者业绩等其他因素。

1. 对于 **应用增值税**，选择选项：

   - `Disabled`  — （默认）选择您不希望将增值税应用于列表价格的时间。

   - `Enabled`  — 选择何时要将增值税应用到清单价格。 增值税通常用作欧洲国家/地区的销售税，并添加到您在Amazon的最终上市价格中。 增值税不适用于智能定价规则内使用的列表的最终价格，除非 [底价](./floor-price.md) 中。
   >[!NOTE]
   >
   >欧盟(EU)的企业需要向企业购买者发送发票，以便客户可以汇税。 您可以自行生成这些发票并计算税金，也可以使用税务计算服务，如Amazon的增值税计算服务。 Amazon建议注册 [Amazon增值税计算服务](https://sell.amazon.co.uk/learn/vat-resources?ref_=asuk_soa_rd&amp;){target=&quot;_blank&quot;}。 如果您选择其他方法，则需负责增值税合规性。>
   >
   >Amazon可能需要10-14天才能验证和激活您的增值税计算服务帐户。

1. 对于 **[!UICONTROL VAT Percentage]**，输入增值税率的值。

   默认值为 `0.00`. 此值用于计算要添加到上市价格的增值税额。 如果 `10.2` 输入，则对您的列表价格应用10.20%的增值税。 将“应用增值税(VAT)”字段设置为 `Disabled`.

1. **（仅限英国商店）** 对于 **[!UICONTROL Amazon Product Tax Code (PTC)]**，选择选项：

   - `Do Not Manage PTC`  — （默认）选择您是使用第三方计税服务，还是已在您的 [!DNL Amazon Seller Central] 帐户。 选择后，Amazon销售渠道不会向您的 [!DNL Amazon Seller Central] 帐户。

   - `Set Default PTC`  — 选择是否具有要用于所有产品的通用产品税码(PTC)。 选择后，您必须完成 _[!UICONTROL Default PTC]_.

      - 对于 **[!UICONTROL Default PTC]**，输入要用于所有符合条件的Amazon列表的默认PTC。 如果在 [!DNL Amazon Seller Central] 帐户，将此字段留空。 对此字段所做的更改不会影响现有的Amazon列表。 要更改现有列表的“默认PTC”(Default PTC)，该列表必须为 [结束](./end-listings-manually.md) 并创建一个新列表。
   >[!NOTE]
   >
   >如果您使用Amazon的增值税计算服务，则必须知道产品的税种。 PTC是Amazon在欧盟为B2B购买的税类ID代码。 请参阅 [Amazon的产品税码](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target=&quot;_blank&quot;}。

1. 对于 **[!UICONTROL Currency Conversion]**，选择一个选项。

   默认值为 `Disabled`. 这些选项取决于您的 [!DNL Commerce] [货币](https://docs.magento.com/user-guide/configuration/general/currency-setup.html){target=&quot;_blank&quot;}设置。 如果没有可用的选项，请设置您的货币设置。

1. 完成后，单击 **[!UICONTROL Save listing settings]**.

![上市价格](assets/amazon-listing-price.png)

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Magento Price Source] | 确定创建Amazon列表时使用的价格源。 默认值为 `Price`. 如果您选择其他属性，例如 `Amazon Price` 或 `Special Price`，则该属性的定义值将用于Amazon列表。 但是，如果未定义选定属性， `Price` 中，将使用。 |
| [!UICONTROL Minimum Advertised Price (MAP)] | 的 [!DNL Commerce] 属性。 选择MAP选项会在上市价格低于MAP价格时，将您的Amazon列表自动设置为MAP价格。 |
| [!UICONTROL Strike Through Price (MSRP)] | 的 [!DNL Commerce] 表示MSRP定价的属性。 如果您的Amazon上市价格低于MSRP，则会显示MSRP价格和上市价格的一次执行。 此设置还用于计算“您保存”金额和百分比，但此功能仅适用于已赢得 [Buy Box](./buy-box-competitor-pricing.md) 位置。 |
| [!UICONTROL Apply Value Added Tax (VAT)] | 增值税由欧盟的销售者使用。<br><br>选择 `Disabled` 如果您不希望将增值税添加到列价。<br><br>选择 `Enabled` 然后，输入增值税百分比，以将增值税应用于列表价格。 |
| [!UICONTROL VAT Percentage] | 定义用于计算要添加到Amazon列表的列价中的增值税金额的百分比。 <br><br>如果输入 `5`，则在应用所有定价规则后，最终上市价格将应用5%的增值税。 增值税不适用于智能定价规则内使用的列表的最终价格，除非 [地板](./floor-price.md) 或 [天花板](./optional-ceiling-price.md) 中。 |
| [!UICONTROL Amazon Product Tax Code (PTC)] | （仅对英国商店显示）确定Amazon销售渠道是否将产品税码信息发送至 [!DNL Amazon Seller Central] 帐户。 <br><br>选择 **不管理PTC** 如果您使用第三方计税服务，或已在您的 [!DNL Amazon Seller Central] 帐户。 当设置为此选项时，Amazon销售渠道不会向您的 [!DNL Amazon Seller Central] 帐户。<br><br>选择 **设置默认PTC** 如果您拥有通用产品税代码，则您希望将其用于所有产品。<br><br>请参阅 [Amazon的产品税码](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target=&quot;_blank&quot;}。 |
| [!UICONTROL Default PTC] | 仅在 **Amazon产品税码(PTC)** 设置为 `Set Default PTC`. 输入将用于所有符合条件的Amazon列表的默认PTC。 如果在 [!DNL Amazon Seller Central] 帐户，将此字段留空。 <br><br>对此字段所做的更改不会影响现有的列表。 列表必须为 [结束](./end-listings-manually.md) 以及为更改生效而创建的新列表。 |
| [!UICONTROL Currency Conversion] | 允许 [!DNL Commerce] storefront默认货币，以准确换算为默认的Amazon货币，以适当的货币发布列表价格。 货币兑换始终基于 [!DNL Commerce] 默认货币。<br><br>您仍可以查看默认 [!DNL Commerce] 和Amazon货币。 如果默认 [!DNL Commerce] 货币与您的默认Amazon货币匹配，并保持禁用“货币兑换”。<br><br>例如，如果 [!DNL Commerce] 默认货币为CAD（加元），Amazon默认货币为USD，您必须启用“货币折换”并选择“折换率CAD为USD”。 提供的选项以内置 [!DNL Commerce] 货币换算。 如果您没有看到要查找的选项， [在中设置货币 [!DNL Commerce]](https://docs.magento.com/user-guide/stores/currency-configuration.html){target=&quot;_blank&quot;}。 |

**快速访问** - [!UICONTROL Listing Settings] 章节

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
