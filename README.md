# Crouton Alpha — Landing Page

Astro 静态单页。**主入口为 OpenCode 原生模型**，OpenRouter 仅作备选。

## 调研来源（2026-11-08）

### OpenCode（主入口）
- 模型：**Crouton Alpha Free**，ID `crouton-alpha-free`，provider `opencode`
- 2026-11-03 在 OpenCode Console + Go 上线；`/models` 中直接选用，无需经 OpenRouter
- 上下文 1,048,576，最大输出 270,000，推理等级 minimal→max，$0/$0 限时免费
- 端点：`https://opencode.ai/inference/openai/v1`（openai-responses）
- 用量（opencode.ai/data）：上线首周 Token 排名 #8，近 2 个月 1.4T tokens、30K 用户、335,380 会话
- 数据：免费期收集数据保留 30 天，不用于训练；地区限制：欧盟、中国（含港澳）、俄罗斯、巴基斯坦等不可用

### OpenRouter（备选）
- 模型 ID `stealth/crouton-alpha`，2026-11-03 同日上线
- 上下文 1,048,576，最大输出 943,718（与 OpenCode 版不同）
- 定位：轻量模型，为可扩展编码、Agentic 与多模态工作流而生；Agent 子任务、工具调用、文档分析

### 开发方
两边均标注匿名 stealth，无公司认领。社区推测指向 Meta Muse 但 token 计数不匹配，身份未定，本页不作断言。

## 运行

```bash
npm install
npm run dev     # http://localhost:4321
npm run build   # 生成 dist/
npm run preview # 预览构建产物
```
