# 源类型处理器

## 语雀文档 (yuque_article)
- 检测: yuque.com 或 yuque.antfin.com
- 处理: skylark_resolve_url → skylark_doc_detail → raw/yuque-{slug}.md

## 钉钉文档 (dingtalk_doc)
- 检测: alidocs.dingtalk.com
- 处理: mcp_MCP_get_document_info → mcp_MCP_get_document_content → raw/dingtalk-{uuid}.md

## 本地 Markdown
- 检测: .md 结尾
- 处理: 复制到 raw/

## 本地 PDF
- 检测: .pdf 结尾
- 处理: pdf skill 解析

## 本地 DOCX
- 检测: .docx 结尾
- 处理: docx skill 解析

## Web 文章
- 检测: http(s):// 非语雀/钉钉
- 处理: fetch_content → raw/
