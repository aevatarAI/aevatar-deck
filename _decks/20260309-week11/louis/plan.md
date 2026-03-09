---
layout: deck
title: "Week 11 Plan"
date: 2026-03-09
week: "2026-W11"
type: plan
member: louis
---

## Week 11 Plan

**Aevatar Team** · March 9, 2026

---

## 1. Marc.AI: Web Content Scraping Tool Integration

<div class="slide-meta"><span class="owner-tag">@louis</span> · <strong>Marc.AI</strong> · Due Friday 3/13</div>

<div class="slide-section-label">具体内容</div>

- 在 Marc.AI 业务服务中 web content scraping tool，实现基于用户描述或网站链接的营销内容抓取
- web search tool 作为独立的 MCP 服务，Marc.AI 通过 MCP 协议调用该服务获取相关页面
- cheerio 作为独立的 MCP 服务，Marc.AI 通过 MCP 协议调用该服务解析 HTML 内容，提取关键营销信息（标题、正文、CTA、产品特性等）
- 支持多种输入格式：自然语言描述、直接 URL、关键词搜索
- 将 Marc.AI web scraping tool 集成到 NyxID MCP 服务，NyxID MCP 实现 agent 调用该 tool 的能力

***

<div class="slide-section-label">验收标准</div>

- Marc.AI web scraping tool 实现完成
- web search tool MCP 服务和 cheerio MCP 服务独立部署成功
- Marc.AI 成功通过 MCP 协议调用 web search tool 和 cheerio MCP 服务
- 支持通过用户描述或 URL 抓取网页内容
- 成功提取关键营销元素（标题、正文、CTA 等）
- 错误处理完善（无效链接、网络超时、解析失败）
- 提取准确率 ≥ 85%
- Marc.AI tool 成功集成到 NyxID MCP 服务，NyxID MCP 实现 agent 调用该 tool，Aevatar agent 可通过 NyxID MCP 正常调用

---

## 2. Marc.AI: Marketing Content Reasoning Agent

<div class="slide-meta"><span class="owner-tag">@louis</span> · <strong>Marc.AI</strong> · Due Friday 3/13</div>

<div class="slide-section-label">具体内容</div>

- 在 Marc.AI 业务服务中构建 marketing content reasoning tool，基于抓取的营销内容进行深度分析
- 必要工具作为独立的 MCP 服务（如 sentiment analysis MCP 服务、keyword extraction MCP 服务、competitor analysis MCP 服务等），Marc.AI 通过 MCP 协议调用这些服务
- 分析营销内容的核心卖点、目标受众、情感倾向、关键信息结构
- 生成结构化分析报告：内容摘要、关键洞察、改进建议
- 将 Marc.AI reasoning tool 集成到 NyxID MCP 服务，NyxID MCP 实现 agent 调用该 tool 的能力


***

<div class="slide-section-label">验收标准</div>

- 独立分析工具 MCP 服务（sentiment analysis、keyword extraction 等）部署成功
- Marc.AI 成功通过 MCP 协议调用这些分析工具 MCP 服务
- 能够准确识别营销内容的核心卖点与目标受众
- 情感分析准确率 ≥ 80%
- 生成的分析报告结构清晰、洞察有价值
- 支持批量内容分析
- Marc.AI reasoning tool 成功集成到 NyxID MCP 服务，NyxID MCP 实现 agent 调用该 tool，Aevatar agent 可通过 NyxID MCP 正常调用

---

## 3. Marc.AI: Content Generation with nanobananaimg/APIs

<div class="slide-meta"><span class="owner-tag">@louis</span> · <strong>Marc.AI</strong> · Due Friday 3/13</div>

<div class="slide-section-label">具体内容</div>

- 在 Marc.AI 业务服务中实现 content generation tool，基于分析结果生成营销内容
- nanobananaimg 或其他内容生成 API 作为独立的 MCP 服务，Marc.AI 通过 MCP 协议调用这些服务进行内容生成（文案、标题、描述等）
- 支持多种内容类型：产品描述、广告文案、社交媒体帖子、邮件营销内容
- 根据用户需求与 reasoning 结果，生成符合品牌调性的营销内容
- 将 Marc.AI content generation tool 集成到 NyxID MCP 服务，NyxID MCP 实现 agent 调用该 tool 的能力


***

<div class="slide-section-label">验收标准</div>

- 内容生成 MCP 服务（nanobananaimg MCP 服务等）独立部署成功
- Marc.AI 成功通过 MCP 协议调用内容生成 MCP 服务生成营销内容
- 生成内容符合用户需求与品牌调性
- 支持多种内容格式输出
- Marc.AI content generation tool 成功集成到 NyxID MCP 服务，NyxID MCP 实现 agent 调用该 tool，Aevatar agent 可通过 NyxID MCP 正常调用

---

## 4. Marc.AI: User Output & Integration

<div class="slide-meta"><span class="owner-tag">@louis</span> · <strong>Marc.AI</strong> · Due Friday 3/13</div>

<div class="slide-section-label">具体内容</div>

- 完成 Marc.AI 业务服务端到端流程整合：scraping → reasoning → generation → output
- 设计用户友好的输出格式（结构化 JSON、Markdown、可视化报告等）
- 实现错误处理与用户反馈机制
- 完成所有 Marc.AI tools 集成到 NyxID MCP 服务的端到端测试
- 完成 NyxID MCP 服务中 agent 调用 tools 的端到端测试与文档编写
***

<div class="slide-section-label">验收标准</div>

- 所有独立 MCP 服务（web search tool、cheerio、sentiment analysis、keyword extraction、content generation 等）独立部署成功
- Marc.AI 业务服务端到端流程完整可用（输入 → 输出），成功通过 MCP 协议调用所有独立 MCP 服务
- 所有 Marc.AI tools（scraping、reasoning、generation）成功集成到 NyxID MCP 服务
- NyxID MCP 服务成功实现 agent 调用所有 Marc.AI tools 的能力
- Aevatar agent 可通过 NyxID MCP 完整调用所有 Marc.AI tools
- 输出格式清晰、易读、可复用
- 错误处理完善，用户体验良好
- 文档完整（独立 MCP 服务文档 + Marc.AI tools 文档 + NyxID MCP 服务集成文档），便于其他成员使用
