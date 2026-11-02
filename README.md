# Reese Tunnel

**Reese Tunnel** is an Android VPN and tunneling application developed and maintained by **John Reese**. It is designed to route a phone's network traffic through supported SSH- and V2Ray-based tunnel profiles using Android's `VpnService`.

## What it does

- Connects supported SSH tunnel configurations.
- Imports and uses supported V2Ray profiles, including VLESS, VMess, and Trojan where the selected transport is supported.
- Offers separate Stream and Gaming mode selections. Gaming mode is intended to forward UDP for compatible tunnel profiles; real-world compatibility depends on the server, protocol, carrier transport, Android device, and the app/game.
- Imports and exports Reese Tunnel configuration files. Some file protections can be tied to a password or device, depending on the export settings and file format.

This repository is a **public product-information and release-announcement page only**. Reese Tunnel's application source code, native libraries, build scripts, signing keys, and private development files are not published here. A public repository does not mean that the application is open source or that its code may be copied or redistributed.

## Project details

- Product: Reese Tunnel
- Product owner and maintainer: John Reese
- Android application ID: `com.johnreese.fsociety`
- Current documented development version: **3.23.25** (version code 142)
- Minimum Android API declared by the app: **24** (Android 7.0)
- Supported ARM package targets: `arm64-v8a` and `armeabi-v7a`

Version details describe the current development build, not a guarantee that a corresponding signed public release is available. Consult the Releases page before downloading; do not install APKs from unofficial mirrors.

## Limitations and status

VPN and gaming behavior varies by server configuration and network. In particular, **Free Fire login and match connectivity have not been confirmed fixed on a physical device**. A successful tunnel status or ping does not by itself prove that game traffic is reaching and returning from the game service.

Cloud configuration import/export, automatic update enforcement, and a mandatory update lockout are not currently documented as available features. Do not assume that an update is required to connect unless a future release notice says so.

## Security and responsible use

Use only tunnel servers and configuration files you are authorized to use. Protect exported files and their passwords. Device binding or encryption raises the bar against casual access but cannot make data impossible to inspect on a device controlled by an attacker or owner with root/debugging access. Do not post passwords, signing keys, private configuration files, or sensitive exploit details in public repository issues.

## Releases

Official release information will be posted under [GitHub Releases](https://github.com/REESETUNNEL/REESE-TUNNEL/releases) when a signed release is ready. Always verify the release notes and package variant for your device architecture. An unsigned APK is not an install-ready official release.

## Ownership and license

Reese Tunnel is a product of John Reese. No application source code or open-source license is included in this repository. Unless a separate written license is provided, no permission is granted to copy, modify, redistribute, or rebrand the application or its private source code. Trademarks and third-party components remain the property of their respective owners.
