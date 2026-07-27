**English** · [Русский](../ru/features/dumpers.md)

# Native Dumper Injection

Inject runtime analysis libraries into an APK in a single tap. Alter handles the
Smali loader and library placement for you, with no manual patching and no build setup.

## Tools

### il2cpp dumper
Injects a native library that dumps IL2CPP metadata (classes, methods, fields)
from a **running** Unity app, entirely inside the app's own process. Useful for
inspecting Unity/IL2CPP builds.

- Based on [muhammadrizwan87/il2cppdumper](https://github.com/muhammadrizwan87/il2cppdumper) (MIT).

### dex dumper
Injects a native library that extracts DEX files from a running app's memory,
handy for recovering DEX from packed or protected apps.

- Based on [muhammadrizwan87/dexdumper](https://github.com/muhammadrizwan87/dexdumper) (MIT).

## Options

- **Select APK file**: choose the target APK.
- **32-bit**: toggle when the target runs as a 32-bit process, so the matching
  native libraries are injected.
- **Sign**: re-sign the patched APK so it can be installed.

## How to use

1. Open **Dex dumper** or **il2cpp dumper** from the Home tab.
2. Tap **Select APK file** and pick your target.
3. Set **32-bit** / **Sign** as needed.
4. Tap **Inject dumper**.
5. Install and run the patched app; the dump is written to the app's files
   directory (see each upstream project for exact output paths).

> These libraries operate inside the target app's own sandbox. Use them only on
> apps you own or are authorized to analyze.
