---
slug: zh-cn/real-world-development/app
title: "GitHub Copilot app"
authors:
  - geektrainer
lastUpdated: 2026-10-22
---

**[GitHub Copilot app](https://docs.github.com/copilot/concepts/agents/github-copilot-app)** 是一款基于 Copilot CLI 构建的桌面应用程序，可在专注的工作区中进行代理式开发。它提供并行代理会话、可切换的会话模式、共享画布，以及原生 GitHub 议题和拉取请求管理功能。其中包括 **Agent Merge**，可协助拉取请求完成变基、处理审查反馈、修复持续集成 (CI) 问题并合并。

本研讨会将带你完成 Tailspin Toys 中的一整套工作流：

1. 准备项目、安装应用、连接仓库，并了解工作区和预置的待办事项。
2. 添加一项小型星级评分更改，在浏览器中审查，并手动合并第一个拉取请求 (PR)。
3. 从筛选议题开始，在 **Plan** 模式中确定方案，在 **Autopilot** 模式中构建，然后在 **Interactive** 模式中审查。
4. 更新仓库指令，并将其应用于筛选功能。
5. 自定义现有的 `quality-checks` 技能，并使用它运行项目检查。
6. 添加 Playwright Model Context Protocol (MCP) 服务器，并在浏览器中探索筛选功能。
7. 创建质量保证 (QA) 自定义代理，用于审查需求、覆盖范围和验证证据。
8. 审查完整的筛选更改，并对第二个 PR 使用 Agent Merge。
9. 检查画布是否可用，然后使用 Database Explorer，创建并测试连接到仓库的分诊画布。如果缺少所需功能，请记录阻碍，并使用只读替代方案或继续完成总结。

为保持内容聚焦，你将创建两个 PR：一个用于星级评分，另一个用于筛选功能（包含指令更新、技能更新、QA 配置和测试）。每个 PR 都从更新后的 `main` 开始。筛选和质量工作流共用一个会话、工作树和分支，让你可以在探索各项工具时逐步扩展已有工作。最后的画布练习保留在自己的会话中，让你专注于创建和测试共享界面，而无需重复 PR 工作流。

## 课程

| 课程 | 主题 | 描述 |
|--------|-------|-------------|
| [0. 先决条件][ex0] | 设置 | 安装 Node.js 并创建 Tailspin Toys 项目副本 |
| [1. 安装 Copilot app][ex1] | 设置 | 安装应用、连接项目并熟悉工作区 |
| [2. 添加星级评分：快速改进][ex2] | 第一次更改 | 显示现有评分和 null 时的替代内容，然后合并第一个 PR |
| [3. 代理模式：Plan 和 Autopilot][ex3] | 代理模式 | 从议题规划功能，使用 Autopilot 构建，再用 Interactive 审查 |
| [4. 使用自定义指令引导 Copilot][ex4] | 上下文 | 探索并更新指令，然后将其应用于筛选功能 |
| [5. 自定义并使用质量检查技能][ex5] | 可重复检查 | 查看现有技能、更改报告格式并运行技能 |
| [6. 使用 Playwright MCP 验证功能][ex6] | 浏览器观察 | 通过 Customize 配置 MCP 并检查筛选行为 |
| [7. 创建并使用 QA 代理][ex7] | 需求和覆盖范围 | 创建并选择专用配置，然后收集最终验证证据 |
| [8. 创建并合并功能 PR][ex8] | 审查和合并 | 审查筛选、指令、技能、QA 配置和测试，然后对第二个 PR 使用 Agent Merge |
| [9. 探索和创建画布][ex9] | 协作 | 使用 Database Explorer，然后创建并测试连接到仓库的分诊画布 |
| [10. 总结和后续步骤][ex10] | 总结 | 回顾工作流、产出和更多资源 |

## 先决条件

参加本研讨会前，请确保具备以下条件：

- [ ] 拥有有效的 **Copilot Student、Pro、Pro+、Business 或 Enterprise** 计划的 GitHub 帐户
- [ ] 一台运行 **macOS、Linux 或 Windows** 的计算机
- [ ] 已在计算机上[安装 Git][install-git]

> [!TIP]
> 没有付费计划？经过验证的学生可以通过 [GitHub Education][callout-student-plan-education] 免费使用 GitHub Copilot。**Copilot Student** 计划包含本研讨会使用的代理、MCP、代码审查和 Copilot CLI 功能，因此可以完成所有课程。

> [!NOTE]
> Copilot app 在你的计算机上运行，而不是在 codespace 中运行。因此，[先决条件练习][ex0]会引导你在安装应用前安装 Node.js 并创建项目副本。

> [!NOTE]
> 如果使用 Copilot Business 或 Copilot Enterprise，管理员必须保持 **GitHub Copilot app** 策略处于启用状态。此策略与 Copilot CLI 策略相互独立。

## 开始

**[从先决条件开始 →][ex0]**

[ex0]: 0-prerequisites/
[ex1]: 1-install-copilot-app/
[ex2]: 2-add-star-rating/
[ex3]: 3-agent-modes/
[ex4]: 4-custom-instructions/
[ex5]: 5-agent-skills/
[ex6]: 6-mcp-playwright/
[ex7]: 7-qa-agent/
[ex8]: 8-create-pull-request/
[ex9]: 9-canvases/
[ex10]: 10-review/
[install-git]: https://github.com/git-guides/install-git
[callout-student-plan-education]: https://github.com/education/students
