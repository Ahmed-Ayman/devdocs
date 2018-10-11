---
group: installation-guide
title: Magento 2.3.x technology stack requirements
functional_areas:
  - Install
  - System
  - Setup
---

### Operating systems (Linux x86-64)

<<<<<<< HEAD
Linux distributions such as RedHat Enterprise Linux (RHEL), CentOS, Ubuntu, Debian, and so on.
=======
Linux distributions, such as RedHat Enterprise Linux (RHEL), CentOS, Ubuntu, Debian, and similar.
>>>>>>> 2.3.0-beta

### Memory requirement

Upgrading the Magento applications and extensions you obtain from Magento Marketplaces and other sources can require up to 2GB of RAM. If you are using a system with less than 2GB of RAM, we recommend you create a [swap file]({{ page.baseurl }}/comp-mgr/trouble/cman/out-of-memory.html); otherwise, your upgrade might fail.

### Composer (latest stable version)
{% glossarytooltip d85e2d0a-221f-4d03-aa43-0cda9f50809e %}Composer{% endglossarytooltip %} is required for developers who wish to contribute to the Magento 2 codebase or anyone who wishes to develop Magento extensions.

### Web servers
<<<<<<< HEAD

||||||| merged common ancestors
=======
<<<<<<< HEAD

*	<a href="http://httpd.apache.org/download.cgi" target="&#95;blank">Apache 2.2 or 2.4</a>
=======
>>>>>>> d5d623cb5417027e016a6a61e5689de46ee6e31b
*	[Apache 2.2 or 2.4](http://httpd.apache.org/download.cgi)
>>>>>>> 2.3.0-beta

	In addition, you must enable the Apache `mod_rewrite` and `mod_version` modules. The [`mod_rewrite`](https://httpd.apache.org/docs/2.4/mod/mod_rewrite.html) module enables the server to perform URL rewriting. The [`mod_version`](https://httpd.apache.org/docs/2.4/mod/mod_version.html) module provides flexible version checking for different `httpd` versions. For more information, see [our Apache documentation]({{page.baseurl}}/install-gde/prereq/apache.html).

*	[nginx 1.x](https://nginx.org/en/download.html)

### Database

MySQL 5.6, 5.7

Magento is also compatible with MySQL NDB Cluster 7.4.&#42;, MariaDB 10.0, 10.1, 10.2, Percona 5.7, and other binary-compatible MySQL technologies.

{:.bs-callout .bs-callout-info}
Magento only uses MySQL features compatible with MariaDB. MariaDB may not be compatible with all MySQL features, however, so be sure to research compatibility issues before using a feature in your Magento module.

### PHP

{:.bs-callout .bs-callout-info}
Magento, with assistance from our community, is implementing PHP 7.2 compatibility for the 2.3.0 release. Any backward-incompatibility issues will be resolved in this release, and all 3rd party libraries now support PHP 7.2. Fully tested 7.2 support will be delivered in following patch releases. If you are interested in participating in Magento Community projects we welcome your help! See our [ZenHub board](https://app.zenhub.com/workspace/o/magento-engcom/php-7.2-support/boards?repos=116423356,116426364,115111902) for a full list of outstanding issues.

{% include install/php_2.3.md %}

#### Required PHP extensions

<<<<<<< HEAD
{:.bs-callout .bs-callout-info}
||||||| merged common ancestors
<div class="bs-callout bs-callout-info" id="info" markdown="1">
=======
<div class="bs-callout bs-callout-info" id="info" markdown="1">
<<<<<<< HEAD
The [CentOS]({{page.baseurl}}/install-gde/prereq/php-centos.html) and [Ubuntu]({{page.baseurl}}/install-gde/prereq/php-ubuntu.html) PHP installation instructions include a step for installing these extensions.
=======
>>>>>>> d5d623cb5417027e016a6a61e5689de46ee6e31b
The [PHP installation instructions](prereq/php-centos-ubuntu.html) include a step for installing these extensions.
<<<<<<< HEAD

*	[bc-math](http://php.net/manual/en/book.bc.php){:target="_blank"} ({{site.data.var.ee}} only)
* [ctype](http://php.net/manual/en/book.ctype.php){:target="_blank"}
*	[curl](http://php.net/manual/en/book.curl.php){:target="_blank"}
* [dom](http://php.net/manual/en/book.dom.php){:target="_blank"}
*	[gd](http://php.net/manual/en/book.image.php){:target="_blank"}
*	[intl](http://php.net/manual/en/book.intl.php){:target="_blank"}
*	[mbstring](http://php.net/manual/en/book.mbstring.php){:target="_blank"}
*	[hash](http://php.net/manual/en/book.hash.php){:target="_blank"}
*	[openssl](http://php.net/manual/en/book.openssl.php){:target="_blank"}
*	[PDO/MySQL](http://php.net/manual/en/ref.pdo-mysql.php){:target="_blank"}
*	[SimpleXML](http://php.net/manual/en/book.simplexml.php){:target="_blank"}
*	[soap](http://php.net/manual/en/book.soap.php){:target="_blank"}
* [spl](http://php.net/manual/en/book.spl.php){:target="_blank"}
*	[libxml](http://php.net/manual/en/book.libxml.php){:target="_blank"}
*	[xsl](http://php.net/manual/en/book.xsl.php){:target="_blank"}
*	[azip](http://php.net/manual/en/book.zip.php){:target="_blank"}
*	[json](http://php.net/manual/en/book.json.php){:target="_blank"}
*	[iconv](http://php.net/manual/en/book.iconv.php){:target="_blank"}
||||||| merged common ancestors
</div>

*	[bc-math](http://php.net/manual/en/book.bc.php){:target="&#95;blank"} ({{site.data.var.ee}} only)
* [ctype](http://php.net/manual/en/book.ctype.php){:target="&#95;blank"}
*	[curl](http://php.net/manual/en/book.curl.php){:target="&#95;blank"}
* [dom](http://php.net/manual/en/book.dom.php){:target="&#95;blank"}
*	[gd](http://php.net/manual/en/book.image.php){:target="&#95;blank"}
*	[intl](http://php.net/manual/en/book.intl.php){:target="&#95;blank"}
*	[mbstring](http://php.net/manual/en/book.mbstring.php){:target="&#95;blank"}
*	[hash](http://php.net/manual/en/book.hash.php){:target="&#95;blank"}
*	[openssl](http://php.net/manual/en/book.openssl.php){:target="&#95;blank"}
*	[PDO/MySQL](http://php.net/manual/en/ref.pdo-mysql.php){:target="&#95;blank"}
*	[SimpleXML](http://php.net/manual/en/book.simplexml.php){:target="&#95;blank"}
*	[soap](http://php.net/manual/en/book.soap.php){:target="&#95;blank"}
* [spl](http://php.net/manual/en/book.spl.php){:target="&#95;blank"}
*	[libxml](http://php.net/manual/en/book.libxml.php){:target="&#95;blank"}
*	[xsl](http://php.net/manual/en/book.xsl.php){:target="&#95;blank"}
*	[azip](http://php.net/manual/en/book.zip.php){:target="&#95;blank"}
*	[json](http://php.net/manual/en/book.json.php){:target="&#95;blank"}
*	[iconv](http://php.net/manual/en/book.iconv.php){:target="&#95;blank"}
=======
>>>>>>> 2.3.0-beta
</div>

*	[bc-math](http://php.net/manual/en/book.bc.php){:target="&#95;blank"} ({{site.data.var.ee}} only)
* [ctype](http://php.net/manual/en/book.ctype.php){:target="&#95;blank"}
*	[curl](http://php.net/manual/en/book.curl.php){:target="&#95;blank"}
* [dom](http://php.net/manual/en/book.dom.php){:target="&#95;blank"}
<<<<<<< HEAD
*	[gd](http://php.net/manual/en/book.image.php){:target="&#95;blank"}, [ImageMagick 6.3.7](http://php.net/manual/en/book.imagick.php){:target="&#95;blank"} (or later) or both
=======
*	[gd](http://php.net/manual/en/book.image.php){:target="&#95;blank"}
>>>>>>> 2.3.0-beta
*	[intl](http://php.net/manual/en/book.intl.php){:target="&#95;blank"}
*	[mbstring](http://php.net/manual/en/book.mbstring.php){:target="&#95;blank"}
*	[hash](http://php.net/manual/en/book.hash.php){:target="&#95;blank"}
*	[openssl](http://php.net/manual/en/book.openssl.php){:target="&#95;blank"}
*	[PDO/MySQL](http://php.net/manual/en/ref.pdo-mysql.php){:target="&#95;blank"}
*	[SimpleXML](http://php.net/manual/en/book.simplexml.php){:target="&#95;blank"}
*	[soap](http://php.net/manual/en/book.soap.php){:target="&#95;blank"}
* [spl](http://php.net/manual/en/book.spl.php){:target="&#95;blank"}
<<<<<<< HEAD
*	[libxml](http://php.net/manual/en/book.spl.php){:target="&#95;blank"}
*	[xsl](http://php.net/manual/en/book.xsl.php){:target="&#95;blank"}
*	[zip](http://php.net/manual/en/book.zip.php){:target="&#95;blank"}
=======
*	[libxml](http://php.net/manual/en/book.libxml.php){:target="&#95;blank"}
*	[xsl](http://php.net/manual/en/book.xsl.php){:target="&#95;blank"}
*	[azip](http://php.net/manual/en/book.zip.php){:target="&#95;blank"}
>>>>>>> 2.3.0-beta
*	[json](http://php.net/manual/en/book.json.php){:target="&#95;blank"}
*	[iconv](http://php.net/manual/en/book.iconv.php){:target="&#95;blank"}
>>>>>>> d5d623cb5417027e016a6a61e5689de46ee6e31b

#### PHP OPcache
<<<<<<< HEAD
=======

<<<<<<< HEAD
We strongly recommend you verify that  [PHP OPcache](http://php.net/manual/en/intro.opcache.php) is enabled for performance reasons. The OPcache is enabled in many PHP distributions. To verify if it is installed, see our [PHP documentation](prereq/php-centos-ubuntu.html).
||||||| merged common ancestors
We strongly recommend you verify that  <a href="http://php.net/manual/en/intro.opcache.php" target="&#95;blank">PHP OPcache</a> is enabled for performance reasons. The OPcache is enabled in many PHP distributions. To verify if it is installed, see our [PHP documentation](prereq/php-centos-ubuntu.html).
=======
We strongly recommend you verify that  <a href="http://php.net/manual/en/intro.opcache.php" target="&#95;blank">PHP OPcache</a> is enabled for performance reasons. The OPcache is enabled in many PHP distributions. To verify if it is installed, see our [PHP documentation](prereq/php-centos-ubuntu.html).
>>>>>>> 2.3.0-beta
>>>>>>> d5d623cb5417027e016a6a61e5689de46ee6e31b

<<<<<<< HEAD
If you must install it separately, see the [PHP OPcache documentation](http://php.net/manual/en/opcache.setup.php).
||||||| merged common ancestors
If you must install it separately, see the <a href="http://php.net/manual/en/opcache.setup.php" target="&#95;blank">PHP OPcache documentation</a>.
=======
We strongly recommend you verify the [PHP OPcache](http://php.net/manual/en/intro.opcache.php){:target="&#95;blank"} is enabled for performance reasons. The OPcache is enabled in many PHP distributions. To verify if it is installed, see our PHP documentation for [CentOS]({{page.baseurl}}/install-gde/prereq/php-centos.html){:target="&#95;blank"} or [Ubuntu]({{page.baseurl}}/install-gde/prereq/php-ubuntu.html){:target="&#95;blank"}.

If you must install it separately, see the [PHP OPcache documentation](http://php.net/manual/en/opcache.setup.php){:target="&#95;blank"}.
>>>>>>> d5d623cb5417027e016a6a61e5689de46ee6e31b

#### PHP settings

We recommend particular PHP configuration settings, such as `memory_limit`, that can avoid common problems when using Magento.

For more information, see [Required PHP settings]({{ page.baseurl }}/install-gde/prereq/php-settings.html).

### SSL

*	A valid {% glossarytooltip 363d6806-6a7d-4cb6-bc47-efc62bc26a1c %}security certificate{% endglossarytooltip %} is required for HTTPS.
*	Self-signed SSL certificates are not supported.
*	Transport Layer Security (TLS) requirement - PayPal and `repo.magento.com` both require TLS 1.1 or later:

	*	[More information about PayPal]({{page.baseurl}}/install-gde/system-requirements_tls1-2.html)

	*	[More information about `repo.magento.com`]({{ site.baseurl }}/guides/v2.1/release-notes/tech_bull_tls-repo.html)

### Mail server

Mail Transfer Agent (MTA) or an SMTP server

<<<<<<< HEAD
### Magento can use the following technologies:

*	[Redis]({{page.baseurl}}/config-guide/redis/config-redis.html) version 3.2 (compatible with 2.4+ ) for page caching and session storage
*	[Varnish]({{page.baseurl}}/config-guide/varnish/config-varnish.html) version 4.x or 5.0
*	[memcached]({{page.baseurl}}/config-guide/memcache/memcache.html) latest stable version for session storage with either `memcache` or `memcached` PHP extensions (latest stable version)

####	{{site.data.var.ee}} only
=======
### Technologies Magento can use

*	[Redis]({{page.baseurl}}/config-guide/redis/config-redis.html) version 3.2 (compatible with 2.4+ ) for page caching and session storage
*	[Varnish]({{page.baseurl}}/config-guide/varnish/config-varnish.html) version 4.x or 5.2
>>>>>>> 2.3.0-beta

*	[Elasticsearch]({{page.baseurl}}/config-guide/elasticsearch/es-overview.html)

    {{site.data.var.ee}} version 2.3.x supports the following Elasticsearch versions:

    *	Elasticsearch [5.2.x](https://www.elastic.co/downloads/past-releases/elasticsearch-5-2-2){:target="_blank"}
    *	Elasticsearch [2.x](https://www.elastic.co/downloads/past-releases/elasticsearch-2-4-5){:target="_blank"}

<<<<<<< HEAD
    Magento 2.3 uses [Elasticsearch PHP client](https://github.com/elastic/elasticsearch-php){:target="_blank"} version 5.2. (Before version 2.3, Magento used PHP client version 5.1.)
||||||| merged common ancestors
    Magento 2.3 uses [Elasticsearch PHP client](https://github.com/elastic/elasticsearch-php){:target="&#95;blank"} version 5.2. (Before version 2.3, Magento used PHP client version 5.1.)
=======
<<<<<<< HEAD
    Magento 2.2.3 uses [Elasticsearch PHP client](https://github.com/elastic/elasticsearch-php){:target="&#95;blank"} version 5.1. (Before version 2.2.3, Magento used PHP client version 2.0.)
=======
    Magento 2.3 uses [Elasticsearch PHP client](https://github.com/elastic/elasticsearch-php){:target="&#95;blank"} version 5.2. (Before version 2.3, Magento used PHP client version 5.1.)
>>>>>>> d5d623cb5417027e016a6a61e5689de46ee6e31b

*	RabbitMQ 3.7.x (compatible with 2.0 and later)
>>>>>>> 2.3.0-beta

    [RabbitMQ]({{page.baseurl}}/config-guide/mq/rabbitmq-overview.html){:target="_blank"} can be used to publish messages to queue and to define the consumers that receive the messages asynchronously.

<<<<<<< HEAD
    [RabbitMQ]({{page.baseurl}}/config-guide/mq/rabbitmq-overview.html){:target="&#95;blank"} can be used to publish messages to queue and to define the consumers that receive the messages asynchronously.

*	Three master databases

    These [master databases]({{page.baseurl}}/config-guide/multi-master/multi-master.html) provide scalability advantages for different functional areas of the Magento application, such as checkout, orders, and all remaining Magento2 application tables.
=======
####	{{site.data.var.ee}} only

*	Three master databases

    These [master databases]({{page.baseurl}}/config-guide/multi-master/multi-master.html) provide scalability advantages for different functional areas of the Magento application such as checkout, orders, and all remaining Magento2 application tables.
>>>>>>> 2.3.0-beta

### Optional but recommended

*	[php_xdebug 2.5.x](http://xdebug.org/download.php){:target="_blank"} or later (development environments only; can have an adverse effect on performance)

{:.bs-callout .bs-callout-info}
There is a known issue with `xdebug` that can affect Magento installations or access to the storefront or Magento Admin after installation. For details, see [Known issue with xdebug]({{page.baseurl}}/install-gde/trouble/tshoot_install-issues.html#known-devbeta-xdebug).

* [`mcrypt`](http://php.net/manual/en/book.mcrypt.php){:target="_blank"}
*	PHPUnit (as a command-line tool) 6.2.0
<<<<<<< HEAD

### Documentation

[Install Magento prerequisites]({{page.baseurl}}/install-gde/prereq/prereq-overview.html){:target="&#95;blank"}
=======
>>>>>>> 2.3.0-beta
