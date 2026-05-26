# Biome 使用说明（代码风格和自动修复）

本仓库使用 Biome 作为 lint/format 工具，并在 CI 中运行 Biome 检查。

本地命令：

- 检查（不修改）：

```
pnpm run biome:check
```

- 自动修复（应用安全修复）：

```
pnpm run biome:fix
```

- CI 专用（只读，建议在 CI 中使用）：

```
pnpm run biome:ci
```

在本地启用并安装 Biome：

```
corepack enable
corepack prepare pnpm@11 --activate
pnpm add -D -E @biomejs/biome
pnpm exec biome init
```

CI 中已配置在 .github/workflows/ci-pnpm.yml，使用 `pnpm run biome:ci` 来执行 Biome 检查并在 PR 页面显示注释。
