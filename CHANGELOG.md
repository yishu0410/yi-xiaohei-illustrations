# Changelog

本文件记录相对上游 [helloianneo/ian-xiaohei-illustrations](https://github.com/helloianneo/ian-xiaohei-illustrations) 的修改。

## 2026-10-01 — 新增第二个 IP「易姐」，改为多 IP 可切换

**新增**

- `references/yijie-ip.md`：易姐角色卡。外形（黑色齐肩短发 + 白西装 + 粗黑轮廓 + 面部极简淡彩）、性格、12 个动作池（比心 / 递东西 / 敲白板 / 握手 / 指方向 等）、禁止事项、与小黑的分工对照表、同框规则。
- `assets/ip-reference/yijie-reference.jpg`：易姐形象基准图，生成时可读图校准。

**修改**

- `SKILL.md`
  - frontmatter 触发词新增「易姐」「多 IP」；明确未指定 IP 时默认小黑。
  - 顶层新增「支持多 IP 形象」小节，列出两个 IP 的定位与角色卡路径。
  - 「先读这些参考」加入 `yijie-ip.md`。
  - shot list 表格新增字段：用哪个 IP（小黑 / 易姐 / 两人同框）。
  - 生成提示词必含项由「小黑作为核心动作主体」改为「所选 IP 的外形描述（从角色卡复制）」。
- `references/prompt-template.md`
  - `Recurring IP character required` 段改为三选一变量：小黑 / 易姐 / 两人同框，含易姐的英文外形描述。
  - `Composition` 变量改为「所选 IP 角色」。
  - `Color use` 段补充：易姐的肤色 / 红唇 / 红心计入暖色配额，西装保持纯白黑轮廓。
  - 「增强怪诞感」编辑模板泛化为 IP 角色。
- `references/qa-checklist.md`
  - 必过项「有小黑」改为「有指定 IP 角色（小黑 / 易姐 / 两人同框）」。
  - 失败信号新增「易姐被画成写实插画、影楼风、电商风或换装」。
  - 迭代方法表述泛化为 IP 角色。
- `references/style-dna.md`
  - 颜色段落新增「角色专属色例外」条款：允许易姐的极少量淡彩，计入暖色配额，上色面积不超过画面 10%。
- `references/composition-patterns.md`
  - 原创隐喻第三步「让小黑承担动作」泛化为「让 IP 角色承担动作」，并注明两个 IP 的动作差异。
- `agents/openai.yaml`
  - `short_description` 更新为支持多 IP 形象。

**未改动**

- 小黑的全部设定（`references/xiaohei-ip.md` 一字未改）。
- 风格 DNA 主体条款、8 种构图、反复刻清单、14 张原作者案例图。

## 2026-10-01 — 目录结构扁平化

仓库最初把 skill 放在内层目录 `ian-xiaohei-illustrations/`，导致 GitHub zip 下载后解压，安装器在根目录找不到 `SKILL.md`。现改为仓库根目录即 skill 本体（README / CHANGELOG / NOTICE / LICENSE 与 `SKILL.md` 同级），zip 解压后可直接安装。
