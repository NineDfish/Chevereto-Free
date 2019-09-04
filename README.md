# Chevereto Free

安装cheverto

1、上传安装包

2、解压Chevereto-Free到网站根目录,并赋予权限

chown www:www -R /www/wwwroot/xxxx

3、创建settings.php文件

在/www/wwwroot/xxxx/app目录新建settings.php文件并给予可写入权限:

cd  /www/wwwroot/xxxx/app

touch settings.php

chmod -R 777 settings.php

3、修改网站配置文件，如：/www/server/panel/vhost/nginx/xxxx.conf

添加

location / {

index index.php;
try_files $uri $uri/ /index.php?$query_string;

}

重启nginx
Nginx -s reload

输入域名开始安装
---------------------------------------------------------------------------------------------------------------------------------

Chevereto is an image hosting software that allows you to create a beautiful and full-featured image hosting website on your own server. It's your hosting and your rules, so say goodbye to closures and restrictions. This repo here is Chevereto Free, which is a fork of Chevereto V3 in which only the most essential features are preserved and it is released as Open Source software.

Chevereto Free has the same look and feel of the [paid version](https://chevereto.com). Most likely it will fit all your personal needs. The features removed in this fork are those business-oriented like external storage servers or banner management to name a few.

## Building the next-gen Chevereto

Chevereto is being modernized by introducing new coding standards and turning towards a common Open Source base. [View all updates](https://chevereto.com/community/threads/building-the-next-gen-chevereto.11140/).

Take [the survey](https://forms.gle/B3tU2V7CSykJCpoA6) and help me to shape a better Chevereto.

## Minimum system requirements

Make sure your server meets the minimum system requirements which are:

- PHP 7 (PHP 5.6 min)
- MySQL 8 / MariaDB 10 (ALL PRIVILEGES)
- Apache / NGiNX web server

The system has a built-in system check that will tell you right away when you need to fix something on your server.

## Installation

Chevereto can be installed in several different ways, it all depends on what suits you best.

### ⚡Install using Installer

The [installer](https://github.com/Chevereto/Installer) is a single `.php` file which will download and extract the latest release for you. Automatic database setup for cPanel based web servers.

1. Download the [Chevereto Installer](https://chevereto.com/download/file/installer)
2. Upload the `installer.php` file to your target `public_html` folder.
3. Open your website and follow the steps.

### 🐳Install using Docker

Docker allows you to easily install and maintain all the server dependencies with ease by using automated application containers. The ready-to-use Docker images are under [nmtan/chevereto](https://hub.docker.com/r/nmtan/chevereto/) (many thanks to [Tan Nguyen](https://github.com/tanmng))

### ✨Install using Softaculous/Fantastico

If your web hosting includes [Softaculous](https://softaculous.com/)/[Fantastico](https://netenberg.com/fantastico.php), you can install Chevereto Free with just one click. Chevereto Free should be available for one-click install under the "Image Galleries" category.

### 📦Install via zip/tarball

 1. Download the [latest release](https://github.com/Chevereto/Chevereto-Free/releases/latest)
 2. Upload the contents of your download to your server (usually the `public_html` folder)
 3. Go to your website and follow the instructions

For additional installation instructions, refer to our [official documentation](https://chevereto.com/docs/install).

## Updates

Chevereto has a built-in system that checks for new updates every day via the [Chevereto API](https://chevereto.com/api/get/info/free). The system will notify you when an update is available, and it will guide you through the process.

## Upgrade to paid edition

To upgrade to our paid edition, simply navigate to your dashboard panel and click on the `upgrade` button.

## Support

Use our [Bug Tracking](https://chevereto.com/bug-tracking) to report bugs and our [Community Support](https://chevereto.com/community-support) forums for any support concern.

## License

Copyright [Rodolfo Berríos](http://rodolfoberrios.com) - Released under the AGPLv3 license.

## Warranty

This software doesn't include support. It may contain bugs. Use it at your own risk. This software is offered on an “as-is” basis. No warranty, either expressed or implied, is given.
