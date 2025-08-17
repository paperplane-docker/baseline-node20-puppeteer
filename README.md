# PaperPlane Docker Baseline-Node20-Puppeteer [![Build Status](https://drone.paperplane.cc/api/badges/paperplane-docker/baseline-node20-puppeteer/status.svg)](https://drone.paperplane.cc/paperplane-docker/baseline-node20-puppeteer)

本镜像 [`paperplanecc/baseline-node20-puppeteer`](https://hub.docker.com/r/paperplanecc/baseline-node20-puppeteer) 为 Node.js 和前端开发者提供预装可开箱即用 Puppeteer 的开发镜像。点此访问 [源码](https://git.paperplane.cc/paperplane-docker/baseline-node20-puppeteer) 或 [GitHub 源码镜像](https://github.com/paperplane-docker/baseline-node20-puppeteer)。

镜像基于 `paperplanecc/baseline-node20`（也就是 `node:20-slim`），它已预装 `pnpm@^10`，已预装 `canvas` 的相关依赖并开箱即用，预装 Chromium，并为 Puppeteer 配置了免下载和执行路径的环境变量。

使用须知：

- 在容器中启动 Puppeteer 需要配置 `--no-sandbox` 启动参数，或者启动 Docker 镜像时添加 `--cap-add=SYS_ADMIN` 参数；
- 预装 Chromium 而不是 Chrome，是因为 Chrome 官方不提供 ARM 平台的版本（唯一只给 macOS 提供 ARM 桌面版）；
- 如果用到 `pnpm`，请留意自己项目中 `package.json` 的 `packageManager` 字段，如果此版本号不符合，可能报错。

> 将 `paperplanecc` 替换为 `docker.p01.cc` 即可使用私有库版本。点此访问 [私有库镜像](https://docker.p01.cc/#!/taglist/baseline-node20-puppeteer)。
>
> 私有版本和公开版本目前没有区别。
