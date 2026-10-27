# Codex Skills

这里保存 2026-10-27 本机在用的 23 个 Codex 技能，包含完整的 `SKILL.md`、参考资料和脚本，方便备份、审阅和复用。

## 安装

需要 Node.js。安装全部技能：

```bash
npx skills add hoxiix/codex_skill -g -a codex
```

只安装一个技能：

```bash
npx skills add hoxiix/codex_skill --skill springboot-patterns -g -a codex
```

也可以把 `skills/<技能名>` 整个目录复制到 `~/.agents/skills/`。

## 技能清单

| 技能 | 用途 |
|---|---|
| [api-and-interface-design](skills/api-and-interface-design/SKILL.md) | API、模块边界和接口契约设计 |
| [documentation-and-adrs](skills/documentation-and-adrs/SKILL.md) | 架构决策记录、接口文档和维护文档 |
| [electron](skills/electron/SKILL.md) | Electron 主进程、IPC、安全和打包 |
| [find-skills](skills/find-skills/SKILL.md) | 搜索、评估并安装社区 Agent Skill |
| [frontend-ui-engineering](skills/frontend-ui-engineering/SKILL.md) | 前端界面工程、响应式布局和无障碍 |
| [hallmark](skills/hallmark/SKILL.md) | 新网站和新页面的视觉设计 |
| [impeccable](skills/impeccable/SKILL.md) | 全流程前端设计、审计、打磨、设计系统和原生界面 |
| [java-coding-standards](skills/java-coding-standards/SKILL.md) | Java 命名、不可变对象、异常和依赖注入规范 |
| [jpa-patterns](skills/jpa-patterns/SKILL.md) | JPA/Hibernate 实体、关系、事务和 N+1 处理 |
| [memory-compact](skills/memory-compact/SKILL.md) | 审查、合并和压缩长期记忆 |
| [mysql](skills/mysql/SKILL.md) | MySQL/InnoDB 表设计、索引、查询和事务 |
| [observability-and-instrumentation](skills/observability-and-instrumentation/SKILL.md) | 日志、指标、追踪和告警 |
| [performance-optimization](skills/performance-optimization/SKILL.md) | 前端、后端和数据库性能优化 |
| [planning-with-files](skills/planning-with-files/SKILL.md) | 用文件保存多步骤任务的计划和进度 |
| [security-and-hardening](skills/security-and-hardening/SKILL.md) | 安全审计、输入校验、依赖和隐私 |
| [session-memory](skills/session-memory/SKILL.md) | 跨会话保存本地 Markdown 记忆 |
| [springboot-patterns](skills/springboot-patterns/SKILL.md) | Spring Boot 分层架构、REST、DTO 和异常处理 |
| [springboot-security](skills/springboot-security/SKILL.md) | Spring Security、JWT、CORS、CSRF 和密钥管理 |
| [uni-app](skills/uni-app/SKILL.md) | uni-app 页面、组件、路由和条件编译 |
| [uniapp-x](skills/uniapp-x/SKILL.md) | uni-app x、UTS、uvue 和平台差异 |
| [vue-best-practices](skills/vue-best-practices/SKILL.md) | Vue 3 Composition API、组件和测试规范 |
| [wechat-miniprogram](skills/wechat-miniprogram/SKILL.md) | 微信小程序编译、预览、自动化和联调 |
| [writing-humanizer-zh](skills/writing-humanizer-zh/SKILL.md) | 中文写作去除 AI 生成痕迹 |

## 说明

- 这些技能来自公开仓库，许可和出处见 [SOURCES.md](SOURCES.md)。
- `session-memory` 是为本机工作流编写的本地技能。
- `find-skills` 依赖 Node.js 22.20 及以上版本，通过 `npx skills find` 和 `npx skills add` 使用。
- `impeccable` 的引擎二进制不纳入仓库，首次运行时会按平台自动下载；仓库只保留可审阅的 skill、参考文档和脚本。
- 已移除的英文版 `humanizer` 和旧版 `pdf` 副本没有收录；PDF 使用 Codex 插件自带的新版。
- 技能会以当前 Agent 权限运行，安装前请先阅读对应的 `SKILL.md` 和脚本。
