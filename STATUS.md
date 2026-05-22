# voxpen-legal · STATUS(归档)

> [!warning] **本仓库已于 2026-05-23 废弃**。详见 [README.md](./README.md)。
> 主页 + 法务 + 营销迁移至 [voxpen-web](https://github.com/a2fapower/voxpen-web)。

## 当前状态

**归档,只读**。本仓不再接受 PR 或常规更新。

唯一例外:

- `asc-privacy-questionnaire.md` — App Store 提审前可以更新对齐生产(目前仍是这里维护,因为提审材料跟公开主页不同,不适合放 voxpen-web)

## 历史完成(已不再活跃)

- 2026-05-12 **#2 隐私政策对齐 SIWA**(PR #8 已 merge)
  - 当时的 `privacy.md` 重写,加 SIWA / 邮箱 / 热词云端三块。**该版本现已过时**,新版在 voxpen-web/privacy.html(2026-05-23 重写加了邮箱 OTP / Supabase / MetricKit / 三端等)
  - `asc-privacy-questionnaire.md` 新增
  - `marketing/` 三份模板新增

## 待办 issue(转移指引)

废弃前留下的 open issue:

| Issue | 处理 |
|---|---|
| [#1](https://github.com/a2fapower/voxpen-legal/issues/1) favicon + OG image | 已在 voxpen-web 部分覆盖, 转 voxpen-web 跟进 |
| [#3](https://github.com/a2fapower/voxpen-legal/issues/3) P0 自媒体物料(手工) | 转 voxpen-web 跟进 |
| [#4](https://github.com/a2fapower/voxpen-legal/issues/4) 落地页升级 | 转 voxpen-web 跟进 |
| [#5](https://github.com/a2fapower/voxpen-legal/issues/5) 定价 / 试用对外口径 | 转 voxpen-web 跟进 |
| [#6](https://github.com/a2fapower/voxpen-legal/issues/6) voxpen.cn 域名决策 | **已落实**(2026-05-19 备案通过 + 2026-05-22 邮件链路 + 2026-05-23 主页迁移),可关闭 |
| [#7](https://github.com/a2fapower/voxpen-legal/issues/7) 客服 SOP | 转 voxpen-web 跟进或继续作产品决策类 |
| [#9](https://github.com/a2fapower/voxpen-legal/issues/9) terms.md 重写 | **已在 voxpen-web/terms.html 完成**,可关闭 |
| [#10](https://github.com/a2fapower/voxpen-legal/issues/10) sitemap.xml / robots.txt | **已在 voxpen-web 完成**,可关闭 |
| [#11](https://github.com/a2fapower/voxpen-legal/issues/11) privacy.md 补充手机号 + 微信 + MetricKit | 部分完成(MetricKit + Supabase 已加),手机号 / 微信等启用后再补 voxpen-web/privacy.html |

## 不再需要的内容(已删除或将删除)

- `_test_typeless/` 调研截图 + JS 脚本(已删除)
