# 更新日志

## 1.0.1 (2026-11-13)

兼容性修复版本，无接口行为变更，升级无需改动调用方代码。

### 全量扫描结果（PHP 8.4 / 8.5）

- 隐式可空参数：0 处（`?VisibilityConverter`、`?string` 等均为显式可空）。
- 其它 8.2–8.5 弃用写法：`${}` 插值、`utf8_encode`/`strftime`/`each`/`create_function`、`E_STRICT`、非规范类型强转、`Reflection*::setAccessible`、`trigger_error(E_USER_ERROR)` 等均为 0 命中。
- 动态属性：类属性均已声明，无 8.2 动态属性弃用风险。
- 本包源码无需改动（`php -l` 与严格 `E_ALL` 加载均已通过）。

### 元数据

- `require.php` 维持 `^7.2|^8.0`：源码仍兼容 PHP 7.2，PHP 8.0–8.5 已实测可正常加载，不收紧约束以免影响既有用户。
- 补充 `keywords`、`description`、`support`。
- 版本由 Git 标签 `v1.0.1` 决定。
- 新增 `topthink/framework: ^6.1 || ^8.0` 依赖声明；补充 `LICENSE`（MIT 全文，与 `license` 字段一致）。
