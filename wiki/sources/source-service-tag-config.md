---
title: "Source: 心智区支持业务自定义配置亮点标签"
type: source
tags: ["#domain/detail", "#source/dingtalk"]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/dingtalk-kDnRL6jAJMpxeYDohKK2m1YyVyMoPYe1.md"]
direct_link: "raw/dingtalk-kDnRL6jAJMpxeYDohKK2m1YyVyMoPYe1.md"
aliases: ["服务标签配置PRD"]
pm: "宁音"
---
# Source: 心智区支持业务自定义配置亮点标签

## Direct Link
`raw/dingtalk-kDnRL6jAJMpxeYDohKK2m1YyVyMoPYe1.md`

## Summary
本PRD描述了心智区（服务标签区）支持业务自定义配置亮点标签的需求。背景是会员套餐可赠送的权益by品有所不同，需要支持运营配置自定义标签透出，而非仅限于"加赠积分"标签。

## Narrative Thread
文档从业务痛点出发（会员权益配置灵活性不足），提出解决方案（支持业务自定义配置标签），并详细说明了配置后台、透出规则、排序逻辑等实现细节。

## Key Takeaways
1. 支持业务在套餐工作台配置自定义标签
2. 配置维度：标签名称 + skuid list
3. sku维度直接透出，item维度需满足50%阈值
4. 标签排序：立即预约 > 业务配置标签 > 0元囤 > 节假日可住 > 改期/升房
5. 标签需写入summary对外使用

## Entities Mentioned
- [[服务标签区]] — 核心模块
- [[套餐详情页]] — 所属页面

## Concepts Introduced
- 业务配置标签 — 运营平台配置的自定义标签
- sku透出阈值 — item粒度透出需要的sku比例

## Constraints & Risks Documented
| Constraint / Risk | Type | Details |
|---|---|---|
| 标签准确性 | business | 系统不做准确性判断，配置错误由业务承担 |
| 浮层文案必填 | product | 每个标签都要有对应的解释文案 |
| sku透出阈值 | config | 默认50%，可调整配置 |

## Cross-references to Updated Pages
- [[服务标签区]] — 已更新详细逻辑
- [[业务语义字典]] — 新建概念页
