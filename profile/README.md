# immurok

<p align="center">
  <img src="https://raw.githubusercontent.com/immurok/.github/main/profile/images/prd-preview.jpg" alt="immurok IK-1" width="600">
</p>

**Wireless fingerprint authenticator for Mac, Windows, Linux, and your AI coding agent.**

One touch to unlock your screen, authorize sudo, sign SSH commits, and gate the commands your AI agent runs on your behalf.

immurok is a hardware security key with a built-in fingerprint sensor, with all source code public on GitHub. It brings biometric authentication to Mac, Windows, and Linux machines — desktops, clamshell laptops, and headless servers — and to AI coding agents, all over Bluetooth LE.

## Features

- **Screen unlock** — Touch to unlock the macOS lock screen, Windows login (native Credential Provider), and Linux login
- **sudo / polkit** — Fingerprint replaces password for privilege escalation (macOS/Linux)
- **Dual-host** — Bind two computers at once; touch a dedicated switch fingerprint to move the device between them
- **SSH agent** — On-device ECDSA key generation and signing (private key never leaves the device)
- **TOTP** — Hardware-backed one-time passwords with Quick Fill
- **Password manager unlock (macOS)** — Fingerprint unlocks 1Password / Bitwarden with a separately stored vault password
- **AI agent authorization** — Wrap an agent's subprocess with `imk run --agent --`. One fingerprint touch authorizes sudo + SSH signing + secret reads for the entire wrapped command; reject it and the subprocess gets `SIGTERM`.
- **Mutual authentication** — ECDH P-256 pairing + HMAC-SHA256 signed notifications

## Repositories

| Repository | Description |
|------------|-------------|
| [immurok](https://github.com/immurok/immurok) | Project overview, BLE protocol spec, and security whitepaper |
| [firmware](https://github.com/immurok/firmware) | CH592F main application firmware |
| [ota](https://github.com/immurok/ota) | OTA bootloader and firmware update tools |
| [app-macos](https://github.com/immurok/app-macos) | macOS companion app (Swift) |
| [app-win](https://github.com/immurok/app-win) | Windows companion app — .NET service + Credential Provider (C# / C++) |
| [app-linux-rs](https://github.com/immurok/app-linux-rs) | Linux companion app — daemon + CLI (Rust) |
| [imk-skill](https://github.com/immurok/imk-skill) | AI-agent skill — how Claude Code / Cursor / Codex / Cline / Gemini CLI use `imk run --agent` to gate privileged commands |
| [hardware](https://github.com/immurok/hardware) | Hardware design, schematics, and component selection |

## License

All source code is public. The companion apps — [app-macos](https://github.com/immurok/app-macos) (including the PAM module), [app-win](https://github.com/immurok/app-win), and [app-linux-rs](https://github.com/immurok/app-linux-rs) — are open source under the **Apache License 2.0**. Firmware, hardware, and the remaining repositories are source-available under [BSL 1.1](https://github.com/immurok/immurok/blob/main/LICENSE) — personal, education, and research use permitted; converts to Apache 2.0 on 2030-03-05.
