# voxpen-legal · ⚠️ 已废弃 / DEPRECATED

> **此仓库已于 2026-05-23 废弃。** voxpen 主页 + 隐私政策 + 服务条款 + 营销素材全部迁移到 [voxpen-web](https://github.com/a2fapower/voxpen-web),并按当前生产现状重写。本仓现在仅作历史归档 + 存放 App Store 提审专用文档。

---

## 为什么废弃

voxpen-legal 原本承担太多职责:
- 公开主页(index.html)
- 法务文档(privacy / terms)
- 营销素材(marketing/)
- App Store 提审专用问卷(asc-privacy-questionnaire.md)
- Magic link 登录中间页(login.html)
- 各种调研截图(_test_typeless/)

混在一起越来越难管理。2026-05-23 分仓:

| 新仓库 | 职责 |
|---|---|
| **[voxpen-web](https://github.com/a2fapower/voxpen-web)** | 公开主页 + 法务 + 营销(部署在 voxpen.cn) |
| voxpen-legal(本仓,归档) | App Store 提审材料 + 历史归档 |

## 当前仓库内容(不再更新)

| 文件 | 是否还有意义 | 现状 |
|---|---|---|
| `asc-privacy-questionnaire.md` | ✅ App Store 提审专用 | 保留,下次提审前更新对齐生产 |
| `privacy.md` | ⚠️ 已过时 | **不要看本仓的版本**,看 [voxpen-web/privacy.html](https://github.com/a2fapower/voxpen-web/blob/main/privacy.html) |
| `terms.md` | ⚠️ 已过时 | 同上,看 [voxpen-web/terms.html](https://github.com/a2fapower/voxpen-web/blob/main/terms.html) |
| `index.html` | ⚠️ 已过时 | 看 [voxpen-web/index.html](https://github.com/a2fapower/voxpen-web/blob/main/index.html) |
| `login.html` | ❓ 待评估 | Magic link 中间页,当前生产用邮箱 OTP 6 位数字模式,**目前没用到**。后续如启用 magic link 流程再决定是否迁移到 voxpen-web |
| `marketing/` | 已迁移到 voxpen-web | 本仓副本保留作历史,不再更新 |
| `_test_typeless/` | 调研截图 | 已删除(下次 commit) |

## 引用本仓?请改引用 voxpen-web

- 旧引用:`https://a2fapower.github.io/voxpen-legal/privacy.html`
- 新引用:`https://voxpen.cn/privacy.html`

iOS App / Mac App / Win App 内的隐私政策链接、App Store Connect 配置、微信公众号合规材料等所有外部引用都应该更新到 voxpen.cn 域名。

## 关联仓库(全集)

- [voxpen-web](https://github.com/a2fapower/voxpen-web) — 公开主页 + 法务 + 营销
- [voxpen-design](https://github.com/a2fapower/voxpen-design) — 三端设计系统
- [voxpen-mac](https://github.com/a2fapower/voxpen-mac) — macOS 客户端
- [voxpen-win](https://github.com/a2fapower/voxpen-win) — Windows 客户端
- [voxpen-ios](https://github.com/a2fapower/voxpen-ios) — iOS 客户端 + 键盘扩展
- [voxpen-server](https://github.com/a2fapower/voxpen-server) — 后端 / WS / ASR / 润色
