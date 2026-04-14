---
title: "source-酒店日历页套餐推荐模块"
type: source
tags: ["#source/dingtalk", "#domain/recommend", "#domain/calendar"]
created: 2026-04-14
updated: 2026-04-14
source_url: "https://alidocs.dingtalk.com/i/nodes/mExel2BLV5w036yZhQAz5gqa8gk9rpMq"
source_type: dingtalk_doc
---

# 小搜detail页套餐推荐模块迁移 摘要

## 文档信息
- **来源**: 钉钉文档
- **URL**: https://alidocs.dingtalk.com/i/nodes/mExel2BLV5w036yZhQAz5gqa8gk9rpMq
- **项目**: 24年618

## 业务背景

小搜detail页的售卖转化率相较于其他渠道有明显的优势：

| 端 | 购买转化率 |
|---|---|
| 飞猪端 | **6.65%** |
| 淘宝端 | 3.74% |
| 支付宝端 | 4.7% |

## 目标
稳定性目标

## 核心功能

### 1. 选品范围
- 类目ID过滤
- SKU关联shid
- 售卖有效期
- 黑名单过滤

### 2. 排序逻辑
- 业务加权标（ictag=2395202）
- 类目加权
- cico时间可约
- 大促商品标
- 销量、价格、店铺优先级

### 3. 商品卡片输出
- 结构化信息：标题、x元素、图片、价格
- 在线预约套餐优势标签

### 4. 定制逻辑
- 万豪集团商品召回规则
- shid名单控制模块不透出

## 业务术语

| 术语 | 说明 |
|------|------|
| **小搜** | 酒店日历域的开发同学 |
| **ictag** | 商品标签 |
| **shid** | 酒店ID |
| **cico** | check-in check-out |

## 提取的实体
- [[酒店日历页]]
- [[套餐推荐模块]]

## 违规词列表
> 2人起订、单人、差价、补差、定金、咨询客服、单拍无效、确认后再拍、代订、代拍
