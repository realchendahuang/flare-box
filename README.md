# 火花魔盒 · Flare Box (`flare-box`)

> Cloudflare 免费全家桶开箱即用实战模板集  
> Ready-to-deploy minimalist microservices & templates on Cloudflare Workers, D1, R2 & Pages.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![GitHub stars](https://img.shields.io/github/stars/realchendahuang/flare-box?style=social)](https://github.com/realchendahuang/flare-box)
[![GitHub forks](https://img.shields.io/github/forks/realchendahuang/flare-box?style=social)](https://github.com/realchendahuang/flare-box/network/members)
[![GitHub issues](https://img.shields.io/github/issues/realchendahuang/flare-box)](https://github.com/realchendahuang/flare-box/issues)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/realchendahuang/flare-box/pulls)
[![Follow @realchendahuang](https://img.shields.io/badge/Follow-%40realchendahuang-1DA1F2?logo=x&logoColor=white)](https://x.com/realchendahuang)

---

## 设立宗旨

Cloudflare 的边缘计算生态是独立开发者与一人公司最强大的免费基础设施：
- Workers 每天 10 万次免费调用；
- D1 边缘 SQLite 免费 5GB 存储；
- R2 对象存储每月 10GB 免费且免流出带宽费；
- Pages 无限静态托管与免费自定义域名 SSL。

火花魔盒（Flare Box）为开发者提供一组即拷即用、10 秒部署上线的微服务代码模版。

---

## 核心开箱模板目录

### 1. `templates/url-shortener`
- **架构**：Workers + KV
- **功能**：毫秒级重定向短链服务，带自定义后缀与简单访问计数。

### 2. `templates/image-bed`
- **架构**：Workers + R2 + Pages
- **功能**：极简个人图床，支持直接粘贴剪贴板上传、防盗链与公共 CDN 缓存。

### 3. `templates/minimal-api`
- **架构**：Hono.js + D1 + Drizzle ORM
- **功能**：轻量 RESTful API 骨架，带 JWT 认证与增删改查标准流。

### 4. `templates/cron-monitor`
- **架构**：Workers Scheduled Triggers + Webhook
- **功能**：定时网站心跳巡检，出现异常即时推送 Telegram 或飞书通知。

### 5. `templates/cors-proxy`
- **架构**：Pure Worker
- **功能**：为前端临时调试提供干净轻量的 CORS 代理转发。

---

## 部署说明

每个模板均包含独立的 `wrangler.jsonc` 配置文件。

进入对应目录执行：
```bash
pnpm install
pnpm exec wrangler deploy
```

---

## License

MIT License. Copyright (c) 2026 realchendahuang.
