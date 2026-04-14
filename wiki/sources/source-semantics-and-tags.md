---
title: "Source: 业务语义字典与服务标签补充"
type: source
tags: ["#domain/trade", "#domain/detail", "#source/user"]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/user-input-semantics-and-tags.md"]
direct_link: "raw/user-input-semantics-and-tags.md"
aliases: ["语义字典+标签补充"]
---
# Source: 业务语义字典与服务标签补充

## Direct Link
`raw/user-input-semantics-and-tags.md`

## Summary
本文档包含两部分核心内容：1）业务语义字典（单店/通兑定义），2）服务标签区的补充信息（会员类标签、价库亮点标签迭代逻辑）。是产品基础知识的重要组成部分。

## Narrative Thread
文档首先定义了核心业务术语（单店vs通兑），为后续业务逻辑讨论建立统一语言；然后补充了服务标签区的标签类型和迭代逻辑，记录了节假日可住标签的新旧逻辑对比。

## Key Takeaways
1. 单店：item关联1个shid；通兑：item关联>=2个shid
2. 会员类标签格式：【品牌词】享积分房晚
3. 节假日可住标签迭代：优先长假期（春节/五一/国庆）
4. 通兑类节假日可住计算：满足条件hid/关联hid > 99%

## Entities Mentioned
- [[服务标签区]] — 补充详细信息

## Concepts Introduced
- [[业务语义字典]] — 单店/通兑定义
- 长假期优先逻辑 — 节假日标签的新迭代逻辑

## Constraints & Risks Documented
| Constraint / Risk | Type | Details |
|---|---|---|
| 通兑判断阈值 | calculation | 满足节假日可住的hid/关联hid > 99% |
| 当前节假日跳过 | logic | 进入商详页时间命中某节假日则不计算该节假日 |

## Cross-references to Updated Pages
- [[业务语义字典]] — 新建概念页
- [[服务标签区]] — 已更新迭代逻辑
