# Project Map

一个帮助 Agent 规划并持续维护项目结构和上下文路由的 Skill。

**先识别边界，再设计结构。AGENTS.md 负责路由，CONTEXT.md 负责局部知识。**

适合整理已有项目、建立上下文地图，或在模块边界变化后更新相关说明。完整规则以 [SKILL.md](SKILL.md) 为准。

## 安装到 Codex

将本仓库克隆到 Codex 的 skills 目录，文件夹名为 `project-map`。

Windows PowerShell（默认目录）：

```powershell
git clone https://github.com/ATIpiu/project-map.git "$HOME\.codex\skills\project-map"
```

macOS / Linux（默认目录）：

```sh
git clone https://github.com/ATIpiu/project-map.git ~/.codex/skills/project-map
```

如果设置了 `CODEX_HOME`，请改用该目录下的 `skills/project-map`。安装后开启新的 Codex 会话。

## 使用

在目标项目中对 Codex 说：

```text
使用 $project-map 检查当前项目的模块边界，整理 AGENTS.md 与需要的 CONTEXT.md，让后续任务只读取相关上下文。
```

维护已有地图时：

```text
使用 $project-map 检查这次结构变化影响的上下文路由，更新失真的部分，并向上检查父级引用。
```

Skill 会根据真实职责和依赖判断结构；小项目保持简单，父级说明准确时停止更新。
