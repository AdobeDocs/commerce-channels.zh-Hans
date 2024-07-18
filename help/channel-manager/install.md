---
title: '安装 [!DNL Channel Manager]'
description: '安装[!DNL Channel Manager]扩展。'
role: Admin, Developer
feature: Sales Channels, Install
exl-id: cb593ebd-f077-4a79-a661-bedf4cc70f97
source-git-commit: 1e74150e6ac88dbabb2e4bbb2fa2f243072eb03f
workflow-type: tm+mt
source-wordcount: '611'
ht-degree: 0%

---


# 安装[!DNL Channel Manager]

查看[要求](onboard.md#requirements)，并收集所需的信息，然后再安装渠道管理器。

## 安装扩展

Channel Manager的安装说明取决于Adobe Commerce或Magento Open Source是部署在本地还是部署在云基础架构上。

- 在[内部部署实例](#install-on-an-on-premises-instance)上安装。

- 在云基础架构实例](#install-adobe-commerce-on-cloud-infrastructure)上的[[!DNL Adobe Commerce] 上安装

这两种方法都需要使用命令行界面(CLI)。

>[!NOTE]
>
>有关使用CLI安装[!DNL Commerce]软件的帮助，请参阅[安装扩展](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html)。

### 在内部部署实例上安装

使用这些说明在Adobe Commerce上安装[!DNL Channel Manager]并Magento Open Source到内部部署实例。

1. 以具有](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/file-system/configure-permissions.html)权限的[用户身份登录到[!DNL Commerce]服务器以写入[!DNL Commerce]文件系统。

1. 将您的网站置于[维护模式](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/maintenance-mode.html)。

   ```bash
   $ bin/magento maintenance:enable
   ```

1. 从[!DNL Commerce]项目根目录中，将渠道管理器添加到`composer.json`。

   ```bash
    composer require magento/channel-manager --no-update
   ```

1. 如果出现提示，请输入[!DNL Commerce]帐户中的访问密钥。

   您的公钥是您的用户名；您的私钥是您的密码。

1. 更新依赖项并安装扩展。

   ```bash
   composer update magento/channel-manager
   ```

   `composer update`命令仅更新[!DNL Channel Manager]所需的依赖项。 要更新所有依赖项，请改用此命令： `composer update`。

1. 等待Composer完成项目依赖关系更新并解决所有错误。

1. 验证模块安装：

   - 检查模块状态。

     ```bash
     bin/magento module:status Magento_SalesChannels
     ```

     示例响应：

     ```
     Module is enabled
     ```

   - 如果未启用该模块，请启用该模块。

   ```bash
   bin/magento module:enable Magento_SalesChannels
   ```

1. 注册扩展。

   ```bash
   bin/magento setup:upgrade
   ```

1. 如果出现提示，请重新编译您的[!DNL Commerce]项目。

   ```bash
   bin/magento setup:di:compile
   ```

1. 清理缓存。

   ```bash
   bin/magento cache:clean
   ```

1. 禁用维护模式。

   ```bash
   bin/magento maintenance:disable
   ```

### 在云基础架构实例上的Adobe Commerce上安装

向云实例添加扩展时，请在开发分支中工作。

有关使用分支的帮助，请参阅&#x200B;_Commerce on Cloud Infrastructure指南_&#x200B;中的[开始创建分支](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/cli-branches.html)。

在安装期间，扩展名(`magento\channel-manager`)会自动插入到[app/etc/config.php](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/store-settings.html)文件中。 您无需直接编辑文件。

1. 在本地工作站上，更改为云项目根目录。

1. 创建或签出开发[分支](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/cli-branches.html)。

1. 使用编辑器名称，将扩展名添加到`composer.json`文件的`require`部分。

   ```bash
   composer require magento/module-sales-channels-extension --no-update
   ```

1. 更新依赖项并安装扩展。

   ```bash
   composer update magento/module-sales-channels-extension
   ```

   `composer update`命令仅更新[!DNL Channel Manager]所需的依赖项。 要更新所有依赖项，请改用此命令： `composer update`。

1. 添加、提交和推送代码更改 — 包含对`composer.lock`和`composer.json`文件的更改。

   ```bash
   $ git add -A
   ```

   ```bash
   $ git commit -m "Install channel manager extension" 
   ```

   ```bash
   $ git push origin <branch-name>
   ```

1. 构建和部署过程完成后，使用SSH登录到远程环境并验证扩展是否已正确安装。

```bash
   bin/magento module:status Magento_SalesChannels
```

示例响应：

```
Module is enabled
```

如果禁用该模块，请[在本地环境中启用它](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/extensions.html)并部署更改。


1. 成功安装扩展后，登录到[!UICONTROL Admin]以[配置Commerce服务连接器](connect.md)。

   >[!NOTE]
   >
   >有关将渠道管理器更新为新版本的说明，请参阅[升级模块和扩展](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html)。


## 故障排除

使用以下信息可解决Channel Manager安装过程中发生的错误。

### 不正确的编辑器键

如果用于对Composer存储库进行身份验证的[访问密钥](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html)无效，或者未链接到用于注册[!DNL Channel Manager]服务的[!DNL MAGE ID]，则显示以下错误。

```
Could not find a matching version of package magento/channel-manager. Check the package spelling, your version constraint and that the package is available in a stability which matches your minimum-stability (stable).
```

检查密钥配置：

1. 查找`auth.json`文件的位置：

   ```bash
   $ composer config –global home
   ```

1. 查看`auth.json`文件。

   ```bash
   $ cat /path/to/auth.json
   ```

1. 验证auth.json中的凭据是否与用于注册渠道管理器服务的MAGE ID](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html)关联的[密钥匹配。

### PHP内存不足

如果系统没有为PHP分配足够的内存，则显示以下错误。

```
Fatal error: Allowed memory size of 2146435072 bytes exhausted (tried to allocate 4096 bytes) in phar:///usr/local/bin/composer/src/Composer/DependencyResolver/RuleWatchGraph.php on line 52
```

使用以下任一方法解决内存问题：

- [增加环境`php.ini`文件中PHP](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/app/php-settings.html)的内存限制。 此外，请验证Commerce实例是否具有其他PHP设置的[推荐值](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html)。

- 从命令行指定内存限制。

  ```bash
  $ php -d memory_limit=-1 \[path to composer]/composer require magento/payment-services.
  ```

  例如：

  ```bash
  $ php-d memory_limit=-1 vendor/bin/composer require magento/channel-manager
  ```

### 缺少视图

如果在安装渠道管理器期间收到有关缺少`process_catalog_exporter_view`的错误，请尝试[刷新索引器](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/manage-indexers.html)。

```bash
php bin/magento indexer:refresh
```

### 云部署错误

有关将扩展部署到云中的问题，请参阅[扩展部署失败](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/deploy/recover-failed-deployment.html)。
