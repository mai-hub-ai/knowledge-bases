# Wiki 约定规则

## 文件命名
- 使用 kebab-case（小写字母 + 连字符）
- 不使用空格、下划线或中文

## 链接格式
- 必须使用 \`[[wikilinks]]\` 格式
- 外部URL使用标准Markdown格式

## 标签体系
- #domain/ 业务领域
- #type/ 页面类型
- #status/ 状态标记
- #source/ 来源类型
- #platform/ 端标识

## YAML Frontmatter 必填字段
- title: 页面标题
- type: entity|concept|topic|source|analysis
- tags: 标签数组
- created: YYYY-MM-DD
- updated: YYYY-MM-DD
- sources: 来源文件数组
