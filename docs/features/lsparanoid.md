**English** · [Русский](../ru/features/lsparanoid.md)

# LSParanoid Port

An on-device port of **LSParanoid** that obfuscates `const-string` literals
inside your DEX classes, making static analysis of your strings harder.

- Based on [LSPosed/LSParanoid](https://github.com/LSPosed/LSParanoid) (Apache-2.0),
  itself forked from [MichaelRocks/paranoid](https://github.com/MichaelRocks/paranoid).

## How to use

1. Open **LSParanoid** from the Home tab.
2. Tap **Select APK file** and pick your target.
3. In **Class obfuscation configuration**, describe which classes to obfuscate.
   The configuration uses one rule per line, for example:

   ```
   alter.Main.*
   !com.BuildConfig
   alter.MainActivity;onCreate\(.*
   ```

   - A plain pattern includes matching classes/members.
   - A leading `!` excludes a pattern.
4. Optionally enable **Sign** to re-sign the output.
5. Tap **Continue** to produce the obfuscated APK.

## Notes

- Obfuscation replaces readable string constants with calls to a deobfuscator, so
  the strings are no longer visible in a static dump.
- It does not encrypt code or prevent runtime inspection; it raises the bar for
  static analysis of strings only.
