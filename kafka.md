# kafka 概述

## 消息队列

消息队列的功能

- 解耦:解除业务系统的直接依赖
- 冗余:冗余数据，规避数据丢失的风险
- 扩展性
- 削峰
- 可恢复
- 顺序保证
- 缓冲
- 异步通信

消息队列的两种模式

- 点对点模式：消费者主动拉取，ack之后消息清除，消息只能被一个接受者接收处理
- 发布订阅模式：队列自动推送，消息可以被多次消费

## kafka

kafka是一个开源分布式消息队列，由LinkedIn使用scala开发，于2011年开源。对消息的保存时根据Topic进行归类，发送消息着成为Producer、消息接受者成为Consumer，此外kafka集群有多个kafka实例组成，每个实例被称为broker，无论是kafka集群还是consumer都依赖于ZooKeeper来保证系统的可靠性。