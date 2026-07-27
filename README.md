<div align="center">

**English** · [Русский](README.ru.md)

<img src="docs/assets/icon.png" width="128" alt="Alter logo" />

# Alter

**A modern Android modding toolkit for regex management, Smali dialog generation, runtime dumper injection, and string obfuscation, all in one place.**

<br/>

![Platform](https://img.shields.io/badge/platform-Android-CA8C6E?style=for-the-badge&logo=android&logoColor=white)
![Min SDK](https://img.shields.io/badge/Android-7.0%2B-324154?style=for-the-badge)
![Language](https://img.shields.io/badge/built%20with-Java-324154?style=for-the-badge&logo=openjdk&logoColor=white)
![Root](https://img.shields.io/badge/root-not%20required-CA8C6E?style=for-the-badge)

[![Version](https://img.shields.io/badge/release-2026.07.24-CA8C6E?style=flat-square)](https://github.com/Ivanparfenchuk/Alter/releases/latest)
[![Download](https://img.shields.io/badge/download-APK-5B9BD5?style=flat-square&logo=android&logoColor=white)](https://github.com/Ivanparfenchuk/Alter/releases/latest)
[![Telegram](https://img.shields.io/badge/Telegram-AlterProject-229ED9?style=flat-square&logo=telegram&logoColor=white)](https://t.me/AlterProject)
[![License](https://img.shields.io/badge/license-Proprietary-324154?style=flat-square)](LICENSE)

</div>

<br/>

<div align="center">
  <img src="docs/assets/screenshots/home.jpg" width="19%" alt="Home" />
  <img src="docs/assets/screenshots/regex.jpg" width="19%" alt="Regex manager" />
  <img src="docs/assets/screenshots/dialog-builder.jpg" width="19%" alt="Dialog builder" />
  <img src="docs/assets/screenshots/dex-dumper.jpg" width="19%" alt="Dex dumper" />
  <img src="docs/assets/screenshots/lsparanoid.jpg" width="19%" alt="LSParanoid" />
</div>

---

## Overview

Alter is an all-in-one Android app for reverse engineers and modders. It brings together the tasks you normally juggle across several tools: keeping a searchable library of your regular expressions, generating ready-to-paste Smali for alert dialogs, dropping runtime dump libraries into an APK, and obfuscating string literals, all inside a single, minimal interface. It runs on **Android 7.0+**, is written in **Java**, and requires **no root**.

## Features

### Regex Manager

A dedicated workspace for the regular expressions you rely on while modding. Instead of keeping patterns in scattered notes, Alter gives you an organized, searchable library you can carry between devices.

- **Add your own patterns:** build your library your way. Alter is not a fixed list; it is a place for the patterns *you* collect and refine.
- **Folders:** organize your collection into named folders by purpose (remove ads, anti-analytics, safety, freemium, and so on).
- **Search that waits for you:** the search runs when you submit your query, so the list is not rebuilt on every keystroke.
- **Portable backup and import:** export your entire collection as a `.zip` of `JSON` files and restore it on any device.

> Unlike tools that only let you use a fixed, read-only set of pre-approved patterns, Alter lets you add your own regexes, organize them, and carry them anywhere.

See [docs/features/regex-manager.md](docs/features/regex-manager.md).

### Alert Dialog Generator

Generate ready-to-use **Smali** code for alert dialogs in several visual styles: Rounded, Material 3, iOS, iOS Dark, and Expiration, straight from a form. Fill in the title, message, buttons and link, preview it, and copy the output into your project.

- Multiple dialog styles out of the box.
- Built-in **tamper-protection logic**: generated dialogs verify their own state so they can't be silently bypassed by editing the app's `SharedPreferences`.

See [docs/features/alert-dialogs.md](docs/features/alert-dialogs.md).

### Native Dumper Injection

Inject powerful runtime analysis libraries into an APK in a single tap, with no manual `smali` edits and no build setup.

- **il2cpp dumper:** dumps IL2CPP classes, methods and fields from a running Unity app.
- **dex dumper:** extracts DEX files from a running app's memory.
- Options for **32-bit** targets and re-**signing** the patched APK.

See [docs/features/dumpers.md](docs/features/dumpers.md).

### LSParanoid Port

An on-device port of **LSParanoid** that obfuscates `const-string` literals inside your DEX classes, making static analysis of your strings significantly harder. Point it at an APK, describe which classes to obfuscate, and continue.

See [docs/features/lsparanoid.md](docs/features/lsparanoid.md).

## Installation

**Requirements:** Android 7.0 (API 24) or newer. No root required.

1. Open the [**Releases**](https://github.com/Ivanparfenchuk/Alter/releases/latest) page.
2. Download the latest `Alter.apk`.
3. Install it (you may need to allow installation from your browser or file manager).

Latest build is always available at this permanent link:

```
https://github.com/Ivanparfenchuk/Alter/releases/latest/download/Alter.apk
```

Releases are also posted on the project's Telegram channel: [t.me/AlterProject](https://t.me/AlterProject).

Full step-by-step guide: [docs/INSTALLATION.md](docs/INSTALLATION.md).

## Permissions

Alter requests only what it needs to read and write APK files and manage your regex backups. Every permission and the reason for it is documented in [docs/PERMISSIONS.md](docs/PERMISSIONS.md).

## Built With

Alter bundles the following open-source components. Full attributions and license texts live in [docs/CREDITS.md](docs/CREDITS.md) and [docs/THIRD_PARTY_LICENSES.md](docs/THIRD_PARTY_LICENSES.md).

| Component | Author | License |
| --- | --- | --- |
| [il2cppdumper](https://github.com/muhammadrizwan87/il2cppdumper) | MuhammadRizwan | MIT |
| [dexdumper](https://github.com/muhammadrizwan87/dexdumper) | MuhammadRizwan | MIT |
| [LSParanoid](https://github.com/LSPosed/LSParanoid) | LSPosed / Michael Rozumyanskiy | Apache-2.0 |

## License

Alter is **proprietary software**. See [LICENSE](LICENSE).

Files **generated by** Alter are covered by the separate, permissive [Alter Generated Content License](LICENSE-GENERATED-CONTENT.txt): you may use them freely in personal and commercial projects, with attribution required when redistributing generated content as part of a library or template pack.

Bundled third-party components remain under their own licenses.

## Links

- **Project channel:** [t.me/AlterProject](https://t.me/AlterProject)
- **Developer:** AvoluxModz ([t.me/AvoluxModz](https://t.me/AvoluxModz))

## Disclaimer

Alter is intended for security research, education, and modifying applications you own or are authorized to modify. You are solely responsible for how you use it and for complying with all applicable laws and any third-party terms of service. See [SECURITY.md](SECURITY.md) for details and for reporting issues.

<div align="center">
<br/>
<sub>© 2026 Alter · Developed by AvoluxModz</sub>
</div>
