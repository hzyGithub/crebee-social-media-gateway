# CreBee 社交媒体网关 (Skill)-支持18+主流社媒平台

[CreBee](https://www.crebee.cn) 社交媒体网关 Skill —— 统一 HTTP API 网关，让 AI Agent 自动化管理中国主流社交媒体平台。

本仓库为 Codex / Agent Skill 形态，核心由 `SKILL.md` 与 `references/` 组成。Agent 加载本 Skill 后即可通过本地 CreBee 桌面客户端提供的 API 操作各平台账号。

## 能力概览

- 多平台账号管理
- 内容发布（视频 / 图文 / 文章，支持批量多平台分发）
- 数据分析与表现指标
- 粉丝 / 观众画像
- 话题、标签、音乐、活动搜索

## 支持的平台

| 平台 | appAlias |
| --- | --- |
| 抖音 | `douyin` |
| B站 | `bilibili` |
| 小红书 | `xiaohongshu` |
| 快手 | `kuaishou` |
| 微博 | `weibo` |
| 公众号 | `gongzhonghao` / `gongzhonghao_official` |
| 百家号 | `baijiahao` |
| 头条号 | `toutiaohao` |
| 企鹅号 | `qiehao` |
| 网易号 | `wangyihao` |
| 视频号 | `shipinhao` |
| 知乎 | `zhihu` |
| 大鱼号 | `dayuhao` |
| 搜狐号 | `souhuhao` |
| 简书 | `jianshu` |
| CSDN | `csdn` |

## 使用前提

本 Skill 通过用户电脑上的 CreBee 桌面客户端提供能力，不包含独立云端服务。使用前必须：

1. 访问 [CreBee 下载页](https://www.crebee.cn/#/download) 下载最新版桌面客户端。
2. 安装并启动 CreBee，注册或登录账号。
3. 在客户端内登录需要操作的平台账号。
4. 确认本地 API `http://127.0.0.1:3456` 可连通后再调用接口。

## 快速参考

| 属性 | 值 |
| --- | --- |
| Base URL | `http://127.0.0.1:3456` |
| API 前缀 | `/galic/v1` |
| 认证方式 | Bearer Token (JWT) |
| 请求方法 | 所有 API 使用 `POST` |
| Content-Type | `application/json` |

## 仓库结构

```
.
├── SKILL.md            # Skill 主文档（Agent 读取）
└── references/
    ├── publishing.md   # 发布流程详细说明
    └── platforms/      # 各平台 API 详细文档
```

## 安装为 Codex Skill

将本仓库（或 `SKILL.md` 所在目录）放入 `$CODEX_HOME/skills/` 即可被 Codex 识别为 Skill：

```bash
cp -r crebee-social-media-gateway ~/.codex/skills/
```

更多详见 [SKILL.md](SKILL.md)。

## 相关链接

- 官网：<https://www.crebee.cn>
- 下载页：<https://www.crebee.cn/#/download>
