**English** · [Русский](ru/PERMISSIONS.md)

# Permissions

Alter requests a small set of permissions, all tied to reading and writing APK
files and managing your regex backups. It does not collect analytics or send
your data anywhere.

| Permission | Manifest name | Why Alter needs it |
| --- | --- | --- |
| Read shared storage | `android.permission.READ_EXTERNAL_STORAGE` | Read APK files you select and import regex-collection backups. |
| Manage all files | `android.permission.MANAGE_EXTERNAL_STORAGE` | Access APKs anywhere on the device so you can pick and patch files outside the app's scoped directory. |
| Write shared storage | `android.permission.WRITE_EXTERNAL_STORAGE` | Save patched APKs, generated files, and regex backups. |
| Vibrate | `android.permission.VIBRATE` | Haptic feedback for actions in the UI. |
| Internet | `android.permission.INTERNET` | Check for updates and download the latest release. |
| Network state | `android.permission.ACCESS_NETWORK_STATE` | Detect whether the device is online before attempting network operations. |

## Notes

- **Storage access on Android 11+.** Because Alter patches arbitrary APK files
  chosen by the user, it uses "All files access" (`MANAGE_EXTERNAL_STORAGE`).
  You can grant it from **Settings → Apps → Alter → Permissions**.
- **`READ_/WRITE_EXTERNAL_STORAGE`** are the legacy storage permissions and
  apply mainly to Android 10 and below.
- Alter uses the internet only for update checks and downloads, nothing else.
