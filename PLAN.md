# 个人网站内容调整 — 实施计划

## Context（背景）

**问题**：现有的 `c:\Users\李打爷的电脑\personal-website` 网站使用虚构人设"沈牧之"和虚构项目内容（6 个 demo 项目、5 条戏剧化信念、占位联系方式）。这与李知旺的真实身份和经历不符。

**目标**：基于三份准备材料（`实习准备/` + `ai学习/` + `AI-Agent-Hub/`），将网站改造为面向 **AI Agent 实习求职** 的真实个人展示网站。重点突出：MCP 协议先行实践、Multi-Agent 架构能力、8+ 真实项目、5 平台验证 / PyPI 发布等量化亮点。

**用户决策**（已确认）：
- ✅ 设计风格：**保留档案室/2099 美学，微调**（牛皮纸/工业橙/打字机保留，去戏剧化）
- ✅ Featured 项目：**4 个都放**（arcgis-agent / project-manager-agent / zhuochong / langchain-langgraph-projects）
- ✅ 结构变更：新增 **Achievements 板块** + 修改 Hero 副标题循环词组 + 重写 Timeline
- ✅ 联系方式：GitHub + 邮箱 + 简历下载链接
- ✅ 简历下载：李知旺_AI_Agent 实习简历（PDF/HTML）
- ✅ 实验残篇：重写为真实内容
- ✅ 邮箱地址：**18797734820@163.com**
- ✅ Skills 调整：**AI 框架/平台 + AI 工具链合并**为"日常开发工具"（OpenClaw / Claude Code / Codex / Trae IDE / Trae Solo / WorkBuddy）
- ✅ 新增 Skills 板块：**知识库管理工具**（Notion / Obsidian / IMA / OneNote）
- ✅ 文案调整：结束文案/自我介绍/宣言 注重**经验沉淀**和**个人积累**

## 关键文件清单

```
c:\Users\李打爷的电脑\personal-website\          # 5 个核心文件
├── index.html      (19,611 字节)  ← 主要修改（Hero / Projects / SHARDS / 新增 Achievements / Footer）
├── about.html      (14,914 字节)  ← 主要修改（基本信息 / 5 段 prose / Timeline / 能力矩阵）
├── style.css       (24,476 字节)  ← 微调（如需）
├── about.css       (10,683 字节)  ← 微调（如需）
└── script.js       (13,421 字节)  ← 微调（phrases 数组）

简历源文件：
C:\Users\李打爷的电脑\Documents\Obsidian Vault\实习准备\03-简历\李知旺_AI_Agent实习简历.pdf
（需复制到 website 根目录作为下载资源）
```

## 实施步骤

### Step 1: 复制简历文件到网站根目录
将 `李知旺_AI_Agent实习简历.pdf` 从 Obsidian 复制到 `c:\Users\李打爷的电脑\personal-website\`，作为可下载资源。

### Step 2: 修改 `index.html`

#### 2.1 顶部 <title> + 头部
- 旧：`ARCHIVE / 2099 — 作品档案`
- 新：`李知旺 — AI Agent 工程师 / 作品档案`

#### 2.2 Hero 主标题
- 旧：`我是 **沈牧之**`
- 新：`我是 **李知旺**`

#### 2.3 宣言文案
- 旧：田野笔记主题（独立开发者）
- 新：工程笔记主题（AI Agent 开发者），**强调经验沉淀与个人积累**：
  > "这不是一份简历，是一份**沉淀笔记**。记录我用 LangChain 凿出的痕迹、用 MCP 协议搭起的桥梁——以及那些*在反复试错中积累下来的、属于我自己的工程直觉*。每一个项目，都是一次新的沉淀。"

#### 2.4 统计数字（4 个数字）
- 旧：42 个项目 / 1700 次 commit / 13 种语言 / ∞ 个未完结（虚构）
- 新：**强调积累与沉淀**：8+ AI Agent 项目 / 600+ 测试用例 / 4 MCP Server / 27+ AI 工具评估

#### 2.5 Projects 板块（§01 作品索引）
**Featured 4 个**（保留 featured 视觉权重，状态标签保持 LIVE / DEV / STABLE 风格）：
| # | 标题 | 状态 | 技术栈 | 核心描述 |
|---|------|------|--------|----------|
| #001 | **arcgis-agent** | ● LIVE | Python · FastAPI · MCP · arcpy | AI Agent CLI for ArcGIS Pro。33 MCP Tools + Click CLI + FastAPI REST + SSE 三重暴露。248 单元测试，**已发布 PyPI** |
| #002 | **project-manager-agent** | ◐ DEV | Python · FastMCP · NetworkX · ChromaDB · DeepSeek | 5 Agent 协作（Coordinator+4 专业 Agent），黑板模式共享状态。MCP Server（10 Tools + 3 Resources + 3 Prompts），**5 平台验证通过** |
| #003 | **zhuochong** | ○ STABLE | PySide6 · OpenAI/Anthropic SDK · Edge-TTS | 智能桌面宠物。4 层架构，27 模块，269 测试，77% 覆盖率。Python 3.10/3.11/3.12 CI 矩阵 |
| #004 | **langchain-langgraph-projects** | ○ STABLE | LangChain · LangGraph · ChromaDB · FastAPI | 4 子项目 ~6000 行：RAG 问答（HyDE+Multi-Query+Reranking）、学习路径状态机、统一后端、文档加载器 |

**Other 项目 4 个**：
| # | 标题 | 状态 | 技术栈 | 描述 |
|---|------|------|--------|------|
| #005 | mcp-tts-ffmpeg | ▲ EXP | Python · FastMCP · MOSS-TTS · FFmpeg | 9 个 MCP Tools + 故事视频生成器 |
| #006 | NovelForge | ○ STABLE | Electron · Vue 3 · FastAPI · Neo4j | AI 辅助小说创作平台，**GitHub 854⭐** |
| #007 | pipeline-deploy | ○ STABLE | Streamlit · pandas · scikit-learn | 端到端数据分析 Web 应用 |
| #008 | tigang-helper | ▲ EXP | Next.js 14 · MediaPipe · PWA | 盆底肌训练 PWA |

**In Progress 3 个**（可作为 SHARDS 上方的"进行中"区块）：
- AI Hub CLI（统一 AI 工具管理器，5/26-6/8）
- Brain RAG（个人知识库搜索引擎，6/9-6/29）
- Code Sentinel（AI 代码审查 Agent，6/30-7/20）

**链接处理**：
- Featured GitHub：`https://github.com/lzw-cjs/项目名`
- #001 PyPI：`https://pypi.org/project/arcgis-agent/`
- Other 项目：GitHub 链接（如有）

#### 2.6 实验残篇板块重写（§02 SHARDS）
6 个真实的小项目/学习记录，保留"碎片"美学：

| 编号 | 标题 | 日期 |
|------|------|------|
| S/017 | 飞书 CLI 集成实战 | 2026·05 |
| S/022 | Pydantic AI Agent 探索 | 2026·05 |
| S/031 | Claude Code Hook 自动化 | 2026·04 |
| S/044 | MCP 协议源码阅读 | 2026·04 |
| S/052 | ArcGIS arcpy 椭球面积脚本 | 2025·11 |
| S/063 | Edge-TTS 工具封装 | 2025·10 |

> 链接可用 `href="#"`（占位即可），或链接到对应 GitHub 仓库

#### 2.7 新增 Achievements 板块（§03 成就 / ACHIEVEMENTS）
**位置**：在 Projects 和 SHARDS 之间（即 §02 与 §03 调整，SHARDS 改为 §04）

**样式**：参考现有作品卡片视觉，使用 3-4 列网格，每个成就卡片包含：
- 图标 / emoji
- 标题
- 简短描述
- 量化数字（高亮）

**内容（10 项）**：

| 类别 | 标题 | 关键数据 | 描述 |
|------|------|----------|------|
| 🏆 竞赛 | 挑战杯院级二等奖 | 2024.03 | 团队项目 |
| 🥇 创业 | 三创赛项目负责人 | 2025.04 | 农产品竞品市场研究 |
| 📦 发布 | arcgis-agent PyPI 发布 | v0.1.0 | 个人首个 PyPI 包 |
| 🛠️ MCP | 4 个自建 MCP Server | 33+ Tools | GIS/项目管理/多媒体/社交 |
| ✅ 验证 | MCP 5 平台验证 | 5/5 | Claude Code/Desktop/Cursor/Trea/OpenClaw |
| 🤖 AI 工具 | 27+ AI 编程助手评测 | 27+ | Cursor/Claude Code/Cline/Trae... |
| 📊 项目 | 8+ AI Agent 项目 | 6+ 主要 | RAG/Multi-Agent/桌面/Web 全覆盖 |
| 🧪 测试 | 600+ 测试用例 | 248+269+54+... | arcgis-agent/zhuochong/project-manager |
| 📚 GIS | 3000+ ArcGIS 国土空间规划文件 | 3K+ | DEM/遥感/矢量数据 |
| 🎓 领导力 | 大创 / 三创 / 互联网+ 项目负责人 | 3+ | 多次 |

#### 2.8 Footer 联系方式
- EMAIL：`mailto:18797734820@163.com`（用户已提供）
- GITHUB：`https://github.com/lzw-cjs` + 显示 `lzw-cjs`
- RESUME（新增）：`李知旺_AI_Agent实习简历.pdf` 下载链接
- 清理：删除 RSS 和 PGP 占位符

### Step 3: 修改 `about.html`

#### 3.1 <title> + 头部
- 旧：`档案 // 关于此人 — 沈牧之`
- 新：`档案 // 关于此人 — 李知旺`

#### 3.2 基本信息栏
| 字段 | 旧值 | 新值 |
|------|------|------|
| NAME | 沈牧之 | **李知旺** |
| ROLE | 独立开发者 / 设计师 | **AI Agent 全栈开发者** |
| BASED | 上海 · 31.23°N | **深圳（求职）· 湖南（学校）** |
| GMT+8 | 晚上 10 点后效率峰值 | （保留或改为"代码由 AI 协作，70%+ 自动生成"） |
| DRINKS | 冰美式 / 单一麦芽 | 冰美式 / 单一麦芽（可保留） |
| + 新增 | — | **GITHUB: lzw-cjs** |

#### 3.3 §I 我是谁（重写）
使用准备材料中的"个人简介长版"，**结尾强调经验沉淀与个人积累**：
> AI Agent 全栈开发者，独立完成 6 个 AI Agent 项目，覆盖 Multi-Agent 协作、RAG 知识库、MCP 协议、桌面应用、数据分析全链路。核心技术栈：LangChain + LangGraph + FastMCP + FastAPI。最新项目基于 Multi-Agent 架构开发了项目管理助手，并用 FastMCP 封装为 MCP Server（10 Tools + 3 Resources + 3 Prompts），已在 Claude Code、Claude Desktop、Cursor、Trea、OpenClaw 5 个平台验证；完成产品化交付：54 个 pytest 测试用例（核心覆盖率 85%+）、Gradio Web Demo、GitHub Actions CI/CD。同时具备 ArcGIS Pro 国土空间规划项目能力。
>
> 专业是人文地理与城乡规划，从国土空间规划跨界到 AI Agent 工程。这种"地理信息 × AI"的交叉背景，让我对智慧城市、空间数据等垂直领域的 AI Agent 应用有更深的理解。
>
> **我相信代码是写给自己未来的笔记**——每一次提交、每一段注释、每一份 README，都是未来某个凌晨三点需要它们的人（包括我自己）的路标。我用 Notion / Obsidian / IMA / OneNote 管理日常积累，把学习路径、项目复盘、踩坑记录沉淀成可检索的"第二大脑"。

#### 3.4 §II 我相信什么（重写 5 条，去戏剧化，**强调积累**）
1. **代码是写给人看的**，顺便能被机器执行。优雅优先于聪明。
2. **好工具应该消失**。当用户感觉不到工具存在，它才真正工作。
3. **AI 是新的协作者**。架构决策由人做，代码实现可以与 AI 协作完成。
4. **沉淀比聪明更重要**。把每天学到的东西写成笔记，半年后你会感谢自己。
5. **跨界是优势**。从国土空间规划到 AI Agent，地理 × 技术的交叉给了我独特的视角。

#### 3.5 §III 轨迹（重写 Timeline，**突出每个阶段的积累**）
| 年份 | 标题 | 描述 |
|------|------|------|
| 2026 | 沉淀与出发 | 6+ AI Agent 项目系统沉淀，MCP 协议先行实践，PyPI 发布 arcgis-agent——把过去两年零散的项目整合成可讲述的工程故事 |
| 2025 | 技术爆发与积累 | 完成 zhuochong、project-manager-agent 等核心项目；Claude Code 深度定制（33 Agent + 80 Skill）；Obsidian 沉淀 100+ 笔记 |
| 2024 | 跨界探索与起步 | 挑战杯院级二等奖；三创赛项目负责人；开始系统性学习 LangChain、LLM，逐步搭建个人技术知识库 |
| 2023 | 大学起点 | 湖南财政经济学院 · 人文地理与城乡规划 · 参加青马工程 · 写下第一份学习笔记 |

#### 3.6 §IV 能力矩阵（重写，**新增"日常开发工具"和"知识库管理"两个板块**）

| 技能 | 等级 | 熟练度 | 说明 |
|------|------|--------|------|
| AI Agent 工程 | LV.5 | 90% | LangChain · LangGraph · Multi-Agent · MCP |
| Python 工程化 | LV.5 | 88% | FastAPI · pytest · CI/CD · PyPI 发布 |
| 后端 / API 设计 | LV.4 | 80% | FastAPI · Flask · SSE · asyncio |
| 数据 / 地理信息 | LV.3 | 70% | ArcGIS Pro · pandas · 国土空间规划 |
| 前端 / 桌面 | LV.3 | 65% | Next.js · PySide6 · Electron · Vue |
| **日常开发工具** | LV.5 | 85% | **OpenClaw** · **Claude Code** · **Codex** · **Trae IDE** · **Trae Solo** · **WorkBuddy** |
| **知识库管理** | LV.4 | 80% | **Notion** · **Obsidian** · **IMA** · **OneNote** |
| 写作 / 表达 | LV.3 | 60% | 技术博客 · 文档 |

> 说明：原来的"AI 框架/平台"和"AI 工具链"两个分类**已合并为"日常开发工具"**，体现"以 AI 为主要编程伙伴"的工作流。

#### 3.7 §V 如何联系我（重写，**强调沉淀与积累的态度**）
> 我相信"工程是慢慢沉淀出来的"。如果你正在做 AI Agent、LLM 应用或 MCP 生态相关的事，欢迎邮件打扰——我愿意和你聊一聊我踩过的坑、沉淀过的笔记、以及那些还在路上的想法。
>
> 深圳地区 3-6 个月可全职实习，每周 3-5 天。
>
> 也欢迎看看我的 [GitHub](https://github.com/lzw-cjs) 和 [简历](#)。

签名：`— 李知旺` / 写于深圳（求职路上，也是积累路上）

### Step 4: 修改 `script.js`

**打字机 phrases 数组**（替换为 AI Agent + 经验沉淀相关词组）：
```js
const phrases = [
  '做 AI Agent。',
  '让 Claude 调用我的工具。',
  '用 MCP 协议重塑工作流。',
  '在 5 个 AI 工具间穿梭。',
  '从国土空间规划到 LLM 工程。',
  '把每次踩坑都写成笔记。'
];
```

**统计数字动画目标值**（如有相关逻辑）：
- 旧：42 / 1700 / 13 / ∞
- 新：8 / 4 / 27 / 600

### Step 5: 微调 `style.css` 和 `about.css`（按需）

仅在以下情况触发：
- Achievements 板块需要新样式
- Hero 副标题需要新动画（如果原 phrases 数量变化）

如果直接复用现有卡片样式，则**无需修改** CSS。

### Step 6: 本地验证

**预览方式**：
- 直接双击 `index.html` 用浏览器打开
- 或运行 `python -m http.server 8000`（在 website 目录）

**检查清单**：
- [ ] 主页 Hero 显示"李知旺"和 AI Agent 主题
- [ ] 打字机循环显示新词组
- [ ] 统计数字动画正确
- [ ] Projects 8 个项目 + 状态标签 + 链接正确
- [ ] SHARDS 6 个真实碎片
- [ ] Achievements 板块正确显示
- [ ] Footer 邮箱/GitHub/简历下载链接有效
- [ ] about.html 基本信息、5 段、Timeline、能力矩阵全部更新
- [ ] 移动端响应式正常（< 768px）
- [ ] Konami 彩蛋（↑↑↓↓←→←→BA）仍可触发
- [ ] 简历 PDF 可正常下载

## 风险与依赖

**阻塞项**（已解决）：
- ✅ **邮箱地址**：18797734820@163.com（用户已提供）

**依赖**：
- 简历 PDF 文件需要从 Obsidian 复制到 website 根目录
- 所有 GitHub 链接以 `github.com/lzw-cjs` 开头

**已规避的风险**：
- ✅ 设计风格统一（保留档案室美学）
- ✅ 内容真实（基于三份准备材料）
- ✅ 项目链接已知（GitHub 用户名 lzw-cjs）

## 实施顺序

1. **【批准后立即执行】** 复制当前 plan 文件到项目目录 `c:\Users\李打爷的电脑\personal-website\PLAN.md`（用户要求项目内可访问）
2. 复制简历 PDF 到 `c:\Users\李打爷的电脑\personal-website\李知旺_AI_Agent实习简历.pdf`
3. 一次性修改 `index.html`（Hero + Projects + SHARDS + 新增 Achievements + Footer）
4. 一次性修改 `about.html`（基本信息 + 5 段 prose + Timeline + 能力矩阵）
5. 修改 `script.js`（phrases 数组 + 统计数字）
6. 按需微调 `style.css` / `about.css`
7. 本地浏览器验证

## 工作量估算

- 5 个文件修改
- index.html: 约 15-20 个具体编辑点（Hero + 4 Featured + 4 Other + 3 In Progress + 6 SHARDS + 10 Achievements + Footer）
- about.html: 约 10-15 个编辑点（基本栏 + 5 段 + Timeline + 矩阵）
- script.js: 2 处（phrases + 统计数字）
- CSS: 按需 0-5 处
- **总工作量**：中等，约 30-40 处编辑
