---
id: packagist-mirror-in-china
date: 2018-09-05 09:31:33
title: Packagist（Composer）中国镜像
categories: Documents
tags: [PHP, Package]
---

从七月份得知国内镜像开始「体检」之后，一直没有收到恢复的消息。

<!--more-->

> 2019 年 6 月 4 日更新：Laravel-China 镜像将于两个月后停用，参见：<https://learnku.com/articles/30758>

目前，[官网](https://pkg.phpcomposer.com/)依旧挂着公告：

> 通知：7 月 13 日（周五）下午 5 点本镜像将暂停更新，并且安装包（zip）资源的下载地址将指向 GitHub，一直持续到 18 日（下周三）。届时本镜像仍然可使用，只是下载安装包时由于走国外的服务器，速度会比较慢。
>
> 原因：此次暂停期间将对本镜像缓存的所有安装包（zip）以及元数据（json）进行校验和修复。上次全面体检时间是 2017 年 3 月份。
>
> 【7 月 18 日更新】：由于镜像暂停期间收到一个重要的 bug，我们正在追踪并修复此 bug，因此将镜像恢复时间再次延长一周，很抱歉各位，请再耐心等待，谢谢！。

尴尬，这是要凉凉吗。

由于公司服务器在国内阿里云（没办法挂 SS），部署项目执行 `composer install` 简直等到花都谢了，不符合应急情况需要快速增加实例的需求，经过一番谷歌，发现一替代方案。

<https://packagist.laravel-china.org/>

好歹也是出自大名鼎鼎的 Laravel-China 社区，应该能抗一阵子... 吧。

唉，还是那句话，努力赚钱，争取早日肉翻。
