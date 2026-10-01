# Ian 小黑配图 Skill（多 IP 增修版）

基于 [helloianneo/ian-xiaohei-illustrations](https://github.com/helloianneo/ian-xiaohei-illustrations) 修改，原作者 Ian（MIT 协议，署名保留）。

在保留原有「小黑」IP 与全部风格体系不变的前提下，新增第二个视觉 IP「**易姐**」，并把 skill 改造成**多 IP 可切换**的形态。

## 这个 skill 做什么

为中文文章（公众号帖子 / 博客 / Notion / 工作流文档 / 方法论）生成 **16:9 横版正文配图**：纯白背景、黑色手绘线稿、少量红橙蓝手写批注、大量留白、怪诞但不说明书。

## 两个 IP，怎么选

| IP | 形象 | 气质 | 适合的文章 |
|---|---|---|---|
| **小黑**（默认） | 黑色实心小怪物，白点眼、细腿、空表情 | 荒诞、呆、冷幽默 | AI 工作流、系统结构、方法论、抽象隐喻 |
| **易姐**（新增） | 白西装短发职业女性，极简淡彩、粗黑轮廓 | 专业、温和、有温度 | 个人品牌、职场成长、培训招生、客户沟通、增长方法 |

- 指定用哪个就用哪个；未指定时默认小黑，个人品牌 / 职场 / 讲解类内容可建议切易姐。
- 支持两人同框：易姐主讲示范，小黑做荒诞辅助，一张图仍只讲一个核心结构。

## 目录结构

仓库根目录即 skill 本体，下载 zip 解压后可直接安装（不要再往里找一层）：

```
.
├── SKILL.md                    调度层：触发词 + 5 步工作流 + 判断规则
├── references/
│   ├── style-dna.md            风格宪法：白底 / 黑线稿 / 留白 35% / 三色克制
│   ├── xiaohei-ip.md           小黑角色卡（未改动）
│   ├── yijie-ip.md             易姐角色卡（本版新增）
│   ├── composition-patterns.md 8 种构图 + 原创隐喻三步法 + 反复刻清单
│   ├── prompt-template.md      生图提示词模板（IP 段改为三选一变量）
│   └── qa-checklist.md         质检闭环：必过项 / 失败信号 / 迭代方法
├── assets/
│   ├── examples/               14 张风格校准案例（原作者素材，禁止复刻构图）
│   └── ip-reference/           易姐形象基准图（本版新增）
└── agents/openai.yaml          OpenAI Agents 接口声明
```

## 安装

方式一（推荐，适合 zip 用户）：下载仓库 zip → 解压 → 把解压出来的整个文件夹（名字随意，建议 `ian-xiaohei-illustrations`）放进 skills 目录即可，里面第一层就应该有 `SKILL.md`。

```bash
# WorkBuddy
cp -R ~/Downloads/yi-xiaohei-illustrations-main ~/.workbuddy/skills/ian-xiaohei-illustrations

# Claude Code
cp -R ~/Downloads/yi-xiaohei-illustrations-main ~/.claude/skills/ian-xiaohei-illustrations
```

方式二（git）：

```bash
git clone https://github.com/yishu0410/yi-xiaohei-illustrations.git ~/.workbuddy/skills/ian-xiaohei-illustrations
```

装完确认：`~/.workbuddy/skills/ian-xiaohei-illustrations/SKILL.md` 存在即生效，无需重启。

## 用法

- 「给这篇文章配几张图」→ 先出 shot list，再逐张生成
- 「用易姐配图」/「小黑和易姐同框」→ 指定 IP
- 「分析这篇怎么配图」→ 只出 shot list，不生图

## 本版改动

见 [CHANGELOG.md](CHANGELOG.md)。原始项目的条款与署名见 [NOTICE.md](NOTICE.md)。
