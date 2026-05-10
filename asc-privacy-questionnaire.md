# App Store Connect Privacy Questionnaire
# VoxPen — Updated for SIWA (Sign in with Apple) Integration
# Last Updated: 2026-05-10

---

## Q1: Does your app or any third-party partner collect data from this app?

**Yes**

---

## Q2: Data Types — Detail by Category

### Contact Info

| Type | Collected | Linked to User | Used to Track | Purposes |
|---|---|---|---|---|
| **Email Address** | **Yes** | **Yes** | No | App Functionality (account identifier) |
| Name | No | — | — | — |
| Phone Number | No | — | — | — |
| Physical Address | No | — | — | — |
| Other Contact Info | No | — | — | — |

**Explanation**: When user signs in with Apple (SIWA), Apple provides the user's email address (or relay address if hidden). This is stored in `users.email` in our database, linked to the user account. Required for account creation and identification.

---

### Health & Fitness

| Type | Collected | Linked to User | Used to Track | Purposes |
|---|---|---|---|---|
| Health | No | — | — | — |
| Fitness | No | — | — | — |

---

### Financial Info

| Type | Collected | Linked to User | Used to Track | Purposes |
|---|---|---|---|---|
| Payment Info | No | — | — | — |
| Credit Info | No | — | — | — |
| Other Financial Info | No | — | — | — |

---

### Location

| Type | Collected | Linked to User | Used to Track | Purposes |
|---|---|---|---|---|
| Precise Location | No | — | — | — |
| Coarse Location | No | — | — | — |

---

### Sensitive Info

| Type | Collected | Linked to User | Used to Track | Purposes |
|---|---|---|---|---|
| Sensitive Info | No | — | — | — |

---

### Contacts

| Type | Collected | Linked to User | Used to Track | Purposes |
|---|---|---|---|---|
| Contacts | No | — | — | — |

---

### User Content

| Type | Collected | Linked to User | Used to Track | Purposes |
|---|---|---|---|---|
| Emails or Text Messages | No | — | — | — |
| Photos or Videos | No | — | — | — |
| **Audio Data** | **Yes** | **Yes** | No | App Functionality |
| Gameplay Content | No | — | — | — |
| Customer Support | No | — | — | — |
| Other User Content | No | — | — | — |

**Explanation for Audio Data**:
- Audio is captured on device, transmitted over WSS/TLS to `voice.orgn.bio` for transcription + AI polish.
- Audio is **not persisted** on the server — it is processed in memory and destroyed immediately after the response is returned.
- Audio requests are authenticated with a JWT (linked to `user_id`), therefore audio is **Linked to User = Yes**.
- **CHANGE from previous questionnaire**: Previously marked "Linked to User: No" (before SIWA/account system). With SIWA in place, audio requests carry the user's JWT, making this "Yes".

---

### Browsing History

| Type | Collected | Linked to User | Used to Track | Purposes |
|---|---|---|---|---|
| Browsing History | No | — | — | — |

---

### Search History

| Type | Collected | Linked to User | Used to Track | Purposes |
|---|---|---|---|---|
| Search History | No | — | — | — |

---

### Identifiers

| Type | Collected | Linked to User | Used to Track | Purposes |
|---|---|---|---|---|
| **User ID** | **Yes** | **Yes** | No | App Functionality (Apple sub as account ID) |
| Device ID | No | — | — | — |

**Explanation**: Apple Sign in with Apple provides an opaque `sub` (user identifier). This is stored in `login_methods.apple_sub`, linked to the user account. It is the primary identifier for the account system.

---

### Purchases

| Type | Collected | Linked to User | Used to Track | Purposes |
|---|---|---|---|---|
| Purchase History | No | — | — | — |

---

### Usage Data

| Type | Collected | Linked to User | Used to Track | Purposes |
|---|---|---|---|---|
| Product Interaction | No | — | — | — |
| Advertising Data | No | — | — | — |
| Other Usage Data | No | — | — | — |

---

### Diagnostics

| Type | Collected | Linked to User | Used to Track | Purposes |
|---|---|---|---|---|
| Crash Data | No | — | — | — |
| Performance Data | No | — | — | — |
| Other Diagnostic Data | No | — | — | — |

---

### Other Data

| Type | Collected | Linked to User | Used to Track | Purposes |
|---|---|---|---|---|
| **Custom Hotwords** | **Yes** | **Yes** | No | App Functionality (hotword sync across iOS + Mac) |

**Explanation**: Users can add custom hotwords (proper nouns, names, product terms) to improve speech recognition accuracy. These are stored on our server (`hotwords` table with `user_id` foreign key) and synced across iOS and Mac. Hotwords contain only words the user explicitly inputs — no audio, no transcription content.

---

## Q3: Does your app use data for tracking?

**No**

VoxPen does not track users across apps or websites owned by other companies. No advertising or tracking SDKs are integrated (no Firebase, Adjust, Facebook SDK, AppsFlyer, etc.).

---

## Summary of Changes vs. Previous Questionnaire (Pre-SIWA)

| Field | Old Answer | New Answer | Reason |
|---|---|---|---|
| Contact Info → Email Address | Not collected | **Yes, Linked to User** | SIWA passes email to `users.email` |
| Identifiers → User ID | Not collected | **Yes, Linked to User** | Apple `sub` stored in `login_methods.apple_sub` |
| Audio Data → Linked to User | No | **Yes** | JWT in WS header links audio to `user_id` |
| Other Data → Hotwords | Not collected | **Yes, Linked to User** | Hotwords moved to cloud, linked to account |
