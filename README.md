# 👋 Hi there, 我是 Zoe

![Go](https://img.shields.io/badge/Go-00ADD8?logo=go&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![AI](https://img.shields.io/badge/AI%20Agent-Eino-4B8BBE)
![RAG](https://img.shields.io/badge/RAG-Redis%20Stack-FF4438)

> 10年+后端开发 | Gopher | 高并发金融系统 | AI 工程化实践者  

---

## 🧑‍💻 关于我

- 🔭 技术栈：Go、Python、Java | 微服务、分布式事务、高并发架构
- 🤖 AI 方向：Agent 工作流编排（Eino）、RAG 混合检索、意图识别与实体链接、Function Calling
- 📊 数据工程：评测集构建、离线指标分析（Recall@K、NDCG）、链路耗时与 Token 统计
- 🧩 工程沉淀：Prompt 模板库、智能单元测试生成、自动化 PR 检查
- 🌱 当前探索：多模态 RAG、AI 短片

---

## 🚀 我的 AI 项目实践

### 📈 个股智能分析系统（AI Agent + RAG）

> 基于 Eino + Redis Stack 构建的投研助手，实现自然语言→结构化查询→多源数据检索→生成报告

- ✅ **意图理解层**：实体知识库（股票/指标/时间）+ 槽位组合规则 + 示例库检索，复杂查询准确率 86%
- ✅ **RAG 工程**：向量 + BM25 双路召回、RRF 融合、规则重排（标题/时效性/来源），Recall@5 从 0.4 提升至 0.72
- ✅ **可观测性**：链路耗时、Token 统计、离线评测集（50 条用例）
- ✅ **可复用工作流**：将 Agent 架构抽象为内部模板，新场景（如房产/电商匹配）可快速复制

[🔗 项目链接](https://github.com/zoe0806/stock-see)

---

### 🤖 风控编排系统（Risk Control Agent）

> 基于 CloudWeGo Eino 构建的可插拔风控编排引擎，支持跨境制裁筛查与股票订单风控两条流水线，提供统一审计与 HTTP 服务

- ✅ **多业务编排**：`RiskEngine` 根据 `business_type` 分发至 `EvaluateCrossBorderTransaction` / `EvaluateStockOrder`，共用审计与名单库（MySQL）
- ✅ **图编排实践**：使用 `compose.NewGraph` + Lambda 节点 + 条件分支，分别实现制裁筛查图和股票订单风险评分图
- ✅ **统一响应结构**：`ScreeningResult` 包含 `blocked`、`block_reason`、`risk_score` 等字段，便于下游系统消费
- ✅ **可观测性**：细粒度观测（每个节点耗时、输入输出）自动落审计库，支持按 `trace_id` 查询，不污染业务响应
- ✅ **配置化运行**：支持 HTTP 端点 `/v1/screen`，自动根据请求负载推断业务类型；内置健康检查

[🔗 项目链接](https://github.com/zoe0806/risk-control)


---

> 欢迎交流 AI 应用落地、后端架构、RAG 工程化等话题。
