# Solution4Tec Desktop

Solution4Tec Desktop is a companion application for Solution4Tec customers.  
It provides a streamlined way to access and manage your Solution4Tec company instances from your desktop, with built‑in support for update checks and configuration.

> **Note:** This repository is a **public releases** repository.  
> The application source code is maintained in a separate private repository.

---

## Features

- **Quick access to company instances**  
  Open your Solution4Tec dashboards directly from the desktop app.

- **Company lookup integration**  
  Resolve company URLs and names via the Solution4Tec API.

- **Automatic and manual updates**  
  Built‑in support for:
  - Automatic background update checks.
  - Optional automatic download and install on quit.
  - Manual “check for updates” and “download update” triggers.

- **User preferences**  
  Remembers window size/position, fullscreen/start‑maximized behavior, and app theme.

---

## Installation

### Windows

1. Download the latest `S4Desktop Setup x.y.z.exe` from the **Releases** page of this repository.
2. Run the installer and follow the setup wizard.
3. Launch “Solution4Tec” from the Start Menu.

### macOS

1. Download the latest `.dmg` or `.zip` from **Releases**.
2. Open the `.dmg` / extract the `.zip`.
3. Drag the “Solution4Tec” app into your `Applications` folder.
4. Launch it from Applications or Spotlight.

### Linux

1. Download the latest Linux artifact from **Releases** (e.g. `.AppImage` or `.deb`, depending on what is provided).
2. For AppImage:
   - Make it executable: `chmod +x S4Desktop-x.y.z.AppImage`
   - Run it: `./S4Desktop-x.y.z.AppImage`
3. For `.deb`:
   - Install: `sudo dpkg -i S4Desktop_x.y.z_amd64.deb`

---

## Updates

The app uses the Electron `electron-updater` integration to check for new versions.

### Automatic updates

When automatic updates are enabled in the app’s settings:

- On startup, the app checks the official release channel for a newer version.
- If an update is available:
  - It is downloaded automatically in the background.
  - Once ready, the app will install the update when you quit and restart the app.

This is the recommended mode for most users to stay secure and up to date.

### Manual “Check for updates”

If you prefer more control:

- You can trigger a **“Check for updates”** action from within the app (e.g. from the settings or about dialog, depending on UI).
- The app will check for a newer version and report whether an update is available.

### Manual download and install

If automatic download is disabled:

- When the app detects a mandatory or recommended update, it can:
  - Show a notification or dialog inside the app.
  - Offer a **“Download update”** action.
- When you confirm, the app downloads the update and installs it on quit.

---

## Configuration

Some aspects of the app behavior depend on your organization’s Solution4Tec configuration and backend environment.

Typical configuration items (set by Solution4Tec or your admin) include:

- **Company lookup API endpoint** – the base URL used by the desktop client to resolve company instances.
- **Desktop API key** – a secret configured on the backend; the desktop app uses a corresponding key to authenticate its lookup requests.

These details are normally pre‑configured in the distributed binaries or managed by your organization’s IT team. End users usually do **not** need to configure API keys or endpoints manually.

If you believe your desktop client is misconfigured (e.g. cannot reach the API or cannot resolve your company instance), please contact your Solution4Tec administrator or Solution4Tec support.

---

## Privacy & Security

- The desktop client communicates with Solution4Tec backend services over HTTPS.
- Local settings (e.g. window layout, theme, auto‑update preference) are stored on your machine.
- Security‑relevant updates are delivered through the auto‑update mechanism when available.

For security reporting and supported versions, see [`SECURITY.md`](./SECURITY.md).

---

## License

This software is proprietary and licensed by Solution4Tec GmbH.  
See [`LICENSE.md`](./LICENSE.md) for details.
