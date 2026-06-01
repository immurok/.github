# immurok

<p align="center">
  <img src="https://raw.githubusercontent.com/immurok/immurok/main/assets/device.png" alt="immurok" width="320">
</p>

**Wireless fingerprint authenticator for Mac, Linux, and your AI coding agent.**

One touch to unlock your screen, authorize sudo, sign SSH commits, and gate the commands your AI agent runs on your behalf.

immurok is an open-source hardware security key with a built-in fingerprint sensor. It brings biometric authentication to every Mac and Linux machine — desktops, clamshell laptops, and headless servers — and to AI coding agents, all over Bluetooth LE.

## Features

- **Screen unlock** — Touch to unlock macOS lock screen and Linux login
- **sudo / polkit** — Fingerprint replaces password for privilege escalation
- **SSH agent** — On-device ECDSA key generation and signing (private key never leaves the device)
- **TOTP** — Hardware-backed one-time passwords with Quick Fill
- **AI agent authorization** — Wrap an agent's subprocess with `imk run --agent --`. One fingerprint touch authorizes sudo + SSH signing + secret reads for the entire wrapped command; reject it and the subprocess gets `SIGTERM`.
- **Mutual authentication** — ECDH P-256 pairing + HMAC-SHA256 signed notifications

## Repositories

| Repository | Description |
|------------|-------------|
| [immurok](https://github.com/immurok/immurok) | Project overview, BLE protocol spec, and security whitepaper |
| [firmware](https://github.com/immurok/firmware) | CH592F main application firmware |
| [ota](https://github.com/immurok/ota) | OTA bootloader and firmware update tools |
| [app-macos](https://github.com/immurok/app-macos) | macOS companion app (Swift) |
| [app-linux-rs](https://github.com/immurok/app-linux-rs) | Linux companion app — daemon + CLI (Rust) |
| [imk-skill](https://github.com/immurok/imk-skill) | AI-agent skill — how Claude Code / Cursor / Codex / Cline / Gemini CLI use `imk run --agent` to gate privileged commands |
| [hardware](https://github.com/immurok/hardware) | Hardware design, schematics, and component selection |

## License

All repositories are licensed under [BSL 1.1](https://github.com/immurok/immurok/blob/main/LICENSE) — personal, education, and research use permitted. Converts to Apache 2.0 on 2030-03-05.
