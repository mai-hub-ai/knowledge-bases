# 飞猪酒店套餐产品知识库 - Schema for Claude Code

## KB Structure

本知识库基于 **Karpathy LLM Wiki 方法论**，采用三层架构：

| 层 | 目录 | 所有者 | 说明 |
|----|------|--------|------|
| Layer 1: Raw Sources | \`raw/\` | 不可变 | 原始文档（语雀/钉钉/本地文件），LLM 只读不写 |
| Layer 2: Wiki | \`wiki/\` | LLM | 结构化 Markdown 页面，LLM 生成维护 |
| Layer 3: Schema | \`.schema/\` | 用户 + LLM | 知识库配置，定义结构和约定规则 |

## Navigation Workflow

1. **Always read \`wiki/index.md\` first** - 快速了解知识库全貌
2. Follow \`[[wikilinks]]\` 导航到相关页面
3. 查询时优先读取 \`wiki/onboarding.md\` 了解当前状态

## Ingest Workflow

用户提供源文档 → 保存到 raw/ → LLM分析提取 → 生成Wiki页面 → 更新导航文件 → Git commit

## Domain Conventions - 酒店套餐产品

### 页面层级标签
- #domain/channel - 频道页
- #domain/calendar - 酒店日历页  
- #domain/detail - 套餐详情页
- #domain/sku - SKU浮层
- #domain/order - 下单页
- #domain/trade - 交易/资金
- #domain/d2o - 详情页到下单转化
