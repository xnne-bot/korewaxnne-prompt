# Lint 检查 (for Codex)

> 用于指导 Codex 在提交代码前通过静态检查。

## Prompt

让代码能通过这两项测试：

```bash
# 类型检查
uv run pyright src/lab tests

# 代码规范检查
uv run ruff check . --exclude packages
```

### 约束

- **不能改动** `pyproject.toml` 的 pyright 设定。
- 实在过不了的可以加 `# type: ignore`。
- 最终的修改应该**仅仅涵盖你本次修改的内容**，不应该超出本次修改内容的范围。
