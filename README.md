<p align="center">
  <a href="README_fa.md"><img src="https://img.shields.io/badge/🇮🇷_فارسی-7c5cff?style=for-the-badge" alt="نسخه فارسی"></a>
</p>

<p align="center">
  <img src="assets/banner.png" alt="CLXY — Fast. Private. Yours." width="100%">
</p>

<p align="center">
  <a href="https://github.com/ClxybyCloner/CLXY-Android/releases/latest"><img src="https://img.shields.io/github/v/release/ClxybyCloner/CLXY-Android?label=latest&color=7c5cff" alt="Latest release"></a>
  <a href="https://github.com/ClxybyCloner/CLXY-Android/releases"><img src="https://img.shields.io/badge/Android-7.0%2B-3DDC84?logo=android&logoColor=white" alt="Android 7.0+"></a>
  <img src="https://img.shields.io/badge/arch-arm64--v8a-4f8cff" alt="arm64-v8a">
  <a href="https://github.com/ClxybyCloner/CLXY-Android/releases"><img src="https://img.shields.io/github/downloads/ClxybyCloner/CLXY-Android/total?label=downloads" alt="Total downloads"></a>
</p>

<h1 align="center">CLXY — Official Android Releases</h1>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=24&duration=2800&pause=1200&color=7C5CFF&center=true&vCenter=true&width=700&lines=Fast.+Private.+Yours.;Official+CLXY+Android+releases;One+tap+away+from+the+newest+build" alt="Fast. Private. Yours.">
</p>

This is the **official download & update channel** for the CLXY Android app.
Every release is published here — and the in-app updater checks this exact
repository, so if you're running CLXY, you're always one tap away from the
newest build.

<p align="center">
  <img src="assets/wave.svg" alt="" width="99%">
</p>

## ⬇️ Download

**Latest: 1.0.26**, released November 6, 2026

- 📦 [Download the ARM64 APK](https://github.com/ClxybyCloner/CLXY-Android/releases/download/v1.0.26/CLXY-1.0.26-Android-arm64-v8a.apk)
- [View the SHA-256 checksum](https://github.com/ClxybyCloner/CLXY-Android/releases/download/v1.0.26/SHA256SUMS.txt)
- 🗂️ [Browse all releases](https://github.com/ClxybyCloner/CLXY-Android/releases)

The source code is available under GPLv3 in the [separate public source repository](https://github.com/ClxybyCloner/CLXY-Android-public-source).

---

## ⚡ Why CLXY

- 🌍 **The open internet, in your pocket** — unblock the sites, apps and services restricted in your region. One tap and you're in.
- 🚀 **Built for speed** — a Go-powered core with HTTP/2 and HTTP/3 (QUIC) stays fast and stable, even on flaky mobile data.
- 🔒 **Your traffic stays yours** — a real encrypted VPN tunnel for the whole device, with per-app control over what goes through CLXY.
- 👨‍👩‍👧 **One subscription for everyone** — share your connection with nearby devices through hotspot proxies (HTTP `11811` / SOCKS5 `11812`).
- 👆 **No setup headaches** — open the app, tap connect, done.
- 🔄 **Always up to date** — the app notifies you the moment a new build is out; nothing installs without your approval.
- 🪶 **Light on your phone** — just ~20 MB, smooth on Android 7.0 and up, even older phones.

---

## CLXY core architecture

CLXY pairs a Flutter interface with an embedded Go networking core. The core runs as a library inside the app. The UI uses a local bridge and loopback API to manage settings and read connection status, while the core handles network traffic.

In VPN mode, Android's `VpnService` creates a virtual TUN interface. A user-space TCP/IP stack processes packets and forwards TCP connections to the core's SOCKS5 proxy. The built-in DNS resolver maps domain names to temporary IP addresses so routing rules can still match domains. These rules choose whether to use the proxy, connect directly, or block a connection. App selection controls which apps use the VPN.

The core supports HTTP/2 CONNECT over TLS and HTTP/3 CONNECT over QUIC for connections to the gateway. Proxy-only mode uses the same core without creating a device-wide VPN. The Android VPN path handles TCP and DNS; other UDP traffic is not tunneled.

---

## Install in 60 seconds

1. **Download** the APK from the link above.
2. **Open it** — Android will ask you to allow *"Install unknown apps"* for your browser. Allow it once.
3. **Tap Install.** Done.

A subscription is required to use CLXY.

---

## ✅ Verify your download

On a computer, calculate the APK's SHA-256:

```bash
sha256sum CLXY-1.0.26-Android-arm64-v8a.apk
```

Compare the output with this expected hash:

```text
6a49bc2594ab3f622374dae6c7e25344764ecfa3b1aab89971b0123592a28177  CLXY-1.0.26-Android-arm64-v8a.apk
```

If they match, the file is exactly what we published.

---

## 🔄 How updates work

CLXY periodically checks this repo's **Releases** for a newer version. When one
is found, you get a notification inside the app — tap it to download, then
confirm the install yourself. The app never installs anything behind your back.

---

## 📋 Current build specs

| | |
|---|---|
| Package | `com.clxy.android` |
| Version / version code | `1.0.26` / `14148` |
| Architecture | `arm64-v8a` |
| Minimum Android | 7.0 (API 24) |
| Size | 20.5 MB |

---

## ❓ FAQ

**Where is the source code?**
The public GPLv3 source is in the [CLXY Android source repository](https://github.com/ClxybyCloner/CLXY-Android-public-source). This repository holds the signed app releases and their checksums.

**I need an older version.**
Older builds stay available on the [Releases page](https://github.com/ClxybyCloner/CLXY-Android/releases).

**The hotspot proxy asks for nothing — is that safe?**
The hotspot HTTP/SOCKS5 proxies have no password by design, so **only turn them on on a hotspot you trust**, and switch them off when you're done. Anyone connected to your hotspot could use them.

---

<p align="center">
  <img src="assets/wave.svg" alt="" width="100%">
</p>

## 📜 Terms

The source and app are distributed under GPLv3. See the public source repository for the license and source code. Official signed releases and checksums are published here.
