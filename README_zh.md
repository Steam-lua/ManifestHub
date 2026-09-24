<div align="center">

![ManifestHub3 — steamtools.games 底层数据中枢](og-home.png)

# ⚡ ManifestHub3 (中文版)

**为 [steamtools.games](https://steamtools.games/) 提供底层支持的社区维护 Steam 清单与 Lua 蓝图数据中心。**

🌐 **[访问 steamtools.games 官方网站 →](https://steamtools.games/)**
· 📖 [开放 API 文档](https://steamtools.games/developers)
· 💬 [Discord 社区](https://discord.com/invite/FDKpJu5zgT)
· 📝 [官方博客](https://steamtools.games/blog)
· 🌍 支持 7 种语言

[![官方网站](https://img.shields.io/badge/官方网站-steamtools.games-0b1220?style=for-the-badge)](https://steamtools.games/) [![API](https://img.shields.io/badge/API-Public%20%26%20Free-22c55e?style=for-the-badge)](https://steamtools.games/developers) [![网络加速福利](https://img.shields.io/badge/雷神加速器-免费50小时口令%EF%BC%9ASTEAMTOOLS-ff5900?style=for-the-badge&logo=speedtest&logoColor=white)](https://www.leigod.com) [![Discord](https://img.shields.io/badge/Discord-加入社区-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.com/invite/FDKpJu5zgT) [![开源协议](https://img.shields.io/badge/协议-MIT-3b82f6?style=for-the-badge)](LICENSE)

<p align="center">
  <a href="README.md">English</a> • <b>简体中文</b>
</p>

</div>

---

> [!IMPORTANT]
> **您几乎完全不需要克隆这个体积庞大的 Git 仓库！**
> [**steamtools.games**](https://steamtools.games/) 提供了免费免登录、零配置的网页端清单生成引擎，输入任意 Steam 游戏名称或 App ID，一秒内即可返回已验证的 `.lua` 蓝图与 `key.vdf` 解密密钥包。
>
> 👉 **[立即前往 steamtools.games 使用网页版](https://steamtools.games/)** — 输入游戏名或粘贴 App ID，按 <kbd>Ctrl</kbd>+<kbd>Enter</kbd> 即可生成！

---

## 🎁 玩家联机与网络加速专享福利（雷神加速器）

针对 Steam 商店访问卡顿、CDN 下载慢及多人联机掉线问题，推荐使用**雷神加速器**：

- 🎁 **专属兑换码**：**`STEAMTOOLS`**
- ⚡ **专属福利**：免费领取 **50 小时超长体验时长**
- ⏱️ **时长随时可暂停**：不玩不扣时，一次领取长久可用，适合各类联机与单机玩家
- 🚀 **专线极速直连**：自研金融级专线，畅快加速 Steam、Apex、黑神话、绝地求生等全平台热门大作
- 👉 **兑换方式**：下载登录[雷神加速器客户端](https://www.leigod.com)，点击顶部「充值中心」/「口令兑换」，输入 **`STEAMTOOLS`** 即可秒到账！

---

## 📖 什么是 ManifestHub3？

ManifestHub3 是社区维护的 Steam 清单文件（Lua 脚本 + Key 密钥）缓存库，专为 **SteamTools** (Watt Toolkit / 原 Steam++) 规范量身定制。它是原 ManifestHub 仓库在 GitHub 归档下架后的长期维护重构版。

- **本 GitHub 仓库**：为每个 Steam App ID 维护独立的 Git 分支，存储 `<AppID>.lua` 和 `key.vdf`。
- **[steamtools.games](https://steamtools.games/)**：高性能面向用户的 Web 前端，通过 Cloudflare Workers 全球边缘计算毫秒级索引并打包供玩家下载。

---

## 🚀 三步极速入库与安装（30 秒完成）

1. 打开 **[steamtools.games](https://steamtools.games/)**。
2. 搜索游戏名称（如《Portal》）或粘贴 App ID（如 `400`）。
3. 按下 <kbd>Ctrl</kbd>+<kbd>Enter</kbd> 或点击下载，获取包含 `.lua` 和 `key.vdf` 的专属 ZIP 压缩包。
4. 将解压出来的文件放入 SteamTools 客户端安装根目录对应路径（或相应插件目录），重启 SteamTools 及 Steam 官方客户端即可开始极速下载畅玩！

---

## 🔌 开放 RESTful API 接口

提供免认证、高可用的纯 HTTP 数据接口：

### 1. 搜索 Steam 游戏目录
```bash
curl -s "https://steamtools.games/api/search?query=portal" | jq
```

### 2. 生成清单及 Lua 脚本文件下载链接
```bash
curl -s -X POST "https://steamtools.games/api/generate" \
  -H "Content-Type: application/json" \
  -d '{"appId": "400", "branch": "public"}' | jq
```

更多接口详情与 OpenAPI 规范，请参阅：[steamtools.games/developers](https://steamtools.games/developers)。

---

## 📄 参与贡献与鸣谢

欢迎提交贡献！详见 [CONTRIBUTING.md](CONTRIBUTING.md)。

- **原始项目**：最初的 ManifestHub 清单数据库维护者们。
- **前端与 API**：[steamtools.games](https://steamtools.games/) 团队。
- **桌面端生态**：SteamTools 开源项目社区。

---

<div align="center">

🌐 **[steamtools.games](https://steamtools.games/)** — 快捷可靠的 SteamTools 清单生成与分发枢纽。

</div>
