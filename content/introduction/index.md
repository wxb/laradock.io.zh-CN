---
title: 介绍
type: index
weight: 1
---




一个基于Docker容器技术的完整PHP开发环境

Includes pre-packaged Docker Images, all pre-configured to provide a wonderful PHP development environment.

Laradock is well known in the Laravel community, as the project started with single focus on running Laravel projects on Docker. Later and due to the large adoption from the PHP community, it started supporting other PHP projects like Symfony, CodeIgniter, WordPress, Drupal...


![](https://s19.postimg.org/jblfytw9f/laradock-logo.jpg)

## 概述

来让我们一起看看安装`NGINX`, `PHP`, `Composer`, `MySQL`, `Redis` 和 `Beanstalkd`有多容易:

1 - 克隆 Laradock 到你的PHP项目中:

```shell
git clone https://github.com/Laradock/laradock.git
```

2 - 进入 laradock 目录, 将 `env-example` 文件名修改为 `.env`(***或者复制 `env-example` 文件命名为 `.env`***).

```shell
cp env-example .env
```

3 - 运行你的容器:

```shell
docker-compose up -d nginx mysql redis beanstalkd
```

4 - 打开你的PHP项目下的 `.env` 文件， 像下面这样配置:

```shell
DB_HOST=mysql
REDIS_HOST=redis
QUEUE_HOST=beanstalkd
```

5 - 打开你的浏览器并访问: `http://localhost`.

```shell
That's it! enjoy :)
```




<a name="features"></a>
## 特性

- 轻松切换PHP版本: 7.1, 7.0, 5.6...
- 选择你最爱的数据库引擎: MySQL, Postgres, MariaDB...
- 运行你自己的软件组合: Memcached, HHVM, Beanstalkd...
- 每个软件都运行在相互隔离的容器中:PHP-FPM, NGINX, PHP-CLI...
- 很容易定制任何容器，只需要简单的编辑 `Dockerfile` 文件.
- All Images extends from an official base Image. (Trusted base Images).
- Pre-configured NGINX to host any code at your root directory.
- Can use Laradock per project, or single Laradock for all projects.
- Easy to install/remove software's in Containers using environment variables.
- Clean and well structured Dockerfiles (`Dockerfile`).
- Latest version of the Docker Compose file (`docker-compose`).
- Everything is visible and editable.
- Fast Images Builds.
- More to come every week..




<a name="Supported-Containers"></a>
## 支持的软件 (镜像)

In adhering to the separation of concerns principle as promoted by Docker, Laradock runs each software on its own Container.
You can turn On/Off as many instances of as any container without worrying about the configurations, everything works like a charm.

- **Database Engines:**
MySQL - MariaDB - Percona - MongoDB - Neo4j - RethinkDB - MSSQL - PostgreSQL - Postgres-PostGIS.
- **Database Management:**
PhpMyAdmin - Adminer - PgAdmin
- **Cache Engines:**
Redis - Memcached - Aerospike
- **PHP Servers:**
NGINX - Apache2 - Caddy
- **PHP Compilers:**
PHP FPM - HHVM
- **Message Queueing:**
Beanstalkd - RabbitMQ - PHP Worker
- **Queueing Management:**
Beanstalkd Console - RabbitMQ Console
- **Random Tools:**
HAProxy - Certbot - Blackfire - Selenium - Jenkins - ElasticSearch - Kibana - Grafana - Mailhog - MailDev - Minio - Varnish - Swoole - Laravel Echo...

Laradock introduces the **Workspace** Image, as a development environment.
It contains a rich set of helpful tools, all pre-configured to work and integrate with almost any combination of Containers and tools you may choose.

**Workspace Image Tools**
PHP CLI - Composer - Git - Linuxbrew - Node - V8JS - Gulp - SQLite - xDebug - Envoy - Deployer - Vim - Yarn - SOAP - Drush...

You can choose, which tools to install in your workspace container and other containers, from the `.env` file.


> If you modify `docker-compose.yml`, `.env` or any `dockerfile` file, you must re-build your containers, to see those effects in the running instance.



If you can't find your Software in the list, build it yourself and submit it. Contributions are welcomed :)



## 赞助商





Support this project by becoming a sponsor. 

Your logo will show up on the [github repository](https://github.com/laradock/laradock/) index page and the [documentation](http://laradock.io/) main page, with a link to your website. [[Become a sponsor](https://opencollective.com/laradock#sponsor)]

<a href="https://opencollective.com/laradock/sponsor/0/website" target="_blank"><img src="https://opencollective.com/laradock/sponsor/0/avatar.svg"></a>
<a href="https://opencollective.com/laradock/sponsor/1/website" target="_blank"><img src="https://opencollective.com/laradock/sponsor/1/avatar.svg"></a>
<a href="https://opencollective.com/laradock/sponsor/2/website" target="_blank"><img src="https://opencollective.com/laradock/sponsor/2/avatar.svg"></a>
<a href="https://opencollective.com/laradock/sponsor/3/website" target="_blank"><img src="https://opencollective.com/laradock/sponsor/3/avatar.svg"></a>
<a href="https://opencollective.com/laradock/sponsor/4/website" target="_blank"><img src="https://opencollective.com/laradock/sponsor/4/avatar.svg"></a>
<a href="https://opencollective.com/laradock/sponsor/5/website" target="_blank"><img src="https://opencollective.com/laradock/sponsor/5/avatar.svg"></a>
<a href="https://opencollective.com/laradock/sponsor/6/website" target="_blank"><img src="https://opencollective.com/laradock/sponsor/6/avatar.svg"></a>
<a href="https://opencollective.com/laradock/sponsor/7/website" target="_blank"><img src="https://opencollective.com/laradock/sponsor/7/avatar.svg"></a>
<a href="https://opencollective.com/laradock/sponsor/8/website" target="_blank"><img src="https://opencollective.com/laradock/sponsor/8/avatar.svg"></a>
<a href="https://opencollective.com/laradock/sponsor/9/website" target="_blank"><img src="https://opencollective.com/laradock/sponsor/9/avatar.svg"></a>

<a target='_blank' rel='nofollow' href='https://app.codesponsor.io/link/JHiroABWV9N5QKgcFuTA2NxX/laradock/laradock'>
  <img alt='Sponsor' width='888' height='68' src='https://app.codesponsor.io/embed/JHiroABWV9N5QKgcFuTA2NxX/laradock/laradock.svg' />
</a>




<a name="what-is-docker"></a>
## Docker是什么?

[Docker](https://www.docker.com) is an open platform for developing, shipping, and running applications.
Docker enables you to separate your applications from your infrastructure so you can deliver software quickly.
With Docker, you can manage your infrastructure in the same ways you manage your applications.
By taking advantage of Docker’s methodologies for shipping, testing, and deploying code quickly, you can significantly reduce the delay between writing code and running it in production.





<a name="why-docker-not-vagrant"></a>
## 为什么是 Docker 而不是 Vagrant!?

[Vagrant](https://www.vagrantup.com) creates Virtual Machines in minutes while Docker creates Virtual Containers in seconds.

Instead of providing a full Virtual Machines, like you get with Vagrant, Docker provides you **lightweight** Virtual Containers, that share the same kernel and allow to safely execute independent processes.

In addition to the speed, Docker gives tons of features that cannot be achieved with Vagrant.

Most importantly Docker can run on Development and on Production (same environment everywhere). While Vagrant is designed for Development only, (so you have to re-provision your server on Production every time).






<a name="Demo"></a>
## 示例教程

What's better than a **Demo Video**:

- Laradock v5.* (should be next!)
- Laradock [v4.*](https://www.youtube.com/watch?v=TQii1jDa96Y)
- Laradock [v2.*](https://www.youtube.com/watch?v=-DamFMczwDA)
- Laradock [v0.3](https://www.youtube.com/watch?v=jGkyO6Is_aI)
- Laradock [v0.1](https://www.youtube.com/watch?v=3YQsHe6oF80)







<a name="Chat"></a>
## 与我们沟通

You are welcome to join our chat room on Gitter.

[![Gitter](https://badges.gitter.im/Laradock/laradock.svg)](https://gitter.im/Laradock/laradock?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)





<a name="Donations"></a>
## 捐助

> Help keeping the project development going, by [contributing](http://laradock.io/contributing) or donating a little. 
> Thanks in advance.

Donate directly via [Paypal](https://www.paypal.me/mzalt)

[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.me/mzalt) 

or become a backer on [Open Collective](https://opencollective.com/laradock#backer)

<a href="https://opencollective.com/laradock#backers" target="_blank"><img src="https://opencollective.com/laradock/backers.svg?width=890"></a>

or show your support via [Beerpay](https://beerpay.io/laradock/laradock) 

[![Beerpay](https://beerpay.io/laradock/laradock/badge.svg?style=flat)](https://beerpay.io/laradock/laradock)
