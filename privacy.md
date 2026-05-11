---
title: Privacy Policy / 隐私政策
---

# Privacy Policy / 隐私政策

**Last Updated / 最后更新：2026-05-10**

VoxPen is made by a2fapower. This policy tells you exactly what data VoxPen collects, why, and what you can do about it — in plain language, no legal boilerplate.

VoxPen 由 a2fapower 开发。本政策用产品语言说清楚 VoxPen 收集了什么数据、为什么收集、你能对它做什么。

---

## 1. 我们收集什么 / What We Collect

### 1.1 账户信息（使用 Apple 登录时）

当你选择用 Apple 账号登录 VoxPen 时，我们会收集：

- **Apple 用户标识符（Apple ID sub）**：Apple 分配的不透明用户 ID，用于识别你的账户。这个 ID 不含你的真实姓名，只在我们系统内部使用。
- **邮箱地址**：Apple 首次授权时提供。如果你选择在 Apple 登录页面隐藏邮箱，我们只拿到 Apple 提供的中继邮箱（relay 邮箱），不是你的真实邮箱。
- **显示名称**：默认用你的邮箱作为显示名称，仅显示在 VoxPen App 内的账户页面，不公开。
- **账户创建时间 / 最近活跃时间**：用于账户管理和删除账户时的数据清理。

登录是可选功能。VoxPen 核心录音功能需要登录，主要是为了把你的自定义热词同步到云端。

---

When you sign in with Apple, we collect:

- **Apple User Identifier (sub)**: An opaque ID assigned by Apple. It doesn't contain your real name and is only used inside our system.
- **Email address**: Provided by Apple on first sign-in. If you hide your email on Apple's login page, we only receive Apple's relay address, not your real one.
- **Display name**: Defaults to your email address; shown only inside VoxPen's account screen, never publicly visible.
- **Account creation and last active timestamps**: Used for account management and cleanup on deletion.

Sign-in is required for cloud hotword sync.

---

### 1.2 自定义热词

你在 VoxPen 里添加的自定义热词（例如：专有名词、人名、产品名），会存储在我们的服务器上，与你的账户关联。热词不含任何录音或转写内容，只是你主动输入的词语列表。

Your custom hotwords (e.g., proper nouns, names, product terms you add to improve recognition accuracy) are stored on our server, linked to your account. Hotwords contain only the words you explicitly add — no audio, no transcriptions.

---

### 1.3 语音录音（仅在请求处理期间）

当你使用 VoxPen 录音时：

1. 录音在你的设备上捕获。
2. 音频数据通过加密 WebSocket 连接（WSS / TLS）上传到我们的语音识别服务器（`voice.orgn.bio`）。
3. 服务器完成识别 + AI 润色，返回转写文字。
4. **录音音频不在服务器持久化保存**——处理完成后立即从内存销毁，不写入磁盘。
5. 转写文字通过键盘 API 插入到你当前使用的 App。**VoxPen 不在云端存储转写文字。**

请求过程中音频与你的账户 JWT 关联（用于鉴权），但音频内容本身不被持久化保存。

---

When you record with VoxPen:

1. Audio is captured on your device.
2. It's sent over an encrypted WebSocket (WSS / TLS) to our server (`voice.orgn.bio`).
3. The server transcribes and AI-polishes the speech, then returns the text.
4. **Audio is never persisted on the server** — it lives only in memory during processing and is destroyed immediately after.
5. Transcribed text is inserted via the keyboard API. **VoxPen does not store transcriptions in the cloud.**

Audio requests are authenticated with your account token, but the audio content itself is not retained.

---

### 1.4 设备本地数据

VoxPen 在你的设备上本地存储以下数据（iOS App Group 沙盒隔离）：

- 用户偏好设置（例如自动关闭时长）
- 当前键盘与主 App 之间的进程间通信状态

这些数据不会上传，卸载 App 时一并删除。

---

VoxPen stores the following locally on your device (within the iOS App Group sandbox):

- User preferences (e.g., auto-close duration)
- Keyboard-to-app inter-process state

This data is never uploaded and is deleted when you uninstall.

---

### 1.5 我们不收集什么

- **不收集**：转写文字的历史记录
- **不收集**：你在其他 App 中输入的任何内容（VoxPen 键盘扩展的"完全访问"权限仅用于将结果回传给键盘，不读取其他内容）
- **不集成**任何第三方广告、追踪或分析 SDK（Firebase Analytics、Adjust、Sentry、Facebook SDK、AppsFlyer 等一律没有）
- **不收集**：位置信息、健康数据、通讯录、浏览历史

---

We do NOT collect:

- Transcription history
- Anything you type in other apps (the keyboard extension's "Allow Full Access" is used only to return results — it does not read other app content)
- Any third-party ad, tracking, or analytics SDK data (no Firebase, Adjust, Sentry, Facebook SDK, AppsFlyer, etc.)
- Location, health, contacts, or browsing data

---

## 2. 为什么收集 / 为什么这样用 / Why and How

| 数据 | 用途 | 法律依据 |
|---|---|---|
| Apple 用户标识符 + 邮箱 | 账户创建、识别你的身份、热词跨端同步 | 合同履行（提供服务所必须） |
| 热词列表 | 提升你专属的语音识别准确率；iOS/Mac 两端共享同一份热词 | 合同履行 |
| 语音录音（处理中） | 执行语音转文字 + AI 润色，这是 VoxPen 的唯一核心功能 | 合同履行 |

我们不把你的数据卖给任何人，不用于广告，不用于训练模型（你的录音处理完即销毁，根本没有原料可用）。

---

| Data | Purpose | Legal basis |
|---|---|---|
| Apple user ID + email | Account creation, identity, hotword sync | Contract performance |
| Hotword list | Personalized recognition accuracy; shared across iOS and Mac | Contract performance |
| Voice audio (in-flight) | Core function: transcription + AI polish | Contract performance |

We never sell your data, use it for advertising, or train models on it (audio is destroyed immediately after processing).

---

## 3. 存在哪 / 存多久 / 谁能访问 / Storage, Retention, Access

- **账户数据（Apple ID sub、邮箱、热词）**：存储在我们在阿里云上的服务器（中国大陆数据中心）。传输使用 TLS 加密。你注销账户时，我们会永久删除所有与你账户关联的数据（users + login_methods + hotwords 三张表全删），时间不超过 7 天。
- **语音录音**：不在服务器保存，处理完毕即销毁，无保留期。
- **访问权限**：只有系统本身（自动化流程）会访问你的数据。开发者（a2fapower）在调试 bug 时可能查看匿名化的服务器日志（日志不含转写文字），不会主动翻阅个人账户数据。

---

- **Account data (Apple ID sub, email, hotwords)**: Stored on our Alibaba Cloud server (mainland China data center), encrypted in transit (TLS). On account deletion, all data is permanently removed within 7 days.
- **Voice audio**: Never persisted; destroyed immediately after processing.
- **Access**: Only automated systems access your data. The developer (a2fapower) may review anonymized server logs for bug debugging — logs do not contain transcription content.

---

## 4. 你能做什么 / Your Rights and Controls

### 查看账户信息
打开 VoxPen App → 设置 → 账户，可以看到你的显示名称和登录方式。

### 删除账户
打开 VoxPen App → 设置 → 账户 → 删除账户。确认后，我们会删除你的 Apple 用户标识符、邮箱、热词等所有账户数据（7 天内完成）。

删除账户后，你在服务器上的热词也会一起删除，热词不再跨端同步。App 本身仍可使用，但不再有云端热词功能。

如果 App 内删除账户功能遇到问题，发邮件到 a2fapower@gmail.com，我们会在 5 个工作日内处理。

### 撤回同意
你可以随时撤回 Apple 登录授权：打开 iPhone 设置 → 你的名字 → 密码与安全性 → 使用 Apple 账户登录 → 找到 VoxPen → 停止使用。这会在 Apple 侧撤回授权，我们的服务器会在你下次尝试使用时拒绝旧 token。

### 卸载 App
卸载 VoxPen 后，设备本地数据全部删除。服务器上的账户数据保留 90 天（方便你重新安装时还原热词），90 天后自动删除。如需提前删除，邮件联系即可。

---

### View your account
Open VoxPen → Settings → Account to see your display name and login method.

### Delete your account
Open VoxPen → Settings → Account → Delete Account. All account data (Apple user ID, email, hotwords) will be permanently deleted within 7 days.

After deletion, cloud hotword sync is disabled. The app still works, just without cloud hotwords.

If in-app deletion doesn't work, email a2fapower@gmail.com and we'll handle it within 5 business days.

### Revoke Apple sign-in
iPhone Settings → Your Name → Password & Security → Apps Using Apple ID → VoxPen → Stop Using. This revokes Apple's authorization; our server will reject old tokens on next use.

### Uninstall
Uninstalling deletes all local data. Server-side account data is retained for 90 days (for easy re-installation), then auto-deleted. Email us for earlier deletion.

---

## 5. 第三方服务 / Third-Party Services

VoxPen 使用以下第三方服务：

### 阿里云百炼（Alibaba Cloud Bailian）
**用途**：语音识别（fun-asr-realtime ASR 引擎）和 AI 文本润色（Qwen 大语言模型）。你的语音录音在处理期间会经过百炼的 API。阿里云的隐私政策适用于这段数据传输。百炼不会持久化存储你的录音内容（根据 API 调用模式，数据在请求生命周期内处理）。

**Alibaba Cloud Bailian**
Purpose: Speech recognition (fun-asr-realtime) and AI text polish (Qwen LLM). Your audio passes through Bailian's API during processing. Alibaba Cloud's privacy policy applies to this data transit. Audio is not retained by Bailian beyond the API request lifecycle.

### Apple Sign in with Apple（SIWA）
**用途**：用户登录授权。Apple 会验证你的身份并向我们提供用户标识符和（可选）邮箱。Apple 的隐私政策适用于 SIWA 流程中 Apple 侧的数据处理。

**Apple Sign in with Apple (SIWA)**
Purpose: User authentication. Apple verifies your identity and provides a user identifier and optional email to us. Apple's privacy policy governs Apple-side processing.

---

## 6. 儿童隐私 / Children's Privacy

VoxPen 不面向 13 岁以下儿童，也不有意收集任何儿童的信息。

VoxPen is not directed at children under 13 and does not knowingly collect data from children.

---

## 7. 政策更新 / Policy Updates

当我们修改隐私政策时，会更新本页面顶部的"最后更新"日期，并在 App 内以通知告知重大变更。

When we update this policy, we'll update the "Last Updated" date above and notify you in-app for material changes.

---

## 8. 联系我们 / Contact Us

对于任何隐私相关问题、账户删除请求、数据查询，请联系：

For any privacy questions, account deletion requests, or data inquiries:

**Email**: a2fapower@gmail.com

我们通常在 5 个工作日内回复。We typically respond within 5 business days.
