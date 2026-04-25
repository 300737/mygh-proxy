# gh-proxy-go

一个用于代理 GitHub 原始资源（如 `raw.githubusercontent.com`、`github.com/blob/...` 等）的 Go 程序，支持配置黑白名单、大小限制，并内置静态页面。

## 特性

- 支持反代 GitHub Releases、raw、blob、gist、archive 等常见地址
- 支持配置 `config.json` 管理白名单/黑名单/大小限制
- 支持嵌入静态资源（如 `index.html`）
- 支持通过 GitHub Actions 自动构建 Docker 镜像
- 支持部署在任意 Linux 服务器，结合 NGINX 使用

---

## 快速开始

###  使用 Docker 本地构建并运行


```docker run -d --name mygh-proxy --restart=always -p 8080:8080 ghcr.io/300737/mygh-proxy-go:latest```

程序默认读取项目根目录的 config.json 配置文件。

## 🔑 LICENSE

MIT License
