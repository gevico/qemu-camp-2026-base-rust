# QEMU 训练营基础阶段 Rust

这个仓库现在是完整的 Rustlings 题库版本，作为 QEMU 训练营基础阶段的 Rust 语言练习。

## 目录说明

### `exercises`

保留完整 Rustlings 练习题和章节说明，继续作为基础阶段 Rust 语言练习使用。

### `src`

Rustlings 命令行工具本体，用来执行 `watch`、`run`、`hint`、`verify` 等练习流程。

### `tests`

Rustlings 的集成测试与评测 fixture，用来验证题库、命令行为和评分流程。

## 自动评测

当前 GitHub Actions 默认会：

1. 编译并运行 Rustlings 评测
2. 汇总题目完成情况
3. 在 `push main/master` 时把成绩回传到 OpenCamp
4. 在 `pull_request` 场景下只做评测，不回传 OpenCamp

工作流文件在 `.github/workflows/rust.yml`。

## 常用命令

```bash
cargo install --force --path .
rustlings watch
rustlings run next
rustlings hint next
rustlings list
cargo test --test cicv --verbose
```

## 说明

- 本仓库基于 rustlings 5.5.1 的完整题库整理而成。
- 评分以 GitHub Actions 结果为准。
- OpenCamp 回传用户名使用触发 workflow 的 GitHub 用户名。
