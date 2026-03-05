# immurok

**Wireless fingerprint authenticator for Mac and Linux.**

One touch to unlock your screen, authorize sudo, sign SSH commits, and more.

immurok is an open-source hardware security key with a built-in fingerprint sensor. It brings biometric authentication to every Mac and Linux machine — desktops, clamshell laptops, and headless servers — over Bluetooth LE.

## Features

- **Screen unlock** — Touch to unlock macOS lock screen and Linux login
- **sudo / polkit** — Fingerprint replaces password for privilege escalation
- **SSH agent** — On-device ECDSA key generation and signing (private key never leaves the device)
- **TOTP** — Hardware-backed one-time passwords with Quick Fill
- **Mutual authentication** — ECDH P-256 pairing + HMAC-SHA256 signed notifications

## Repositories

| Repository | Description |
|------------|-------------|
| [immurok](https://github.com/immurok/immurok) | Project overview, BLE protocol spec, and security whitepaper |
| [firmware](https://github.com/immurok/firmware) | CH592F main application firmware |
| [ota](https://github.com/immurok/ota) | OTA bootloader and firmware update tools |
| [app-macos](https://github.com/immurok/app-macos) | macOS companion app (Swift) |
| [app-linux](https://github.com/immurok/app-linux) | Linux companion app (Python) |
| [hardware](https://github.com/immurok/hardware) | Hardware design, schematics, and component selection |

## License

All repositories are licensed under [BSL 1.1](https://github.com/immurok/immurok/blob/main/LICENSE) — personal, education, and research use permitted. Converts to Apache 2.0 on 2030-03-05.
