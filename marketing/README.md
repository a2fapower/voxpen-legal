# VoxPen 自媒体物料清单

## 截图素材清单

### iOS 截图（必须，发布前）

| 文件名 | 内容 | 状态 |
|---|---|---|
| `ios/01-app-icon-homescreen.png` | iPhone 主屏幕，VoxPen 图标在旁边 | 待截 |
| `ios/02-keyboard-idle.png` | 备忘录里打开 VoxPen 键盘（录音前状态） | 待截 |
| `ios/03-keyboard-recording.png` | 按住录音按钮时（录音中状态） | 待截 |
| `ios/04-result-comparison.png` | 插入结果：口头禅版 vs 润色版 | 待截 |
| `ios/05-hotwords-page.png` | 热词管理页面（有几个热词在里面） | 待截 |
| `ios/06-account-page.png` | 登录状态下的账户/设置页 | 待截 |

**截图方法**：iPhone 侧键 + 音量键，或 Mac QuickTime 镜像截图（分辨率更高）

**截图状态建议**：
- 深色/浅色模式都截一份备用，首选浅色
- 热词页面：提前加几个真实感强的热词（如"VoxPen"、"百炼 ASR"、"会议纪要"）
- 结果对比截图：用一段有代表性的口头禅话（"嗯那个，我想说一下……" → "我想说一下，……"）
- 键盘截图：在"备忘录"或"微信"里截，这两个场景用户最熟悉

---

### Mac 截图（建议，发布后 1 周内）

| 文件名 | 内容 | 状态 |
|---|---|---|
| `mac/07-menubar-icon.png` | 菜单栏 V 图标 + 时间/电量 | 待截 |
| `mac/08-recording-in-app.png` | 在 Mac App（如备忘录）里触发录音 | 待截 |
| `mac/09-result-injected.png` | 文字注入后的效果 | 待截 |

**截图方法**：macOS Shift+Cmd+4（区域截图）

---

### 营销图（建议，发布后）

| 文件名 | 内容 | 尺寸 | 状态 |
|---|---|---|---|
| `marketing/og-image.png` | 社交分享封面 | 1200×630 | 待做（Canva）|
| `marketing/ios-mac-sync.png` | 跨端同步对比图 | 任意 | 待做（截图拼接）|

---

## 文件夹结构（本地截图建议路径）

```
~/Desktop/voxpen-screenshots/
├── ios/
│   ├── 01-app-icon-homescreen.png
│   ├── 02-keyboard-idle.png
│   ├── 03-keyboard-recording.png
│   ├── 04-result-comparison.png
│   ├── 05-hotwords-page.png
│   └── 06-account-page.png
├── mac/
│   ├── 07-menubar-icon.png
│   ├── 08-recording-in-app.png
│   └── 09-result-injected.png
└── marketing/
    ├── og-image.png
    └── ios-mac-sync.png
```

---

## 物料优先级

### P0 — 发布前必须有

1. iOS 核心功能截图 × 5 张（01-06）
2. 30 秒 demo 录屏（iOS 键盘）— 见 `demo-script.md`
3. 首发文案 × 4 条（小红书 / Twitter / 即刻 / B 站）— 见 `social-launch-templates.md`
4. 落地页更新：把 "Mac 版即将上线" 改成 "iOS 现已上线 App Store"（改 `../index.html`）

### P1 — 发布后 1 周内

5. Mac 端截图 × 3 张（07-09）
6. iOS + Mac 跨端同步对比图
7. 行业冲击型短文（律师/医生场景）
8. OG image / Twitter Card 封面图

### P2 — 有时间再做

9. 60 秒 B 站/抖音横版视频
10. 行业场景截图（律师法庭笔记 / 医生病历系统）
11. 英文版 Twitter/Product Hunt 文案
