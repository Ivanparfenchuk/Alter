**English** · [Русский](ru/RELEASING.md)

# Releasing & Auto-Update

This guide is for the maintainer. It explains how to publish a release so users
get a stable, permanent download link that also powers the in-app updater.

## 1. Naming

Alter uses date-based versions: `YYYY.MM.DD` with a build number.

- **Tag:** `v2026.07.24`
- **Release title:** `Alter 2026.07.24 (build 10)`
- **APK asset name:** keep it **exactly** `Alter.apk` on every release, since the
  permanent link below depends on this name never changing.

## 2. Publish a release

1. Go to **Releases → Draft a new release**.
2. **Choose a tag** → type the new tag (e.g. `v2026.07.24`) → *Create new tag on
   publish*.
3. Set the **title** and paste your notes (use `.github/RELEASE_TEMPLATE.md`).
4. **Attach** the `Alter.apk` build as a binary asset.
5. Leave **"Set as the latest release"** checked.
6. **Publish release.**

> Binaries live in Releases, not in the repository tree. Do not commit the APK
> into the repo.

## 3. Permanent download link

Because the asset is always named `Alter.apk` and the release is marked latest,
this URL always resolves to the newest APK:

```
https://github.com/Ivanparfenchuk/Alter/releases/latest/download/Alter.apk
```

Use it for the website button, Telegram, and the in-app "Download update" action.

## 4. In-app update check

To check for updates from inside the app, read the GitHub Releases API and
compare the tag with the installed version:

```
GET https://api.github.com/repos/Ivanparfenchuk/Alter/releases/latest
```

Relevant fields in the JSON response:

- `tag_name`: the latest version (e.g. `v2026.07.24`). Compare with the
  installed version to decide whether to prompt.
- `body`: the release notes to show in an update dialog.
- `assets[].browser_download_url`: direct download URL for the attached APK
  (equivalent to the permanent link above).

Suggested flow:

1. `GET` the endpoint above.
2. If `tag_name` is newer than the installed version, show an update prompt with
   `body` as the changelog.
3. On confirm, download from the permanent `releases/latest/download/Alter.apk`
   link and launch the installer.

> The unauthenticated GitHub API allows a limited number of requests per hour per
> IP. Check on app start or on demand rather than polling frequently.
