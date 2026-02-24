# 代码格式化 (for Codex)

> 用于指导 Codex 在提交前对仓库进行格式化。

## Prompt

提交前应该运行以下命令对仓库进行一次 format：

```bash
# 自动修复 import 排序
uv run ruff check --fix --select I . --exclude packages

# 代码格式化
uv run ruff format . --exclude packages
```

### 说明

- 这两条命令应在 `git commit` 之前执行。
- `--exclude packages` 排除第三方/vendored 代码。
- 先 `--fix --select I`（import 排序），再 `format`（整体格式化）。
