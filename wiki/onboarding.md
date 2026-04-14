---
title: Onboarding Guide
type: overview
tags:
  - "#internal/guide"
created: 2026-04-14
updated: 2026-04-14
---
# 知识库快速上手指南

> 本文档帮助新对话中的 LLM 快速了解知识库状态和下一步工作

## 当前状态快照

- **知识库名称**: fliggy-hotel-package-kb
- **创建日期**: 2026-04-14
- **最后更新**: 2026-04-14
- **总页面数**: 4（初始结构）
- **已摄入源**: 0
- **待处理任务**: 等待用户发送源文档

## 已完成工作

- [x] 知识库初始化
- [x] Schema配置完成
- [x] 目录结构建立

## 待完成工作

- [ ] 摄入首批源文档
- [ ] 提取实体和概念
- [ ] 建立页面间交叉引用

## 产品领域说明

我是酒店套餐产品经理，负责以下产品流程：

**用户流程**：
频道页 → 酒店日历页 → 套餐详情页 → 套餐SKU浮层 → 套餐普通下单页/套餐即买即约下单页

**核心目标**：
促进用户购买酒店套餐，提升套餐详情页→下单用户的转化（d2o）

**复杂度来源**：
- 横向：多端差异（iOS/Android/H5/小程序）、页面内模块多版本历史逻辑
- 纵向：交易状态流转、资金逻辑

## 源接入方式

### 语雀文档
- URL 格式: `https://yuque.com/{group}/{repo}/{slug}`
- 示例: "摄入这个语雀 PRD: https://yuque.com/xxx"

### 钉钉文档
- URL 格式: `https://alidocs.dingtalk.com/i/nodes/{dentryUuid}`
- 示例: "摄入这个钉钉 PRD: https://alidocs.dingtalk.com/i/nodes/xxx"

### 本地文件
- 直接发送文件路径
- 示例: "摄入这个文件: /path/to/prd.pdf"

## 常见操作命令

- 摄入新文档: 发送文档URL或路径
- 查询知识库: 直接提问
- 健康检查: "/knowledge-base-builder lint"

## 标签体系

按页面层级组织：
- #domain/channel - 频道页
- #domain/calendar - 酒店日历页
- #domain/detail - 套餐详情页
- #domain/sku - SKU浮层
- #domain/order - 下单页
- #domain/trade - 交易/资金
- #domain/d2o - 详情页到下单转化

## 注意事项

1. 每次摄入后必须更新 `index.md`、`log.md`、`onboarding.md`
2. 保持 Frontmatter 完整性
3. 所有交叉引用使用 `[[wikilink]]` 格式
4. Git commit 遵循规范: "ingest: {title}"
