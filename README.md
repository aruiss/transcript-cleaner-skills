# ASR Transcript Cleaner Skills

视频 ASR（自动语音识别）转录文本清洗工具集。

## 文件结构

```
skills/
├── transcript-cleaner/
│   └── SKILL.md          # 核心清洗 Skill（subagent）
├── batch-clean/
│   └── SKILL.md          # 批量清洗编排器（inline）
└── DICTIONARY.md         # 独立术语词库
```

## 使用方法

### 单文件清洗
```
/transcript-cleaner path=转录文件路径.txt
```

### 批量去重清洗
```
/batch-clean
```
自动比对输出目录，只清洗未处理的新文件。

## 三级字典体系

| 等级 | 替换策略 | 示例 |
|:----|:---------|:-----|
| 🔒 一级 | 无条件替换（空格分隔字母） | `l l m` → LLM |
| 🟡 二级 | 上下文验证通过才替换 | `car` → Karpathy（仅当周围有 AI/OpenAI） |
| ⚠️ 三级 | 永不自动修正，仅存疑展示 | `序员` → 可能为"程序员" |

词库独立维护在 `DICTIONARY.md`，修改即可更新规则，无需改动 Skill。
