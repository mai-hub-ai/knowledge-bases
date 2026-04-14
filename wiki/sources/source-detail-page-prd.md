---
title: "Source: 套餐商品详情页改版1.0"
type: source
tags: ["#domain/detail", "#source/dingtalk"]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/dingtalk-oP0MALyR8kKL2Xb0H29q6rAL83bzYmDO.md"]
direct_link: "raw/dingtalk-oP0MALyR8kKL2Xb0H29q6rAL83bzYmDO.md"
aliases: ["详情页改版PRD"]
---
# Source: 套餐商品详情页改版1.0

## Direct Link
`raw/dingtalk-oP0MALyR8kKL2Xb0H29q6rAL83bzYmDO.md`

## Summary
本PRD是套餐商品详情页改版1.0的完整需求文档，旨在解决用户购买转化的三大核心问题：价格因素（用户看不清加价是否值得）、可住日期（担心买了不能住）、价值感知（无法快速感知套餐核心价值）。目标预计提升D2O转化率2.7pt。

## Narrative Thread
文档从业务问题出发（购买转化核心问题），提出解决方案（首屏信息架构重构、可住日历外露等），详细描述了头部媒体容器、价格区块、囤好货规则等模块的改造需求，并包含AB实验设计和数据埋点需求。

## Key Takeaways
1. 目标：D2O提升2.7pt（4.8% → 7.5%）
2. 头部媒体容器：导航栏位置变更、模块顺序调整、酒店图片上限<=5张
3. 囤好货规则：slogan变更、新增可住日历（仅单店&单sku）
4. 可住日历：外露30天，单店&单sku才透出
5. AB实验：基于uid维度50%对照组、50%实验组

## Entities Mentioned
- [[媒体容器区域]] — 模块1
- [[囤好货标签区]] — 模块7

## Concepts Introduced
- 可住日历透出条件 — 仅单店&单sku
- 大促场景导航栏顺序 — 图集-套餐权益-视频-酒店-相册

## Constraints & Risks Documented
| Constraint / Risk | Type | Details |
|---|---|---|
| 可住日历透出条件 | product | 仅单店&单sku才透出 |
| 酒店图片上限 | product | <=5张 |
| 淘宝端拼接限制 | technical | 通兑无视频时不拼接图片 |
| 大促时间配置 | operation | 需提前配置，支持多个时间段 |

## Cross-references to Updated Pages
- [[媒体容器区域]] — 已更新详细信息
- [[囤好货标签区]] — 已更新详细信息
