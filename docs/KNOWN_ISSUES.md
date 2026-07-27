**English** · [Русский](ru/KNOWN_ISSUES.md)

# Known Issues

This page tracks known limitations and rough edges. If you hit something that
isn't listed, please open a
[bug report](https://github.com/Ivanparfenchuk/Alter/issues/new/choose).

## Current

- _Nothing tracked yet for this release._

## Notes & limitations

- **Storage access:** on Android 11+, patching APKs requires "All files access"
  (`MANAGE_EXTERNAL_STORAGE`). If file selection or saving fails, confirm the
  permission is granted (see [PERMISSIONS.md](PERMISSIONS.md)).
- **Protected / packed targets:** some apps use protections that can interfere
  with dumping or patching. Results vary by target; see the upstream dumper
  projects for details on what they can and cannot handle.
- **Signing:** if a patched APK won't install, make sure the **Sign** option was
  enabled and that any previous copy of the app is uninstalled first
  (signature mismatch).

## Template for reporting

When reporting an issue, please include:

- Alter version (e.g. `2026.07.24`)
- Device model and Android version
- The tool you used (Regex / Dialog / il2cpp dumper / dex dumper / LSParanoid)
- Exact steps to reproduce
- What you expected vs. what happened
