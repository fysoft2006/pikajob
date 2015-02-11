PikaJob
=======

PikaJob is pure-Java Asynchronous Job-Flow Platform.

通用异步工作流平台

![http://ww1.sinaimg.cn/bmiddle/60c9620fjw1eozsd1u8fuj205k06a3z3.jpg](http://ww1.sinaimg.cn/bmiddle/60c9620fjw1eozsd1u8fuj205k06a3z3.jpg)

## 项目信息 ##

- Java项目(1.6+)
- Maven管理(3.0.5+)

pikajob.git branches and Maven version:

- dev(develop branch): 0.0.1-SNAPSHOT
- master(develop branch): 0.0.1-SNAPSHOT
- [更新日志](https://github.com/knightliao/pikajob/wiki/updates) 

## 它是什么? ##

PikaJob可以为各种业务平台提供统一的异步工作流解决方案。

## 功能特点 ##

提供简单、统一、通用的简单异步任务管理平台

- 异步化机制，消息推送
- 操作幂等支持
- 操作查询支持
- 语法支持业界通用的Spring AMQP

## 应用场景 ##

- 用户知道可能会失败的场景
    - 举例1：陆金所 投资一个项目
        - 问题：投资一个项目涉及的操作特别多，譬如需要判断银行是否有足够的余额。这里投资可能会失败，可能是由于用户自己银行余额不够。
        - 解决办法：投资项目时直接返回给用户成功，项目状态为投资中。系统异步的与银行确定是否有足够的金额，若成功，则通过站内信返回投资成功；若失败，则通过站内信返回投资失败。
    - 举例2：申请云主机
    - 举例3：下载自定义报表
- 用户明确知道一定会成功的场景
    - 举例1：新浪微博 发布一条消息
        - 问题：发布一条微博涉及的操作特别多，值得注意的是，用户认为发布一定会成功。（除非新浪挂机）
        - 解决办法：用户发布消息后，业务系统生成一条假消息先让用户通过界面可以查询得到（此时消息还未真正处理完成）；后端异步的处理这条消息。
    - 举例2：下载自定义报表
        - 问题：
        - 解决办法

## 模块架构图  ##

## 模块信息##

## 用户指南 ##

### 概述 ###

## 开发人员指南 ##

- [pikajob详细设计文档](https://github.com/knightliao/pikajob/wiki/overall-design)

## 其它 ##

