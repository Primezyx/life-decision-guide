# life-decision-guide（离线版）

> 回答人生选择、风险、维权、医疗、理财、职场、婚姻、取舍类问题时使用。
> 先从《高性价比人生指南》正文里把相关条目查出来，照书里的算账方式排序，再回答，每条注明出自第几节第几条。
> **书里没有的内容，如实说没写，不编数字。**

---

## 出处与致谢

**本技能的正身内容全部来自以下开源项目，本仓库只是它的离线打包版。**

| 项目 | 地址 |
| --- | --- |
| 仓库 | https://github.com/eternity4719/HowToLiveBetter |
| 书名 | 《高性价比人生指南》 |
| 作者 | eternity4719 |
| 原书README | [`references/README.md`](references/README.md) |
| 原作者写的 skill 文件 | [`references/ORIGINAL-SKILL.md`](references/ORIGINAL-SKILL.md) |

原作者本人就写了配套技能（仓库内 `skills/life-decision-guide/`），本仓库的问答纪律、条目格式、排序算法**全部沿用**。

### 许可

原作者的许可协议原文随包保留在 [`references/LICENSE`](references/LICENSE)：正文内容为 **CC BY 4.0（署名 4.0 国际）**，允许商业使用与改编，只需署名。

代码部分另有 [`references/LICENSE-CODE`](references/LICENSE-CODE)（MIT License），一并保留。

本仓库作为二次打包，遵守原许可：署名 eternity4719、指向原仓库。

如需二次分发，请一并保留：
- 原作者署名 eternity4719
- 原许可协议与指向原仓库的链接

正文内容归原作者所有。本仓库不修改正文判断规则、不改动任何结论与数字。

### 与原版的唯一差别

原版 skill 的第1 步是「本地没有就去GitHub 现取正文」（`git clone` 或 `curl` raw 文件）。

本离线版把 34 篇正文、README、配套长文、官方来源核实记录**全部预打包进 `references/`**，安装后不联网、不克隆、不下载即可检索。原版规则原文存于 `references/ORIGINAL-SKILL.md`，可随时对照。

其余问答纪律一字未改。

---

## 打包了什么

| 内容 | 数量 | 位置 |
| --- | --- | --- |
| 正文 | 34 篇 / **677 条** | `references/book/` |
| 配套长文 | 10 篇 | `references/docs/` |
| 官方来源核实记录 | 144 篇 | `references/docs/核实记录/` |
| 章节索引速查表 | 1 | `references/INDEX.md` |
| 档位算法来源 | 1 | `references/index.html` |
| 原作者 skill 原件 | 1 | `references/ORIGINAL-SKILL.md` |

条目证据等级分布：A 441 条 / B 189 条 / C 47 条。

正文与原仓库逐字节一致，可用 `diff -r` 自行核对。

---

## 安装

**安装不需要 GitHub 账号，不需要登录，克隆公开仓库也不用认证。** 只有往仓库里推送才需要凭据。

本技能是完整离线包 —— 正文已经打包在里面，装完不联网、不克隆、不下载即可检索。

### 方式一：直接下载拷贝（推荐，零依赖）

在 https://github.com/Primezyx/life-decision-guide 点 **Code → Download ZIP**，解压后把 `life-decision-guide` 整个文件夹拷进你的 skill 目录：

| 客户端 | skill 目录 |
| --- | --- |
| Claude Code | `~/.claude/skills/life-decision-guide/` |
| Codex | `~/.agents/skills/life-decision-guide/` |
| WorkBuddy | `~/.workbuddy/skills/life-decision-guide/` |

### 方式二：克隆本仓库

```bash
git clone https://github.com/Primezyx/life-decision-guide.git ~/.workbuddy/skills/life-decision-guide
```

Windows PowerShell：

```powershell
git clone https://github.com/Primezyx/life-decision-guide.git "$env:USERPROFILE\.workbuddy\skills\life-decision-guide"
```

### 装完验证

skill 目录里应该有 34 篇正文、677 个条目：

```bash
ls ~/.workbuddy/skills/life-decision-guide/references/book/*.md | wc -l   # 应为 34
grep -rh '^### ' ~/.workbuddy/skills/life-decision-guide/references/book | wc -l   # 应为 677
```

装完直接问「每天通勤两小时值不值」「朋友让我替他担保，签不签」就会触发；也可以显式说「用 life-decision-guide 回答」。

> 想更新到最新版，重下 ZIP 覆盖，或 `git pull`。

---

## 用起来是什么样

回答固定五段：

1. **一句话结论** —— 划不划算、该不该做、第一步是什么
2. **先做这几条**（3–7 条，按性价比和证据等级排序）
3. **别做 / 不用做的**
4. **书里没写的**
5. 复查点 —— 什么时候回头再看

每条出处写成「第 8 节第 17 条（借条和担保）」这种格式，方便自己翻原文。

### 排序规则（原作者定的，别凭感觉改）

- 成本分 = 钱 + 时间 + 毅力三项加权相加，权重见 `references/index.html` 第 995 行 `COST_W`
- 收益量级配成本分落档，见第 577 行 `e.ratio`
- 先按性价比，同档再按**证据等级 A > B > C**，再按贴合度
- **不同口径之间不排序** —— 换钱的和换寿命的分开列，各排各的
- 「一般」不等于不该做，只是那笔花销得你自己掂量

### 硬纪律

- **没查到就别答**。每个数字、每条法条、每个结论都要能指回某一条正文
- **四样分开算，不互相折算** —— 寿命、时间与精力、金钱、人身自由，不在一把尺子上
- **急症优先**：倒地没呼吸、大出血、火灾、溺水、触电、中毒、卒中或心梗症状，先说打 120 / 119 和现场第一个动作，别先讲性价比
- **心理援助**：提到自杀念头、活不下去，先给全国心理援助热线 12356
- **法律程序进行中**（已被传唤、拘留、起诉），先指第 8 节，并说明书只给通用口径，个案要找律师
- **数字照抄条目**，一个不改。HR、RR、OR 旁边就地翻成「低约 28%」，原值不删
- **不引二手转述**，只给条目「来源」栏里已有的链接
- 标了「争议」的条目，反方证据也要说一句；标了「TODO 待核实」的，别当结论用

### 边界

这本书给的是通用口径，**不替代医生、律师、会计**。涉及具体病情、具体案件、具体税务的，按条目给方向和该找谁，别替专业人士下判断。不给个性化投资建议。

政策类金额和时限集中在第 7、19、21、24、31、32 节，正文写了截至日期。引用时带上日期，并提醒使用者自查官方渠道 —— 这些数字会变。

---

## 目录结构

```
life-decision-guide/
├── SKILL.md                          # 技能定义（frontmatter name: life-decision-guide）
└── references/
    ├── INDEX.md                      # 章节索引速查表：问题 → 节号 → 文件 → 条目数
    ├── book/                         # 34 篇正文，677 条
    │   ├── 01-不要早死.md
    │   ├── 02-不要慢慢死.md
    │   ├── ...（全书 34 篇）
    │   └── 34-家里的常备药别吃出事.md
    ├── docs/                         # 10 篇配套长文
    │   ├── 结婚划不划算.md
    │   ├── 家庭应急装备清单.md
    │   ├── 被裁了之后先做什么.md
    │   ├── 遇到陌生人出事该不该停.md
    │   └── ...
    │   └── 核实记录/                 # 144 篇官方来源核实记录
    ├── README.md                     # 原书 README
    ├── index.html                    # 档位算法权威来源
    ├── ORIGINAL-SKILL.md             # 原作者 skill 原件
    ├── CLAUDE.md                     # 原书完整创作说明
    ├── LICENSE                       # 原许可协议
    └── LICENSE-CODE
```

---

## 检索怎么走

节文件最大的有 110 KB，**别整篇读**，按关键词捞：

```bash
# 先看有哪些条目标题
grep -rn '^### ' references/book/ | grep -E '彩礼|担保'

# 正文里搜，带上下文
grep -rn -B2 -A8 '关键词' references/book/08-别把自己搭进去.md

# 按条号抽一整条（务必读完「备注」栏，适用人群和例外都在那里）
sed -n '/^### 17\. /,/^### 18\. /p' references/book/08-别把自己搭进去.md
```

一条长这样：

```markdown
### 5. 把家里的食盐换成低钠盐（钾盐）
<!-- 成本标签: 钱=少 时间=少 毅力=否 收益=中 口径=死亡率 -->
- 成本：每袋贵几元
- 说人话：……死亡的概率低约 12%……
- 收益：脑卒中降 14%，心血管事件降 13%，总死亡率降 12%
- 证据等级：A
- 来源：Neal B, et al. (2021). NEJM. https://doi.org/10.1056/NEJMoa2105675
- 备注：争议。肾功能不全、正在吃保钾利尿剂的人不要用。……
```

那行 HTML 注释是给机器读的成本标签：钱 0/少/多、时间 少/中/多、毅力 否/些/是、收益 大/中/小、口径 死亡率/金钱/时间/自由。

---

## 维护

章节若有增删，重跑 `references/INDEX.md` 里的统计，别手改条目数。

原书在线版：https://eternity4719.github.io/HowToLiveBetter/
原书离线单文件 HTML / PDF / EPUB / Anki 牌组：见原书 README。