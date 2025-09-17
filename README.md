# 此仓库已废弃

现在 Node.js 的 Baseline 系列镜像已转移至 [paperplane-docker/baseline-node](https://github.com/paperplane-docker/baseline-node) 仓库。

# PaperPlane Docker Baseline-Node20-Puppeteer

本镜像 [`paperplanecc/baseline-node20-puppeteer`](https://hub.docker.com/r/paperplanecc/baseline-node20-puppeteer) 为 Node.js 和前端开发者提供预装可开箱即用 Puppeteer 的开发镜像。

- 基于 `paperplanecc/baseline-node20`，预装 Chromium，并为 Puppeteer 配置了免下载和执行路径的环境变量；
- 在容器中启动 Puppeteer 需要配置 `--no-sandbox` 启动参数，或者启动 Docker 镜像时添加 `--cap-add=SYS_ADMIN` 参数；
- 预装 Chromium 而不是 Chrome，是因为 Chrome 官方不提供 ARM 平台的版本（唯一只给 macOS 提供 ARM 桌面版）；
- 如果用到 `pnpm`，请留意自己项目中 `package.json` 的 `packageManager` 字段，如果此版本号不符合，可能报错。
