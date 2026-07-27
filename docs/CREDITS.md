**English** · [Русский](ru/CREDITS.md)

# Credits

Alter stands on the work of several open-source projects. Huge thanks to their
authors and maintainers. Each component remains the property of its respective
author and is used under its own license. Full license texts are collected in
[THIRD_PARTY_LICENSES.md](THIRD_PARTY_LICENSES.md).

## Bundled components

### il2cppdumper
- **Author:** MuhammadRizwan ([@muhammadrizwan87](https://github.com/muhammadrizwan87))
- **Repository:** https://github.com/muhammadrizwan87/il2cppdumper
- **License:** MIT
- **Role in Alter:** native runtime library injected by the *il2cpp dumper* tool
  to dump IL2CPP classes, methods and fields from a running Unity app.
- Built on the foundation of [Zygisk-Il2CppDumper](https://github.com/Perfare/Zygisk-Il2CppDumper) by Perfare.

### dexdumper
- **Author:** MuhammadRizwan ([@muhammadrizwan87](https://github.com/muhammadrizwan87))
- **Repository:** https://github.com/muhammadrizwan87/dexdumper
- **License:** MIT
- **Role in Alter:** native runtime library injected by the *dex dumper* tool to
  extract DEX files from a running app's memory.

### LSParanoid
- **Authors:** LSPosed and Michael Rozumyanskiy
- **Repository:** https://github.com/LSPosed/LSParanoid
- **License:** Apache License 2.0
- **Role in Alter:** basis for the *LSParanoid* string-obfuscation tool that
  obfuscates `const-string` literals inside DEX classes.
- Forked from [MichaelRocks/paranoid](https://github.com/MichaelRocks/paranoid).

## Thank you

If you maintain one of the projects above and would like an attribution
adjusted, please reach out via [t.me/AvoluxModz](https://t.me/AvoluxModz).
