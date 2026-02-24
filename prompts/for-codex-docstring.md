# Docstring 规范 (for Codex)

> 用于指导 Codex 为新添加的公共 API 补充文档说明。

## Prompt

新添加的函数/类/属性缺少的文档说明。根据自定义编码指南 3.4，所有公共模块、函数、类和方法都必须使用 Google Python 样式提供**中文**的文档说明。每个函数都应记录其目的、参数（使用 `Args:` 部分）和返回值（使用 `Returns:` 部分）。

### 约束

- `Returns: None` 在 Google style 的 docstring 中应该被**省略**。

### 示例

```python
def fetch_data(url: str, timeout: int = 30) -> dict:
    """从指定 URL 获取数据。

    Args:
        url: 目标请求地址。
        timeout: 请求超时时间（秒），默认 30。

    Returns:
        包含响应数据的字典。
    """
    ...
```
