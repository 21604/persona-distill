# Persona Distiller V1.2

> 将任何人的写作风格、说话方式、知识体系蒸馏成可安装的 Persona Skill。
> 开源免费，MIT License。

---

## 快速开始

**触发词**（说任何一个都会启动本技能）：

| 类型 | 触发词示例 |
|------|-----------|
| 中文日常 | "蒸馏一个人"、"做个Persona"、"帮我分析下这个人的风格"、"把这段话的风格打包成Skill" |
| 个人品牌 | "做个人品牌"、"AI分身"、"把我的说话风格做成工具" |
| 场景指定 | "做个公众号风格的"、"做个朋友圈风格的"、"做个工作邮件风格的" |
| 英文/缩写 | "distill a persona"、"create persona skill"、"style transfer" |

**调用方式**：直接在对话中说出你的需求，不需要任何特殊命令。

---

## 工作流程（4步）

```
Step 1：收集素材（文章/聊天/邮件/口述）
Step 2：风格分析（六维分析 + 量化节奏统计）
Step 3：冲突检测（检查是否已有同名Persona）
Step 4：生成 Skill 包（输出完整可安装文件）
```

---

## 输出文件

**文件夹格式：**
```
[人名]-persona-v[版本号]-[YYYYMMDD]
```

**示例：**
- `张伟-persona-v1.0-20260512`
- `李娜-persona-v1.2-20260601`

**文件清单：**
```
张伟-persona-v1.0-20260512/
├── SKILL.md         # 技能定义（核心文件）
├── SOUL.md          # 灵魂部分
├── README.md        # 安装说明
├── demo.txt         # 示例对话
├── CHANGELOG.md     # 版本记录
└── install.bat      # Windows一键安装脚本
```

---

## 安装方法

### 方法一：一键安装（Windows）
1. 把整个文件夹复制到任意位置
2. 双击 `install.bat`
3. 重启 QClaw

### 方法二：手动安装
1. 在 `~/.qclaw/skills/` 下新建文件夹，命名为 `[人名]-persona`
2. 把 `SKILL.md`（必需）和其他文件复制进去
3. 重启 QClaw

### 方法三：skillhub 命令
```bash
skillhub install /path/to/persona-folder
```

---

## 没有素材？用快问快答

7个问题拿到5个以上回答即可生成：

1. "你最常说的一句话是什么？"
2. "你说话喜欢短句还是长句？"
3. "你最讨厌别人怎么跟你说话？"
4. "给你三句话，你会怎么改写？"
5. "你在什么话题上最有底气？"
6. "你觉得自己最独特的表达习惯是什么？"
7. "如果有人模仿你说话，你觉得哪里最假？"

---

## 目录结构

```
~/.qclaw/skills/persona-distiller/          ← 本技能本体
├── SKILL.md                               ← 技能定义（AI读取）
├── README.md                              ← 本使用手册
└── references/
    ├── persona-template.md                 ← Persona输出模板
    ├── install.bat                         ← 安装脚本模板
    └── changelog-template.md               ← 更新记录模板

~/.qclaw/skills/[人名]-persona/            ← 蒸馏产出的 Persona
├── SKILL.md
├── SOUL.md
├── README.md
├── demo.txt
├── CHANGELOG.md
└── install.bat
```

---

## 开源协议

MIT License - 自由使用、修改、分发。

---

*Version 1.2 | 2026-05-14*
