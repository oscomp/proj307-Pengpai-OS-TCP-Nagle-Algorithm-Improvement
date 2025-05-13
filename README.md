# proj307-Pengpai-OS-TCP-Nagle-Algorithm-Improvement
## 澎湃OS-TCP Nagle算法完善

## 项目描述

### 关于小米澎湃OS

小米澎湃OS是一款以人为中心、打造「人车家全生态」的操作系统。小米澎湃OS经过 13 年探索，历时 7 年研发，参与的工程师超过5000名，进行了史无前例的系统底层重构，为未来百亿设备、百亿连接做好「万物互联的公有底座」。

2017年，小米自研的Vela OS正式发布，逐步统一IoT设备生态。2019年，小米开始并行研发纯自研通用系统Mina OS。2021年，小米开启了车机OS的研发。2022年初，小米统一MIUI、Vela、Mina、车机OS四个系统的软件架构，自此小米的操作系统底层合并完成。
小米澎湃OS融合200+品类，可连接8.2亿设备，全球首创的「人车家全生态」由此大幕开启。

### 关于Vela和NuttX

**关于Vela**：[Vela](https://iot.mi.com/vela)是小米公司基于开源实时操作系统NuttX打造的物联网嵌入式软件平台，Vela在各种物联网硬件平台上提供统一的软件服务，支持丰富的组件和易用的框架，用于打通碎片化的物联网应用场景。

**关于NuttX**：[NuttX](https://nuttx.apache.org/docs/latest/)是一个在IoT、分布式嵌入式系统、无人机系统中广泛使用的RTOS，第一个版本由 Gregory Nutt 于 2007 年发布。NuttX 可以支持 8 位到64位的处理器，支持risc-v，arm，mips，x86等主流芯片平台，按照POSIX和 ANSI 标准进行设计，支持MMU和MPU，支持多线程和进程。2019年NuttX在小米的推动下正式进入Apache基金会，小米多位资深工程师参与了[NuttX社区](https://github.com/apache/nuttx)的开发和架构设计。经过多年的不懈努力，NuttX功能丰富，性能稳定，商业化成熟度高，在各种物联网产品上得到了广泛的应用。

### 关于赛题

Nagle算法（[RFC 896](https://datatracker.ietf.org/doc/html/rfc896) && [RFC 1122 Section 4.2.3.4](https://datatracker.ietf.org/doc/html/rfc1122#page-98)）在TCP发送流程中是一个重要的能力，对于大量小数据的发送性能起到优化作用。Vela操作系统拥有一个精简的TCP协议栈，而Vela的TCP对Nagle算法的支持尚不完备。本项目的目标是基于Vela已有的TCP协议栈，探索Nagle算法的实现及优化，提升Vela操作系统的TCP发送性能。

## 预期目标

- 了解POSIX规范的TCP socket通信
- 学习Vela/NuttX的TCP协议栈实现，探索Nagle算法优化思路
- 设计并实现功能完善的Nagle算法，并进行性能对比
- 提交最终实现代码至NuttX开源社区

## 特征

- 实际运行、修改、验证开源操作系统内核中的网络能力及收发性能
- 文档、代码、问题、答疑交互过程都开放和开源的
- 支持各种硬件，可以使用模拟器或实际硬件进行开发验证（环境配置见参考资料）

## 已有参考资料

- [NuttX的最新文档](https://nuttx.apache.org/docs/latest/)
  - [在PC上运行NuttX模拟器](https://nuttx.apache.org/docs/latest/platforms/sim/sim/index.html)
  - [使用QEMU虚拟机运行NuttX](https://nuttx.apache.org/docs/latest/platforms/arm/qemu/boards/qemu-armv7a/index.html)
  - [使用Raspberry Pi Pico (W)运行NuttX](https://nuttx.apache.org/docs/latest/platforms/arm/rp2040/boards/raspberrypi-pico-w/index.html)
  - [使用K210板卡运行NuttX](https://nuttx.apache.org/docs/latest/platforms/risc-v/k210/boards/maix-bit/index.html)
  - [使用ESP32-C3运行NuttX](https://nuttx.apache.org/docs/latest/platforms/risc-v/esp32c3/index.html)
- [POSIX socket](https://pubs.opengroup.org/onlinepubs/9699919799/basedefs/sys_socket.h.html)
- [NuttX代码](https://github.com/apache/nuttx)
  - [Simulator（含使用网络的说明）](https://github.com/apache/nuttx/blob/master/Documentation/guides/simulator.rst)
  - [TCP协议栈](https://github.com/apache/nuttx/tree/master/net/tcp)

## 赛题分类

操作系统内核大类 --> 内核完善

## 参赛要求

- 以小组为单位参赛，最多三人一个小组
- 允许学生参加大赛的多个不同题目，最终自己选择一个题目参与评奖
- 请遵循“2025全国大学生操作系统比赛”的章程和技术方案要求

## 难度

中等

## License

Apache-2.0 License

## 所属赛道

2025全国大学生操作系统比赛的“OS功能挑战”赛道

## 项目导师

- 姓名：翁喆
- 单位：小米
- github ID：[https://github.com/wengzhe](https://github.com/wengzhe)
- email：[wengzhe@xiaomi.com](mailto:wengzhe@xiaomi.com)

---

- 姓名：张虹雨
- 单位：小米
- github ID：[https://github.com/zhhyu7](https://github.com/zhhyu7)
- email：[zhanghongyu@xiaomi.com](mailto:zhanghongyu@xiaomi.com)
