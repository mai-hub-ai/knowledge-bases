---
title: "source-即买即约迭代"
type: source
tags: ["#source/dingtalk", "#domain/booking"]
created: 2026-04-14
updated: 2026-04-14
source_url: "https://alidocs.dingtalk.com/i/nodes/ZgpG2NdyVXYDdEa4tQ0a4BDzJMwvDqPk"
source_type: dingtalk_doc
---

# 即买即约日历页自动锚定日期+权益透出 摘要

## 文档信息
- **来源**: 钉钉文档
- **URL**: https://alidocs.dingtalk.com/i/nodes/ZgpG2NdyVXYDdEa4tQ0a4BDzJMwvDqPk
- **类型**: 补充需求

## 背景

观测页面转化数据发现：
1. 进入即买即约日历页的用户，仅20%的用户点击了日期
2. 进入下单页后即买即约Tab下唤起日历浮层中，仅60%的用户点击了日期

说明用户可能不知道日期可点击，权益表达透出过低。

## 核心需求

### 即买即约日历页自动锚定日期
进入即买即约日历页时，自动锚定近x天内权益最多的日期：
- 权益优先级：立减 > 改期 > 升房
- 特殊情况处理

### 底部权益气泡交互
选中日期后，底部权益气泡支持免费改期、免费升房透出：
- 多权益滚动展示
- 气泡出现需做弹出动效

### 即买即约下单页返回挽留弹窗
立即预订Tab下返回上一步时：
- 若日期有权益：展示权益挽留弹窗
- 若日期无权益：展示库存紧张挽留弹窗
- 疲劳度控制：24h内仅出现x次

## 提取的实体
- [[即买即约日历页]] — 自动锚定逻辑
- [[即买即约双Tab下单页]] — 返回挽留弹窗

## 关联页面
- [[source-即买即约PRD]]
