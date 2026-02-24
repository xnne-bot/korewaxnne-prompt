# korewaxnne-prompt

Korewaxnne 的常用 prompt 集合。主要用于指导 AI 编码助手（如 Codex）遵循项目的代码规范。

## 目录结构

```
prompts/
├── for-codex-lint.md       # Lint 检查 — pyright 类型检查 + ruff 代码规范
├── for-codex-docstring.md  # Docstring 规范 — Google style 中文文档说明
└── for-codex-fmt.md        # 代码格式化 — ruff import 排序 + format
```

## 用法

| 文件 | 场景 | 说明 |
|------|------|------|
| `for-codex-lint.md` | 提交前检查 | 确保代码通过 pyright 和 ruff check，不改 pyproject.toml 设定 |
| `for-codex-docstring.md` | 新增公共 API | 为函数/类/方法补充 Google style 中文 docstring |
| `for-codex-fmt.md` | 提交前格式化 | 运行 ruff 自动修复 import 排序并格式化代码 |

## 如何使用

将对应 prompt 文件的内容复制到 Codex 的指令中，或在 `AGENTS.md` / `codex.md` 中引用。
