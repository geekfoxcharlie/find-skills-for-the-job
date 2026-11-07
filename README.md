# Find skills for the job

[![skills.sh](https://skills.sh/b/geekfoxcharlie/find-skills-for-the-job)](https://skills.sh/geekfoxcharlie/find-skills-for-the-job)

Find an Agent Skill for a job on [SkillPicker](https://skillpicker.xyz). Agent Skills are `SKILL.md` packages that Claude, Cursor, Codex, and other agents load. SkillPicker groups them by the work people search for: a task, a role, a tool, an agent, or an output.

This repository is the skill those agents should load. The procedure is in [`skills/find-skills-for-the-job/SKILL.md`](skills/find-skills-for-the-job/SKILL.md). The 109 topics are in [`skills/find-skills-for-the-job/references/topics.md`](skills/find-skills-for-the-job/references/topics.md), so an agent can choose a topic before it opens the site.

## Install

```bash
npx skills add geekfoxcharlie/find-skills-for-the-job
```

Claude Code:

```text
/plugin marketplace add geekfoxcharlie/find-skills-for-the-job
```

## Find a skill on the site

Open [skillpicker.xyz](https://skillpicker.xyz) and search, or open a topic:

| Kind | What it covers | Example |
| --- | --- | --- |
| Tasks | The work itself | [/for/task/web-design/](https://skillpicker.xyz/for/task/web-design/) |
| Roles | Who does the work | [/for/role/developers/](https://skillpicker.xyz/for/role/developers/) |
| Tools | Software the skill drives | [/for/tool/excel/](https://skillpicker.xyz/for/tool/excel/) |
| Agents | Where the skill runs | [/for/agent/claude-code/](https://skillpicker.xyz/for/agent/claude-code/) |
| Outputs | The artifact | [/for/deliverable/resume/](https://skillpicker.xyz/for/deliverable/resume/) |
| Getting started | First steps | [/for/beginner/human-writing/](https://skillpicker.xyz/for/beginner/human-writing/) |

Chinese pages use the same path with a `/zh` prefix, for example [/zh/for/tool/excel/](https://skillpicker.xyz/zh/for/tool/excel/).

The first skills on a topic page are the ones to start with. Open a skill, then read its own `SKILL.md` on GitHub. A listing means the skill matched the job. It is not a security review. [How we pick skills](https://skillpicker.xyz/about/#for-agents).

When the page shows a registry command, it looks like this:

```bash
npx skills add owner/repo@skill-name
```

Agents should use the topic file in this repo, then open one topic page. The machine-readable fallback, when no topic fits, is:

- https://skillpicker.xyz/skill-index.en.json
- https://skillpicker.xyz/skill-index.zh.json

Each row has `name`, `path`, `topicPath`, `source`, and `description`.

## 怎么在网站上找 skill

打开 [skillpicker.xyz](https://skillpicker.xyz)，用首页搜索，或按工作打开主题页。中文主题在 `/zh/for/` 下面。页面前面的几条是先看的。点进某条之后，读它 GitHub 上的 `SKILL.md`，再决定要不要安装。收录表示它和这个工作对得上，不是安全审计。

安装命令是 `npx skills add owner/repo@skill-name`。想让自己的 agent 以后都按工作找 skill，安装本仓库里的 `find-skills-for-the-job`。

## License

MIT
