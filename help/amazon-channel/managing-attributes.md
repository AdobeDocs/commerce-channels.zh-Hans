---
title: 管理Amazon列表的属性
description: 您可以管理Commerce产品属性到Amazon属性的映射，以确保系统之间的产品信息准确无误。
exl-id: 6f9ded2d-292e-4b7e-8c10-48f478a4383e
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 0%

---

# 管理Amazon列表的属性

Amazon和 [!DNL Commerce] 两者都使用用于定义产品的产品属性系统（称为属性）。 属性定义了产品的描述、内容、图像、价格和各种数据。

Commerce和Amazon之间的成功通信需要 [!DNL Commerce] 可以将属性正确映射（或匹配）到相应的Amazon属性。 与Amazon集成时，您可以将这些属性映射到Amazon属性。 完成后， [!DNL Commerce] 可以将您的Amazon列表与您的网站进行同步和维护。 [!DNL Commerce] 产品目录。

例如，假设您的文件夹中存在相同的项目， [!DNL Commerce] 目录和Amazon列表。 产品的一个属性可能是物料的列表价格。 中的挂牌价名称 [!DNL Commerce] 可能被命名为 `Price`，而Amazon的挂牌价可命名为 `ListingPrice`. 您必须指示 [!DNL Commerce] 在与Amazon通信时， [!DNL Commerce] 已命名的属性 `Price` 与名为的Amazon属性相同 `ListingPrice`. 此过程称为 _管理属性_，包括创建新属性和编辑现有属性。 确保属性正确匹配可确保之间正确通信 [!DNL Commerce] 和Amazon。

设置属性映射时， [!DNL Commerce] 可以与Amazon来回传递产品信息。 如果您有Amazon产品列表， [!DNL Commerce] 可以将您的Amazon产品和详细信息导入 [!DNL Commerce] 目录，允许您从单个集中的产品目录管理Amazon列表。

Amazon sales channel允许您根据需要访问、查看、创建和管理属性，这些属性位于 [_[!UICONTROL Attributes]_视图](./attributes-view.md) 在Amazon sales channel主页上。 如果将属性添加到 [!DNL Commerce] 目录中，可能需要更新所有产品中的这些值。

有关详情，请参阅 [!DNL Commerce] 和Amazon属性集和值，请参见：

- [管理属性基础知识](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html)
- [创建属性](./creating-attributes.md#create-an-attribute)
- [编辑现有属性](./creating-attributes.md#edit-an-attribute)
- [查看属性映射](./amazon-matching-attributes-values.md)
- [编辑或创建属性映射](./amazon-manually-update-incomplete-listing.md)
