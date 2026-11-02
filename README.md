# Reese Tunnel

**An Android VPN and tunnelling app by John Reese.** Reese Tunnel brings SSH, V2Ray, DNS tunnelling, UDP-Custom, and configuration-file tools together in one Android app.

> [!CAUTION]
> The earlier `3.23.27-test` prerelease was a Hello World updater test—not a VPN client—and was signed with Android's debug key. Android cannot update that package in place to the official release. If you installed it, back up any data or configuration files, uninstall the test app, then install the matching ARM APK below. Uninstalling may erase app data.

## What Reese Tunnel does

Reese Tunnel creates an Android VPN interface and routes device traffic through a configured tunnel. Available connection choices include:

- **SSH Stream** and **SSH Gaming** modes.
- **V2Ray Stream** and **V2Ray Gaming** modes, with UDP forwarding available for supported built-in-engine profiles.
- **VLESS, VMess, and Trojan** profile import, plus supported TCP/WebSocket transports. Profiles requiring additional transports may use the bundled Xray core; V2Ray Gaming is limited to compatible profiles and does not use that core for its UDP-forwarding path.
- **SlowDNS** and **UDP-Custom** connection options.
- Payload, SNI, remote-proxy, and DNS settings, along with connection logs, traffic totals, ping diagnostics, and other network utilities.
- ARM64 (`arm64-v8a`) and ARMv7 (`armeabi-v7a`) Android package variants.

Mode availability does not guarantee that every server, carrier, device, or game is compatible. Free Fire login and match connectivity have not been confirmed fixed across devices; a connected indicator alone does not prove that game traffic is working end to end.

## Reese Tunnel `.RT` configuration files

The app can import and export Reese Tunnel configuration files. New exports use an opaque binary format with authenticated encryption. An export must be protected by a password, an authorized hardware ID (HWID), or both; the APK signing certificate is not the file-encryption key. Exporters can also include a note for recipients.

Keep configuration files and passwords private. Encryption and device binding raise the barrier to casual inspection, but do not make a configuration impossible to recover from a device controlled by an attacker, a modified app, or someone who knows the password. Never publish a private configuration or its password in an issue or chat.

## Updates and releases

The app checks the GitHub-hosted [`latest.json`](latest.json) manifest and selects the supported ARM architecture when an update is available. Downloads are checked against the manifest's size and SHA-256 before Android's package installer is opened; installation still requires the user's confirmation.

**Current public release: [Reese Tunnel 3.23.28 (version code 146)](https://github.com/REESETUNNEL/REESE-TUNNEL/releases/tag/v3.23.28).** The manifest points to the two official release APKs and validates their expected size and SHA-256. The older `3.23.27-test` release remains a historical updater test and is not selected by the current manifest. Device-specific VPN and game connectivity can still vary.

## Project and credits

**Owner, creator, and maintainer:** John Reese, also known as Donquixote Doflamingo. Reese Tunnel is an independent project created by a Kenyan developer. It was inspired by the practical approach of HTTP Custom, but it is not affiliated with or endorsed by HTTP Custom.

**Testing and feedback:** Mjaba, Frontend Gidiz, and Kevo loves are credited in the app for testing, bug reports, and troubleshooting. Their feedback helped uncover issues across builds, devices, and network conditions.

## Project status and source

Reese Tunnel's Android source code and private development materials are **not** published in this repository. This repository is for public product information, release notices, and updater metadata; it is not an open-source source-code distribution. No permission to copy, modify, rebrand, or redistribute the private app or source code is granted by the presence of this public repository.

The 3.23.28 release refreshes the protected `.RT` import integrity pins for its signing certificate and packaged application fingerprints. It has passed the project's available automated unit tests and native cryptographic self-test; device-level behavior should be checked on the intended Android device.

## Security and responsible use

Use only tunnel servers and profiles you are authorized to use. Do not share passwords, private signing keys, or unredacted locked `.RT` files. Report security concerns privately to the maintainer rather than posting exploit details or sensitive configuration data publicly.

Third-party libraries and components remain the property of their respective authors and are governed by their own licenses. Reese Tunnel does not claim ownership of those components.

## Maintainer

For support, include the app version, device/Android version, selected tunnel mode, and relevant redacted log lines. Do not include passwords or private configs.

- WhatsApp: [John Reese](https://wa.me/254759424232)
- Telegram: [@donquixoted0flamingo](https://t.me/donquixoted0flamingo)
- Official website: [reesetunnel.com](https://reesetunnel.com)
- Website: [wifibypass.org](https://www.wifibypass.org)
