---
title: Privacy Policy / 隐私政策
---

# Privacy Policy / 隐私政策

**Last Updated / 最后更新:2026-04-25**

VoxPen is developed and operated by a2fapower ("we", "our", "VoxPen"). This Privacy Policy explains how VoxPen handles data when you use the app.

VoxPen 由 a2fapower 开发并运营("我们"、"VoxPen")。本政策说明 VoxPen 在你使用 App 时如何处理数据。

---

## 1. We Do Not Collect Your Personal Information / 我们不收集你的个人信息

VoxPen does not create accounts, require registration, or collect any identifying information about you (name, email, phone, device ID, IDFA, etc.).

VoxPen 不创建账户、不要求注册、不收集任何识别你身份的信息(姓名、邮箱、电话、设备 ID、IDFA 等)。

VoxPen integrates **no third-party tracking, analytics, or advertising SDKs** (such as Firebase Analytics, Adjust, Sentry, Facebook SDK, AppsFlyer, etc.).

VoxPen **不集成任何第三方追踪、分析、广告 SDK**(如 Firebase Analytics、Adjust、Sentry、Facebook SDK、AppsFlyer 等)。

---

## 2. How We Handle Voice Recordings / 语音录音处理

When you record voice with VoxPen:

1. The recording is captured on your device.
2. Audio data is uploaded over an encrypted WebSocket connection (WSS / TLS) to our transcription server (`voice.orgn.bio`).
3. The server performs speech recognition and text refinement, then returns the transcribed text.
4. **The audio recording is not persisted on the server.** It exists only in memory during processing and is destroyed immediately after the response is returned.
5. The transcribed text is inserted into the current app's input field via the standard iOS keyboard API. **VoxPen does not store any transcribed text in the cloud.**

当你使用 VoxPen 录音时:

1. 录音在你的设备上捕获;
2. 音频数据通过加密 WebSocket 连接(WSS / TLS)上传到我们的转写服务器(`voice.orgn.bio`);
3. 服务器执行语音识别 + 文本润色,返回转写文本;
4. **录音音频不在服务器持久化保存**,仅在请求处理期间存在于内存,响应返回后立即销毁;
5. 转写文本通过 iOS 标准键盘 API 插入到当前 App 的输入框。**VoxPen 不在云端存储任何转写文本。**

---

## 3. Local Data / 本地数据

VoxPen stores the following data on your device only (within an App Group sandbox, isolated by iOS at the system level):

- User preferences (auto-close duration, hotword list)
- Current voice transcription state (for inter-process communication between the main app and keyboard extension)

This data is **never uploaded**, used only by the app itself, and is deleted when you uninstall the app.

VoxPen 在你的设备上存储以下数据(均位于 App Group 沙盒,iOS 系统级别隔离):

- 用户偏好设置(自动关闭时长、热词列表)
- 当前语音转写状态(供主 App 与键盘扩展之间进程间通信)

这些数据**永远不会上传**,只供 App 自身使用,卸载 App 时一并删除。

---

## 4. iOS Permissions / iOS 权限

VoxPen requires the following iOS permissions, all used solely for core functionality:

- **Microphone**: For recording your voice to transcribe to text.
- **Keyboard Extension "Allow Full Access"**: For communication between the keyboard and the main app (returning transcription results). **VoxPen does not read or upload anything you type in other apps.**

You can revoke these permissions at any time in iOS Settings. The app will display a notice if revoked, and some features will not work.

VoxPen 需要以下 iOS 权限,所有权限仅为 App 核心功能服务:

- **麦克风**:为录制你的语音并转写为文字。
- **键盘扩展"允许完全访问"**:为让键盘与主 App 通信(转写结果回传)。**VoxPen 不会读取或上传你在其他 App 中输入的任何内容。**

你可在 iOS 设置中随时撤销这些权限。撤销后 App 会显示提示,部分功能将无法使用。

---

## 5. Data Security / 数据安全

- All network transmission is encrypted using TLS / WSS.
- The server holds audio data only temporarily during request processing, destroyed immediately after.
- We do not store logs, accounts, or transcription history.

- 所有网络传输使用 TLS / WSS 加密。
- 服务器仅在请求处理期间临时持有音频数据,处理完成立即销毁。
- 我们不储存日志、不储存账户、不储存转写历史。

---

## 6. Children's Privacy / 儿童隐私

VoxPen is not directed at children under 13 and does not knowingly collect information from children.

VoxPen 不针对 13 岁以下儿童,也不有意收集任何儿童的信息。

---

## 7. Policy Updates / 政策更新

If this policy changes, we will update the "Last Updated" date on this page. Material changes will be communicated within the app.

如本政策变更,我们将在此页面更新"最后更新"日期。重大变更时会在 App 内通知。

---

## 8. Contact Us / 联系我们

For any privacy-related questions, please contact:

如有任何隐私相关问题,请联系:

**Email**: a2fapower@gmail.com
