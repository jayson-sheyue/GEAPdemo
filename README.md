# Gemini Enterprise 生态导览

静态站点，用来梳理 Google Cloud **Gemini Enterprise** 相关产品、组件和官方文档入口。面向产品、架构、开发和运营同学：先按使用者选产品线，再看组件、API、规格、治理与计费。

资料核对日期：**2026-09-29**。功能状态、区域、配额与价格会变化，请以链接的官方文档和 Cloud Console SKU 为准。本仓库是学习与对照用导览，不是 Google 官方文档。

## 三条产品线

| 产品线 | 面向谁 | 解决什么 | 入口 |
| --- | --- | --- | --- |
| **Agent Platform** | 开发与平台团队 | 构建、托管运行、治理和优化企业 Agent | `dist/platform.html` |
| **Gemini Enterprise** | 企业员工与管理员 | 搜索、助手、连接器、工作流与组织治理 | `dist/enterprise.html` |
| **Gemini Enterprise for CX** | 客户体验与坐席 | 客服/购物 Agent、评测部署、洞察与商业动作 | `dist/cx.html` |

首页 `dist/index.html` 用 Build → Scale → Govern → Optimize 概括生产链路，并给出选型对照。官方参考索引在 `dist/sources.html`。

## 本地预览

仓库是纯静态 HTML/CSS，没有构建步骤。

```bash
# 任选一种方式打开 dist/
open dist/index.html

# 或用本地 HTTP 服务（避免部分浏览器对 file:// 的限制）
python3 -m http.server 8080 --directory dist
```

浏览器访问 `http://localhost:8080/`。

`dist/` 为站点根目录；`.openai/hosting.json` 标明静态资源目录为 `dist`。

## 站点地图

```
dist/
├── index.html                 总览与选型
├── site.css                   子页共用样式
├── sources.html               官方文档索引
│
├── platform.html              Agent Platform 能力地图
├── platform-build.html        Build：模型、数据、Agent 构建
├── platform-scale.html        Scale：Runtime、会话、沙箱
├── platform-govern.html       Govern：身份、网关、策略
├── platform-optimize.html     Optimize：评测与可观测性
│
├── enterprise.html            Gemini Enterprise 产品地图
├── ge-search-data.html        搜索与数据
├── ge-assistant.html          Assistant 与个性化
├── ge-agents.html             Agents、Skills 与 Workflow
├── ge-admin-api.html          管理、安全、分析与 API
├── ge-developer.html          开发者工具与权益
│
├── cx.html                    Gemini Enterprise for CX
├── cx-build.html              构建对象
├── cx-tools.html              工具与 Toolsets
├── cx-evaluate.html           评测与优化
├── cx-deploy.html             渠道、语音与 API
├── cx-operate.html            Agent Assist、Insights、Commerce
└── cx-reference.html          监控、配额、地区与计费
```

## 怎么用这份导览

1. **先选产品线，不要混用三个入口。** 写代码、编排多 Agent、托管运行看 Agent Platform；员工检索与审批流看 Gemini Enterprise；面向消费者的客服/购物看 CX。
2. **再下钻组件页。** 每条子线按对象、规格、用法、边界展开，并链到对应官方专题。
3. **上线前回到官方页核对。** 预览/GA、区域、配额、模型和价格以 Google Cloud 文档为准。

常用官方入口：

- [Agent Platform overview](https://docs.cloud.google.com/gemini-enterprise-agent-platform/overview)
- [Gemini Enterprise docs](https://docs.cloud.google.com/gemini/enterprise/docs)
- [Gemini Enterprise for CX](https://docs.cloud.google.com/gemini-enterprise-cx)

## 许可与归属

页面内容整理自公开的 Google Cloud 产品文档与定价页，版权归原权利人所有。本仓库仅作索引与结构化导览。
