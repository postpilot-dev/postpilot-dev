# PostPilot

Stop switching between API client, DB tools, and JSON viewers.

## Why I built this

I kept doing this all day:

- Call API → get response
- Copy ID
- Open DB tool → paste → query
- Go back to API → repeat

Too much context switching. Too much copy-paste.

So I built PostPilot to keep everything in one flow.

https://github.com/user-attachments/assets/a759e944-c214-4c7a-95f5-134420f69963

---

## Download

### Free 14-Day Trial — no credit card required

| Platform | File | Requirement |
|----------|------|-------------|
| Windows | `PostPilot-Setup-x.x.x.exe` | Windows 10 or later |
| macOS | `PostPilot-x.x.x.dmg` | macOS 10.15 or later |
| Linux | `PostPilot-x.x.x.AppImage` | Ubuntu 18.04+, Fedora 32+ |

> See the [Releases](../../releases) page for all versions and release notes.

---

## Features

- **Fully Local** — Work offline with full privacy. All requests, queries, and data live safely on your device.
- **All in One Place** — API client, database client, and JSON/XML inspector in a single workspace.
- **Variables & Collections** — Define reusable variables, group requests, and resume your workspace where you left off.
- **Lightweight** — Fast startup, minimal UI, no bloat.

---

## What You Can Do

| Feature | Details |
|---------|---------|
| **API Testing** | Send HTTP requests (method, URL, headers, body)<br>Inspect responses with built-in JSON viewer<br>Extract and reuse values from responses as variables<br>Save and organize requests in collections |
| **Database Query** | Connect to PostgreSQL, MySQL, SQLite and more<br>Run SQL queries and browse table metadata<br>Extract values from results as variables<br>Save and reuse queries |
| **Data Inspection** | Import JSON/XML from clipboard, file, or API response<br>Format, validate, and search by key or value<br>Run multiple JSONPath queries at once |
| **Environment & Variables** | Define variables at workspace or environment scope<br>Reference variables across API requests and queries<br>Switch environments without rewriting requests |
| **Private Workspace** | All data stored locally on your device<br>No cloud sync, no account required<br>Workspace persists across sessions |

---

## Installation

### Windows
1. Download `PostPilot-Setup-x.x.x.exe`
2. Run the installer and follow the wizard
3. Launch from Start menu or desktop shortcut

### macOS
1. Download `PostPilot-x.x.x.dmg`
2. Open the DMG, drag PostPilot to Applications
3. Launch from Applications

> If you see a security warning: System Preferences → Security & Privacy → "Open Anyway"

### Linux
1. Download `PostPilot-x.x.x.AppImage`
2. `chmod +x PostPilot-x.x.x.AppImage`
3. `./PostPilot-x.x.x.AppImage`

<details>
<summary>Verify Linux release (recommended)</summary>

All Linux releases are signed with GPG and include SHA256 checksums.

**Import signing key (once):**
```bash
curl -fsSL https://raw.githubusercontent.com/postpilot-dev/postpilot-dev/main/linux/postpilot-linux-signing-public.asc | gpg --import
```

**Verify:**
```bash
gpg --verify PostPilot_1.x.x_amd64.AppImage.asc PostPilot_1.x.x_amd64.AppImage
sha256sum -c PostPilot_1.x.x_amd64.AppImage.sha256
```

Expected output:
- `Good signature from "Lac Tran An (PostPilot.Dev Linux Release Signing Key) <anlac96.it@gmail.com>"`
- `PostPilot_1.x.x_amd64.AppImage: OK`

</details>

---

## Pricing

**Desktop Pro — $40 one-time**

- 14-day free trial, no credit card required
- Perpetual license — pay once, own forever
- 1 year of updates included
- 1 device license

After 1 year: keep using your current version forever, or optionally renew for new features.

---

## License & Privacy

**License**: The desktop app requires periodic online verification. After the 14-day trial, a $40 license is required. See [Terms of Service](https://www.postpilot.dev/terms-of-service).

**Privacy**: All workspace data is stored on your device. No cloud sync. Anonymous telemetry is opt-out. See [Privacy Policy](https://www.postpilot.dev/privacy-policy).

---

## Getting Started

1. Download and install for your platform
2. Launch — your 14-day free trial starts automatically
3. Create API requests, database queries, or inspect data
4. Use variables and collections to organize your work
5. After 14 days, purchase a $40 license to keep going

Docs and guides: [www.postpilot.dev](https://www.postpilot.dev)

---

## Frequently Asked Questions

<details>
<summary>How does the 14-day trial work?</summary>

Starts automatically on first launch. No credit card required. Full access to all features. After 14 days, purchase a $40 license to continue.

</details>

<details>
<summary>What happens after 1 year?</summary>

Your license never expires. Keep using your current version indefinitely. Renew only if you want new features and updates.

</details>

<details>
<summary>Can I use PostPilot on multiple devices?</summary>

The $40 license covers 1 device. You'll need a separate license for each additional device.

</details>

<details>
<summary>What if I change my computer?</summary>

Email anlac96.it@gmail.com to transfer your license to a new device.

</details>

<details>
<summary>Do I need an internet connection?</summary>

The app requires periodic online verification for license validation. After that, you can work fully offline.

</details>

<details>
<summary>Is my data secure and private?</summary>

Yes. All workspace data is stored locally. We never access your API requests, queries, or any sensitive data. See [Privacy Policy](https://www.postpilot.dev/privacy-policy).

</details>

<details>
<summary>Can I get a refund?</summary>

Since PostPilot has a 14-day free trial, we encourage you to fully evaluate before purchasing. Refund policy is as displayed at time of purchase.

</details>

---

## Looking for a Free Alternative?

Try the **[free web version](https://www.postpilot.dev/workspace)** — no install, works in your browser.

| | Web (Free) | Desktop Pro ($40) |
|--|--|--|
| API client | ✅ | ✅ |
| Data inspector | ✅ | ✅ |
| Environment variables | ✅ | ✅ |
| Database client | ❌ | ✅ |
| Offline mode | ❌ | ✅ |
| No account required | ✅ | ✅ |

---

## Support

- **Website**: [www.postpilot.dev](https://www.postpilot.dev)
- **Issues**: [GitHub Issues](../../issues)
- **Email**: anlac96.it@gmail.com

---

## Legal

- [Terms of Service](https://www.postpilot.dev/terms-of-service)
- [Privacy Policy](https://www.postpilot.dev/privacy-policy)

---

**© 2026 Lac Tran An. All rights reserved.**
