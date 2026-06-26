# Transcript Cleaner — 术语字典

> 此文件为 transcript-cleaner 的外部词库。修改此文件即可更新清洗规则，无需修改 Skill 本体。

## 🔒 一级字典（高置信度 — 无条件替换）

空格分隔字母序列，不可能出现在正常英文中：

| ASR 错误 | 正确形式 |
|----------|----------|
| `l l m` | LLM |
| `r a g` | RAG |
| `p d f` | PDF |
| `g p t` | GPT |
| `m c p` | MCP |
| `c l i` | CLI |
| `s d k` | SDK |
| `a p i` | API |
| `i d e` | IDE |
| `j s o n` | JSON |
| `h t m l` | HTML |
| `c s s` | CSS |
| `s q l` | SQL |
| `mark down` | Markdown |
| `y o l o` | YOLO |
| `b n` | BN |
| `c n n` | CNN |

## 🟡 二级字典（中等置信度 — 需上下文验证）

| ASR 错误 | 正确形式 | 上下文验证条件 |
|----------|----------|---------------|
| `obid` | Obsidian | 周围出现: 笔记/知识库/插件/链接/库/图谱 |
| `obidian` | Obsidian | 同上 |
| `car` | Karpathy | 周围出现: OpenAI/AI/知识库/LLM/科学家。如果出现: 开车/汽车/轮胎 — 保留原文 |
| `carpath` | Karpathy | 周围出现: OpenAI/AI/知识库 |
| `androidac` | Karpathy | 周围出现: OpenAI/科学家/前 |
| `anji` | Agent（待确认） | 周围出现: 技术/AI/代码 |
| `cloud op` / `cloudap` | Claude Opus | 周围出现: 大模型/上下文/AI/LLM |
| `over` | Obsidian | **必须**同时出现: wiki/笔记/知识库/obid |
| `get` | Git | **仅当**周围出现: 版本管理/提交/代码/仓库 |
| `relu` | ReLU | 周围出现: 激活函数/神经网络/深度学习/折线 |
| `drop out` | Dropout | 周围出现: 随机关灯/训练/正则化 |
| `何凯明` | 何恺明 | 周围出现: 微软/ResNet/残差网络/深度学习 |
| `汪涛` | 汪滔 | 周围出现: 大疆/DJI/无人机/创始人/港科大 |
| `com m` | 悟空-M (WooKong-M) | 周围出现: 大疆/飞控/无人机/航模 |
| `romo` | Romo | 周围出现: 大疆/扫地机器人/避障 |
| `schedule` | Skydio | 周围出现: 无人机/美国/竞争对手 |
| `pirot` | Parrot | 周围出现: 无人机/法国/竞争对手 |
| `影食` | 影石/Insta360 | 周围出现: 全景相机/Insta360/竞争对手 |
| `卓誉科技` | 卓驭科技 | 周围出现: 智能驾驶/自动驾驶/定点合作 |
| `即飞科技` | 极飞科技 (XAG) | 周围出现: 农业植保/无人机/前大疆 |
| `抛三` | Pocket 3 | 周围出现: DJI/运动相机/Action/Pocket |
| `精灵` | Phantom | 周围出现: DJI/无人机/航拍 |
| `江维大机` | 降维打击 | 周围出现: 竞争/超越/领先/对手 |

## ⚠️ 三级字典（低置信度 — 仅存疑标记，不自动修正）

| ASR 错误 | 可能的正确形式 | 说明 |
|----------|--------------|------|
| `序员` | 程序员 | 中文同音词 |
| `胡哨` | 花哨 | 可能真是"胡哨" |
| `极稿` | 极高 | 也可能是稿件 |
| `部 mark` | Markdown | 发音模糊 |
| `个人为基` | 个人Wiki/个人知识库 | 语义模糊 |
| `ne瓶井块` | Bottleneck 块 | ASR 音变严重 |
| `装点` | 节点 | Obsidian 语境下可能是"节点编辑" |
| `roma 二` | Romo 2 | 发音模糊 |

---

> **维护记录**:
> - 2026-06-26: 初始创建
