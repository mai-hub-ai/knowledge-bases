---
title: "Source: 套餐各叶子类目id"
type: source
tags: ["#domain/trade", "#source/dingtalk"]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/dingtalk-93NwLYZXWyZPdyb1CdZ6Xo47VkyEqBQm.md"]
direct_link: "raw/dingtalk-93NwLYZXWyZPdyb1CdZ6Xo47VkyEqBQm.md"
aliases: ["类目ID文档"]
---
# Source: 套餐各叶子类目id

## Direct Link
`raw/dingtalk-93NwLYZXWyZPdyb1CdZ6Xo47VkyEqBQm.md`

## Summary
本文档定义了酒店套餐的所有叶子类目ID，是套餐产品的基础数据字典。文档明确了类目的两级分类（含房/含餐服务）以及各类目的唯一标识ID，同时澄清了"电子凭证"、"日历套餐"是预约方式而非类目的概念。

## Narrative Thread
文档作为产品数据字典存在，目的是为开发、运营提供统一的类目ID参考。核心要点是区分类目本身与预约方式两个不同维度的概念。

## Key Takeaways
1. 酒店套餐分为两大类：含房类目、含餐/服务类目
2. 每个类目有唯一的数字ID标识
3. "电子凭证"、"日历套餐"是预约方式，不是类目
4. 同一类目可支持多种预约方式

## Entities Mentioned
- [[境内酒店套餐]] — 类目ID: 201189402，含房类目
- [[境外酒店套餐]] — 类目ID: 201188002，含房类目
- [[在线预约套餐]] — 类目ID: 50794037，含房类目
- [[境外在线申请套餐]] — 类目ID: 202032304，含房类目
- [[酒店餐饮美食]] — 类目ID: 201214101，含餐/服务类目
- [[酒店服务（新）]] — 类目ID: 201214201，含餐/服务类目
- ~~[[境内在线申请套餐]]~~ — 类目ID: 202032004，**已废弃**

## Concepts Introduced
- [[类目分类体系]] — 含房类目 vs 含餐/服务类目的分类逻辑
- [[预约方式]] — 电子凭证、日历套餐的概念说明

## Constraints & Risks Documented
| Constraint / Risk | Type | Details |
|---|---|---|
| 类目ID唯一性 | data | 每个类目ID必须唯一，不可重复使用 |
| 废弃类目 | operational | 境内在线申请套餐(202032004)已废弃，不再使用 |

## Cross-references to Updated Pages
- [[类目分类体系]] — 新建概念页
- [[预约方式]] — 新建概念页
- 各类目实体页 — 新建
