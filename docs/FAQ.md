**English** · [Русский](ru/FAQ.md)

# FAQ

### What is Alter?
An all-in-one Android modding toolkit: a regex manager, a Smali alert-dialog
generator, one-tap injection of the il2cpp and dex dumper libraries, and an
LSParanoid string-obfuscation port.

### Does it require root?
No. Alter works on non-rooted devices running Android 7.0+.

### What Android versions are supported?
Android 7.0 (API 24) and newer.

### Is Alter open source?
No. The application is proprietary (see [../LICENSE](../LICENSE)). It bundles a
few open-source components, credited in [CREDITS.md](CREDITS.md).

### Can I use files that Alter generates in my own projects?
Yes. Generated content (for example, generated Smali dialogs) is covered by the
permissive [Alter Generated Content License](../LICENSE-GENERATED-CONTENT.txt).
You can use it in personal and commercial projects; attribution is required only
when you redistribute generated content as part of a library or template pack.

### In what format are regex backups saved?
A `.zip` archive with an index file (`folders_meta.json`), one `JSON` file per
folder, and a signature file (`backup.sig`) that Alter verifies on import so
externally modified archives are rejected. Full details are in
[features/regex-manager.md](features/regex-manager.md).

### What does the "Secret cryptKey" field in the dialog builder do?
It powers the dialog's tamper-protection logic, which prevents the dialog from
being bypassed by editing the host app's `SharedPreferences`. See
[features/alert-dialogs.md](features/alert-dialogs.md).

### What is the "32-bit" option in the dumpers?
Enable it when the target app runs as a 32-bit process so the matching native
libraries are injected.

### What does "Sign" do?
It re-signs the patched APK so Android will install it.

### How do I get updates?
Use the in-app update check, download the latest build from the
[Releases](https://github.com/Ivanparfenchuk/Alter/releases/latest) page, or grab
it from the project's Telegram channel
[t.me/AlterProject](https://t.me/AlterProject), where releases are also posted.

### Where can I report a bug or ask for a feature?
Open an issue on GitHub, or reach the project on Telegram:
[t.me/AlterProject](https://t.me/AlterProject).
