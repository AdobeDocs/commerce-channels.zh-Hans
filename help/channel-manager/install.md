---
title: 安装 [!DNL Channel Manager]
description: 安装Channel Manager扩展。
exl-id: cb593ebd-f077-4a79-a661-bedf4cc70f97
source-git-commit: 50c5a3b5987f0e5227d9c4f4999caab8bf6b3fd8
workflow-type: tm+mt
source-wordcount: '701'
ht-degree: 0%

---

# 安装渠道管理器

查看 [先决条件](onboard.md#prerequisites) 并在安装“渠道管理器”之前收集所需信息。

## 更新最小稳定性设置

在安装扩展之前，请更新 `minimum-stability` 您的 `composer.json` 文件，以便您可以使用编辑器安装早期版本的渠道管理器。

要更新配置，请将以下行添加到 `composer.json` 文件。

```json
{
   "minimum-stability": "alpha",
   "prefer-stable": true
}
```

## 安装扩展

Channel Manager的安装说明取决于Adobe Commerce或Magento Open Source是部署在本地还是云基础架构上。

- 在 [本地实例](#install-on-an-on-premises-instance).

- 在 [[!DNL Adobe Commerce] 云基础架构实例](#install-adobe-commerce-on-cloud-infrastructure)

这两种方法都要求您使用命令行界面(CLI)。

>[!NOTE]
>
>如需有关安装的帮助 [!DNL Commerce] 使用CLI的软件，请参阅 [常规CLI安装](https://devdocs.magento.com/extensions/install/){target=&quot;_blank&quot;}。

### 在本地实例上安装

请按照以下说明在Adobe Commerce和Magento Open Source平台上安装。

1. 登录到 [!DNL Commerce] 服务器as a [具有权限的用户](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/file-system-perms.html){target=&quot;_blank&quot;}写入 [!DNL Commerce] 文件系统。

1. 将您的网站放入 [维护模式](https://devdocs.magento.com/guides/v2.4/install-gde/install/cli/install-cli-subcommands-maint.html){target=&quot;_blank&quot;}。

   ```bash
   $ bin/magento maintenance:enable
   ```

1. 从 [!DNL Commerce] 项目根目录，将渠道管理器添加到 `composer.json`.

   ```bash
    $ composer require magento/channel-manager --no-update
   ```

1. 如果出现提示，请输入 [!DNL Commerce] 帐户。

   您的公钥是您的用户名；您的私钥是您的密码。

1. 更新依赖项并安装扩展。

   ```bash
   $ composer update
   ```

   的 `composer update` 命令会更新所有依赖项。 要仅更新与“渠道管理器”相关的依赖项，请改用以下命令： `composer update magento/channel-manager`.

1. 等待编辑器完成更新项目依赖项并解决任何错误。

1. 验证安装

   ```bash
   $ bin/magento module:status channel-manager
   ```

   示例响应：

   ```terminal
   Module is disabled
   ```

1. 注册扩展。

   ```bash
   $ bin/magento setup:upgrade
   ```

1. 如果出现提示，请重新编译 [!DNL Commerce] 项目。

   ```bash
   $ bin/magento setup:di:compile
   ```

1. 验证扩展是否已启用：

   ```bash
   $ bin/magento module:status channel-manager
   ```

   示例响应：

   ```bash
   Module is enabled
   ```

1. 清除缓存。

   ```bash
   $ bin/magento cache:clean
   ```

1. 禁用维护模式。

   ```bash
    $ bin/magento maintenance:disable
   ```

### 在云基础架构实例上的Adobe Commerce上安装

向云实例添加扩展时，请在开发分支中工作。

有关使用分支的帮助，请参阅 [开始创建分支](https://devdocs.magento.com/cloud/env/environments-start.html#getstarted)Adobe Commerce开发人员文档中的{target=&quot;_blank&quot;}。

在安装过程中，扩展名称(`&lt;VendorName>\_&lt;ComponentName>`)会自动插入到 [app/etc/config.php](https://devdocs-beta.magento.com/guides/v2.3/config-guide/config/config-php.html){target=&quot;_blank&quot;}文件。 您无需直接编辑文件。

1. 在您的本地工作站上，更改为云项目根目录。

1. 创建或签出开发 [分支](https://devdocs-beta.magento.com/cloud/env/environments-start.html#getstarted){target=&quot;_blank&quot;}。

1. 使用编辑器名称，将扩展添加到 `require` 部分 `composer.json` 文件。

   ```bash
   $ composer require magento/channel-manager --no-update
   ```

1. 更新项目依赖项。

   ```bash
   $ composer update
   ```

1. 添加、提交和推送代码更改 — 包括对 `composer.lock` 和 `composer.json` 文件。

   ```bash
   $ git add -A
   ```

   ```bash
   $ git commit -m “Install channel manager extension” 
   ```

   ```bash
   $ git push origin <branch-name>
   ```

1. 构建和部署完成后，使用SSH登录到远程环境，并验证扩展是否正确安装。

   ```bash
   $ bin/magento module:status channel-manager
   ```

   示例响应：

   ```terminal
   Module is enabled
   ```

1. 安装成功后，登录到 [!UICONTROL Admin] to [配置Commerce Services Connector](connect.md).

   >[!NOTE]
   >
   >有关将Channel Manager更新到新版本的说明，请参阅 [升级模块和扩展](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html){target=&quot;_blank&quot;}。


## 疑难解答

使用以下信息可解决在Channel Manager安装过程中发生的错误。

### 编辑器键不正确

如果 [访问密钥](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/connect-auth.html)用于对编辑器存储库进行身份验证的{target=&quot;_blank&quot;}无效，或未链接到 [!DNL MAGE ID] 用来注册 [!DNL Channel Manager] 服务时，将显示以下错误。

```terminal
Could not find a matching version of package magento/channel-manager. Check the package spelling, your version constraint and that the package is available in a stability which matches your minimum-stability (stable).
```

检查密钥配置：

1. 查找 `auth.json` 文件：

   ```bash
   $ composer config –global home
   ```

1. 查看 `auth.json` 文件。

   ```bash
   $ cat /path/to/auth.json
   ```

1. 验证auth.json中的凭据是否与 [与图像ID关联的键](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/connect-auth.html){target=&quot;_blank&quot;}用于注册Channel Manager服务。

### 内存不足，PHP

如果系统没有为PHP分配足够的内存，则会显示以下错误。

```terminal
Fatal error: Allowed memory size of 2146435072 bytes exhausted (tried to allocate 4096 bytes) in phar:///usr/local/bin/composer/src/Composer/DependencyResolver/RuleWatchGraph.php on line 52
```

使用以下任一方法解决内存问题：

- [提高PHP的内存限制](https://devdocs.magento.com/cloud/project/magento-app-php-ini.html#increase-php-memory-limit)环境中的{target=&quot;_blank&quot;} `php.ini` 文件。 此外，验证商务实例是否具有 [推荐值](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/php-settings.html){target=&quot;_blank&quot;}，用于其他PHP设置。

- 从命令行中指定内存限制。

   ```bash
   $ php -d memory_limit=-1 \[path to composer]/composer require magento/payment-services.
   ```

   例如：

   ```bash
   $ php-d memory_limit=-1 vendor/bin/composer require magento/channel-manager
   ```

### 缺少视图

如果您收到有关缺失的错误 `process_catalog_exporter_view` 在“Channel Manager（渠道管理器）”安装过程中，尝试 [刷新索引器](https://devdocs.magento.com/guides/v2.4/config-guide/cli/config-cli-subcommands-index.html#config-cli-subcommands-index-reindex){target=&quot;_blank&quot;}。

```bash
php bin/magento indexer:refresh
```

### 云部署错误

有关将扩展部署到云的问题，请参阅 [扩展部署失败](https://devdocs.magento.com/cloud/trouble/trouble_comp-deploy-fail.html){target=&quot;_blank&quot;}。
