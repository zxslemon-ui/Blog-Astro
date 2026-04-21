---
title: 'AI 热点监控工具项目'
description: '这是一套以 AI 编程实战 为核心的项目教程，基于 Express 5 + React 19 + OpenRouter + Socket.io，用 AI 编程的方式从 0 到 1 开发一个《AI 热点监控工具》，带你亲身体验 AI Vibe Coding 的完整工作流，学会用 AI 快速做出实用的提效工具！'
pubDate: 'march 30 2026'
heroImage: '../../assets/blog/ai-monitor/cover.png'
---
## 一、项目介绍
这是一套以 AI 编程实战 为核心的项目教程，基于 Express 5 + React 19 + OpenRouter + Socket.io，用 AI 编程的方式从 0 到 1 开发一个《AI 热点监控工具》，带你亲身体验 AI Vibe Coding 的完整工作流，学会用 AI 快速做出实用的提效工具！

<img src="https://cdn.nlark.com/yuque/0/2026/webp/66845298/1776772150632-d7de14fc-b46d-4ed7-a87e-e1a788732042.webp" width="2550" title="" crop="0,0,1,1" id="u2e51a14a" class="ne-image">

## 二、项目功能演示
### 配置监控关键词
用户输入要监控的关键词，比如"Vibe Coding”、"Claude"等，系统会自动开始监控。支持激活/暂停单个关键词

<img src="https://cdn.nlark.com/yuque/0/2026/webp/66845298/1776772271584-efacf72e-0e4b-4781-8763-83233a9bd897.webp" width="2292" title="" crop="0,0,1,1" id="u8ca07f96" class="ne-image">

### AI 自动抓取和分析热点
系统每30分钟自动从Twitter、Bing、HackerNews、搜狗、B站、微博等8+个信息源抓取内容，利用AI进行查询扩展、真假识别、相关性分析和智能摘要，过滤低质量内容后展示在信息流中。

<img src="https://cdn.nlark.com/yuque/0/2026/webp/66845298/1776772331418-1230cbac-3afe-42f8-8d04-a5ac0c4cc4b9.webp" width="2248" title="" crop="0,0,1,1" id="u7565d955" class="ne-image">

### 多维度筛选和排序
支持按信息来源、重要性、时间范围进行筛选，支持按热度综合、相关性、发布时间排序，帮助用户快速定位需要的热点信息。

<img src="https://cdn.nlark.com/yuque/0/2026/webp/66845298/1776772361550-aa3ca41a-ef64-4bf5-bcb2-a1896429bf5d.webp" width="2238" title="" crop="0,0,1,1" id="ub8aa3b09" class="ne-image">

### 全网搜索
除了监控关键词的实时热点流外，还可以直接搜索特定的关键词，从全网获取信息：

<img src="https://cdn.nlark.com/yuque/0/2026/webp/66845298/1776772395057-566120ef-4e25-40fe-b42e-da9fe0d1964d.webp" width="2182" title="" crop="0,0,1,1" id="u02a34e11" class="ne-image">

### 实时通知
通过WebSocket实时推送热点通知，高重要性的热点还会通过邮件通知：

<img src="https://cdn.nlark.com/yuque/0/2026/webp/66845298/1776772430301-c4f21f7e-3fbd-4ab4-8d93-661ebe0796d2.webp" width="2208" title="" crop="0,0,1,1" id="u95082919" class="ne-image">

### Agent Skills技能包
将热点监控能力封装为标准的 Agent Skills，安装后在 Cursor、VSCode Copilot、Claude Code 等 AI 编程工具中都能使用：

<img src="https://cdn.nlark.com/yuque/0/2026/webp/66845298/1776772480399-98ea7b91-70bf-42bd-b896-1871fed9410a.webp" width="2740" title="" crop="0,0,1,1" id="uc8376147" class="ne-image">

## 三、项目收获
本项目选题新颖，紧跟AI编程时代，以实用工具开发为导向，区别于增删改查的烂大街项目。

快速掌握 AI 编程的核心工作流：需求分析 → 方案设计 → 编码开发 → 测试验证 → 前后端优化 → 功能扩展 → Skills 开发，让你真正体验企业级AI编程的全流程。

从这个项目中你可以学到：

+ 如何用 AI 编程从 0 到 1 开发一个完整的工具
+ 如何安装和使用 MCP 增强 AI 能力
+ 如何安装和使用 Agent Skills 提升 AI 编程质量
+ 如何从多个信息源（Twitter、Bing、HN、B 站等）聚合抓取内容
+ 如何通过 OpenRouter 接入 AI 大模型，实现智能内容审核
+ 如何实现查询扩展（QueryExpansion），提高信息检索的召回率
+ 如何基于 Socket.io 实现 WebSocket 实时推送
+ 如何使用 Aceternity UI 打造炫酷的科技感前端界面
+ 如何开发标准化的 Agent Skills 技能包，并在多种 AI 工具中验证
+ 如何在 AI 编程中进行人工确认、版本控制和迭代优化

## 四、核心业务流程
### 热点监控主流程
整个项目的核心流程比较复杂：用户配置关键词 → 定时任务触发 → AI 查询扩展 → 多源抓取 → 去重过滤 → AI 分析 → 入库 → 实时推送/邮件通知。

<img src="https://cdn.nlark.com/yuque/0/2026/png/66845298/1776773071969-cdef40e9-b53c-415b-8235-5ef015e10379.png" width="784" title="" crop="0,0,1,1" id="ub9a1e97b" class="ne-image">

### Web 端使用流程
用户使用网页来监控热点：

<img src="https://cdn.nlark.com/yuque/0/2026/png/66845298/1776773120255-52f873fe-570b-4e41-b8a1-a1bde4e3c750.png" width="1201.6" title="" crop="0,0,1,1" id="u4447ef10" class="ne-image">

### Agent Skills 使用流程
用户安装热点监控Skills后，可以直接在AI编程工具中通过自然语言触发热点搜索和分析：

<img src="https://cdn.nlark.com/yuque/0/2026/png/66845298/1776773128870-067009f2-64ce-476a-8aee-50674e9f5936.png" width="1140" title="" crop="0,0,1,1" id="u651483c7" class="ne-image">

## 五、项目功能梳理
该项目功能丰富，涵盖关键词管理、热点采集和分析、信息展示和筛选、实时通知系统、全网信息源搜索、Agent Skills 六大模块，20+ 功能点，覆盖了从信息采集、AI 智能分析到实时推送通知的完整热点监控闭环。

<img src="https://cdn.nlark.com/yuque/0/2026/webp/66845298/1776773217582-3020a209-3856-4b18-85ff-733359f711c7.webp" width="2252" title="" crop="0,0,1,1" id="ub8516f42" class="ne-image">

关键词管理模块：

+ 添加 / 删除监控关键词
+ 激活 / 暂停单个关键词
+ AI 自动扩展查询变体（Query Expansion）
+ B 站账号智能检测

热点采集与分析模块：

+ 8+ 数据源并行采集（Twitter、Bing、搜狗、B 站、微博、HackerNews 等
+ AI 内容真实性验证（过滤标题党和虚假内容）
+ AI 相关性评分（0-100分）
+ AI 重要性分级 （urgent / high / medium / low）
+ AI 智能摘要生成
+ AI 相关性分析理由

信息展示与筛选模块：

+ 热点雷达仪表盘（实时统计数据）
+ 5 种排序方式（最新发现 / 最新发布 / 重要程度 / 相关性 / 热度综合）
+ 多维度筛选（来源 / 重要性 / 关键词 / 时间范围）
+ 分页加载
+ 展开 / 折叠相关性分析详情
+ 一键跳转原文

通知系统模块：

+ WebSocket 实时推送
+ 邮件通知（仅 high / urgent 级别）
+ 站内通知管理（已读 / 未读）

全网搜索模块：

+ 全网关键词搜索
+ 多数据源聚合搜索结果

Agent Skills 模块：

+ 完全自包含的 AI 技能包
+ 支持 Cursor、VSCode Copilot、Claude Code 等多工具
+ Python 采集脚本 + 分析框架
+ 无需后端服务，开箱即用

## 六、技术选型
本项目以 Node.js 全栈 + TypeScript 为核心，前后端分离，涵盖多源爬虫数据采集、AI 大模型内容审核、WebSocket 实时推送、定时任务调度、Aceternity UI 科技感前端、Agent Skills 开发等实用技术，一个项目即可掌握工具类产品的核心技术栈。

<img src="https://cdn.nlark.com/yuque/0/2026/webp/66845298/1776773292276-ff29c9c6-40eb-46e0-8ad6-1696e08b7a1a.webp" width="2278" title="" crop="0,0,1,1" id="uf93c14cb" class="ne-image">

### 后端
+ ⭐ Express 5,Node.js Web框架，原生支持async/await
+ ⭐ TypeScript，类型安全开发
+ ⭐ PrismaORM，类型安全的数据库访问
+ SQLite，轻量级嵌入式数据库
+ ⭐ Socket.io,WebSocket实时通信
+ node-cron，定时任务调度
+ Nodemailer，邮件发送

### 前端
+ ⭐ React 19，前端UI框架
+ ⭐ Vite 7，新一代前端构建工具
+ ⭐ Tailwind CSS 4，原子化 CSS 框架
+ Framer Motion，React 动画库
+ ⭐ Aceternity UI 风格组件，科技感视觉动效
+ Socket.io-client，WebSocket 客户端
+ Lucide React，图标库

### AI相关
+ ⭐ OpenRouter API，统一接入 Al 大模型 （DeepSeek、Claude、GPT 等）
+ ⭐ AI 内容审核，真假识别 + 相关性分析 + 重要性分级 + 摘要生成
+ ⭐ Query Expansion，AI 驱动的查询扩展

### AI编程工具
+ ⭐ VSCode + GitHub Copilot，主力 Al 编程 IDE
+ ⭐ MCP插件：Firecrawl（网页抓取）、Context7（最新技术文档）
+ ⭐ Agent Skills：UI UX Pro Max （前端美化）、Skill Creator（技能开发）

## 七、架构设计
本项目采用前后端分离架构，前端使用 React + Vite ，后端使用 Express + Prisma，通过 REST API 和 WebSocket 通信。通过定时任务引擎来驱动多数据源采集和 AI 分析，Agent Skills 作为独立模块可在多种 AI 编程工具中复用。

<img src="https://cdn.nlark.com/yuque/0/2026/webp/66845298/1776774032860-0c833184-6d55-42fe-816b-718c71fedadd.webp" width="2238" title="" crop="0,0,1,1" id="uf582d6da" class="ne-image">

> 本小节内容主要包括：需求分析、VSCode + GitHub Copilot 环境配置、MCP 安装与配置（Firecrawl + Context7）、Agent Skills 安装（UI UX Pro Max + Skill Creator + Find Skills）
>

## 需求分析
---

作为一名对AI感兴趣的程序员，想要第一时间了解AI热点（比如AI大模型更行、新技术迭代），我不想通过手动收集相关信息，而是利用工具自动发现制定的热点变化、或者最新的热点新闻，并且及时给我发送通知。

💡该项目是一个轻量化的工具类需求，计划采用较为敏捷的开发方式，不介入过多人工介入和工程化

项目核心功能：

+ 用户手动输入要监控的关键词，当关键词相关的内容真的出现（注意利用AI识别假冒的内容），第一时间发送通知
+ 每隔一段时间，自动收集用户指定范围（比如“AI编程”）内的热点，并且能够让用户看到

产品的形式：

+ 响应式兼容的 Web 页面
+ 封装成 Agent Skills 技能，能够交给其他的AI来监控和发现热点

### 需求分析的技巧
对于工具类项目，需求分析的核心是抓住 用户痛点 和 使用场景，我的痛点很明确：手动搜索热点效率低、容易遗漏、无法 7*24 小时监控。

在做需求分析时，建议思考以下几个维度：

| 维度 | 问题 | 本项目的回答 |
| --- | --- | --- |
| 目标用户 | 谁会用这个工具？ | AI编程从业者、科技媒体从业者、投资人等需要追踪热点的人 |
| 核心价值 | 解决什么问题？ | 自动化热点发现，减少人工搜索时间 |
| 产品形态 | 用什么方式实现？ | 使用 Web 页面 + Agent Skills |
| 技术可行性 | 能否实现？ | 利用公开 API + 爬虫 + AI 分析，完全可行 |
| 优先级 | 先做什么？ | 先做 Web 端核心功能，再封装 Skills |


### 敏捷开发的使用场景
为什么本项目使用敏捷开发？因为它具有以下特征：

+ 需求明确且轻量：不是复杂的企业级系统，而且一个工具类产品
+ 快速迭代：可以先做出 MVP（最小可行产品），再逐步优化
+ 用户即开发者：我作为用户，可快速验证即反馈

敏捷开发的核心理念是”小步快跑“：先做出能用的版本，后续再不断迭代升级完善

## 环境准备
---

### VSCode 编程 IDE
### Github Copilot 编程助手
本项目使用 Agent 模式，让 AI 自主完成从方案设计到代码开发的完整流程，我们只需在关键节点进行人工确认

#### Copilot 现有工作模式
| 模式 | 说明 | 使用场景 |
| --- | --- | --- |
| 内联补全 | 在编辑器中实时提供代码建议 | 日常编码、写函数体 |
| Chat 对话 | 在侧边栏与 AI 对话 | 方案设计、问题排查 |
| Agent 模式 | AI 自主规划并执行多步骤任务 | 完整功能开发、代码重构 |


### Claude / GPT 大模型
#### 大模型选择建议
+ Claude sonnet / Opus：擅长代码生成和长上下文理解，对前端UI开发支持很好
+ GPT 系列：通用能力强，生态丰富
+ DeepSeek：国内模型，访问速度快，性价比高

本项目使用AI内置模型进行编程开发，同时使用OpenRouter介入AI大模型来做热点内容的智能分析（真假识别、相关性评分等）

两者角色的不同：

+ Opus 模型：负责写代码、生成方案
+ OpenRouter 接入的模型：负责运行时的内容分析，集成在使用的开发工具中

### 扩展工具
项目必备扩展工具包括 MCP 和 Agent Skills

#### 什么是MCP
<img src="https://cdn.nlark.com/yuque/0/2026/webp/66845298/1774512080737-e07e6f70-a148-406d-91ae-51424c75788a.webp" width="1102" title="" crop="0,0,1,1" id="u87d964fa" class="ne-image">

MCP 的全称是 Model Context Protocol （模型上下文协议），它定义了一套标准化接口，让 AI 模型能够与外部工具和数据源进行交互。可以把 MCP 理解为“万能插头”，只要工具实现了 MCP 协议，AI 就能直接调用的。可通过 [这篇文章](https://ai.codefather.cn/library/2010974694076256258) 来了解

本项目主要用到的MCP：

+ Firecrawl MCP：让 AI 能够抓取和解析网页内容
+ Context7 MCP：让 AI 能够获取最新的技术文档，避免使用过时的 API 和代码

#### 什么是 Agent Skills
<img src="https://cdn.nlark.com/yuque/0/2026/webp/66845298/1774513063742-3dcc6e48-6ae3-47d2-b233-a131725f311d.webp" width="1154" title="" crop="0,0,1,1" id="uc0df8d98" class="ne-image">

智能体技能。通过给 AI 准备的技能包，让 AI 快速学习使用各种专业技能，而不是每次重复输入提示词、编写脚本等等。可通过 [这篇文章](https://ai.codefather.cn/library/2013072104018264066) 来了解

本项目主要用到的Agent Skills：

+ UI UX Pro Max：专门用来美化前端页面的技能。本项目需要开发 Web页面，该技能可以使页面更好看。更多美化技巧，可以阅读 [这篇文章](https://ai.codefather.cn/library/2018146417167622146)
+ Skill Creator：能够帮你制作新的技能。因为我们要把工具封装成 Agent Skills 技能，所以用它来开发规范的技能，让各种 AI 编程工具都能识别

MCP 和 Agent Skills 有什么区别？

| 对比维度 | MCP | Agent Skills |
| --- | --- | --- |
| 本质 | 通信协议，连接 AI 与外部工具 | 知识包，教 AI 特定技能 |
| 运行方式 | 需要启动服务器进程 | 纯文件，无需额外进程 |
| 内容 | API 借口定义 | 提示词 + 脚本 + 参考资料 |
| 举例 | Firecrawl（网页抓取能力） | UI UX Pro Max（前端美化技能） |


二者可以协作使用

<img src="https://cdn.nlark.com/yuque/0/2026/webp/66845298/1774514291566-a794c0f9-7931-4d66-9bc0-29e53284393f.webp" width="1114" title="" crop="0,0,1,1" id="u9b44dc88" class="ne-image">

#### 安装 MCP
VSCode 中，在 AI 对话设置中，进入MCP服务器，搜索安装 MCP

<img src="https://cdn.nlark.com/yuque/0/2026/webp/66845298/1774515083629-eb629a6c-cd3d-485f-9d63-a91645bf5f89.webp" width="3022" title="" crop="0,0,1,1" id="u259908b4" class="ne-image">

#### 安装 Agent Skills
使用 Vercel 的 [Skills 工具](https://skills.sh/)，可以用一行命令帮你快速安装 AI 技能

通过 skills 工具安装 [find skills](https://skills.sh/vercel-labs/skills/find-skills) 技能，可以帮你搜索其他的技能

有了 find skills 这个技能后，就可以让 AI 帮我们安装需要的技能：

```markdown
请帮我安装技能 UI UX Pro Max 和 Skill Creator
```

#### 技能安装的本质
当你通过 `npx skills add`安装技能时，实际上发生了一下事情：

1. 从 GitHub 仓库下载技能文件（包含 `SKILLS.md`和相关资源）
2. 将文件复制到你本地的AI编程工具的技能目录中
3. AI 编程工具（ VSCode / Cursor 等）自动识别新增的技能

技能的核心是 `SKILL.md`文件，它告诉 AI：

+ 什么时候应该使用这个技能（触发条件）
+ 如何使用这个技能（操作步骤）
+ 有哪些可用的资源和脚本（辅助文件）

### 其他环境准备
+ Node.js

## 本节小结
在这一节中，我们完成了项目的需求分析和环境搭建：

1. 明确了需求：自动化热点监控 + 实时通知
2. 配置了开发环境：VSCode + GitHub Copilot
3. 安装了 MCP：Firecrawl + Context7
4. 安装了 Agent Skills：UI UX Pro Max + SkillCreator

下一节，我们将进入方案设计阶段，确认信息源、通知方式和 AI 对接方案，然后让 AI 根据方案自动生成代码，并完成功能测试验证
