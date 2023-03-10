---
title: "React理念"
description: "React理念"
pubDate: "2023.3.3"
---
我么知道React时一款重运行时的应用级框架，意味着react在迭代方向上更偏向运行时特性，需要思考以下问题

- React面对的是什么问题？这些问题如何从运行时找到解决方案？
- React从v15升级到v16后，为什么要重构底层架构
- 重构后的新架构是如何工作的
- 如何快速调试源码

# 问题与解决思路

在React官网中提到，React的理念是：构建快速响应的大型web应用程序的首选方式

实现的关键在于快速响应，那么影响快速响应的因素是什么呢

- 当执行大计算量的操作或者设备性能不足时，页面掉帧，导致卡顿，概括为**cpu的瓶颈**
- 进行**I/O**操作后，需要等待数据返回后才能继续操作，等待的过程导致不能快速响应，概括为**I/O瓶颈**