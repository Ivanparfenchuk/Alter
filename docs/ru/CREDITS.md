[English](../CREDITS.md) · **Русский**

# Благодарности

Alter опирается на работу нескольких open-source проектов. Огромная благодарность
их авторам и мейнтейнерам. Каждый компонент остаётся собственностью своего автора
и используется по его лицензии. Полные тексты лицензий собраны в
[THIRD_PARTY_LICENSES.md](THIRD_PARTY_LICENSES.md).

## Встроенные компоненты

### il2cppdumper
- **Автор:** MuhammadRizwan ([@muhammadrizwan87](https://github.com/muhammadrizwan87))
- **Репозиторий:** https://github.com/muhammadrizwan87/il2cppdumper
- **Лицензия:** MIT
- **Роль в Alter:** нативная библиотека, внедряемая инструментом *il2cpp dumper*
  для дампа классов, методов и полей IL2CPP из запущенного Unity-приложения.
- Построено на основе [Zygisk-Il2CppDumper](https://github.com/Perfare/Zygisk-Il2CppDumper) от Perfare.

### dexdumper
- **Автор:** MuhammadRizwan ([@muhammadrizwan87](https://github.com/muhammadrizwan87))
- **Репозиторий:** https://github.com/muhammadrizwan87/dexdumper
- **Лицензия:** MIT
- **Роль в Alter:** нативная библиотека, внедряемая инструментом *dex dumper* для
  извлечения DEX-файлов из памяти запущенного приложения.

### LSParanoid
- **Авторы:** LSPosed и Michael Rozumyanskiy
- **Репозиторий:** https://github.com/LSPosed/LSParanoid
- **Лицензия:** Apache License 2.0
- **Роль в Alter:** основа инструмента *LSParanoid*, обфусцирующего литералы
  `const-string` внутри DEX-классов.
- Форкнут от [MichaelRocks/paranoid](https://github.com/MichaelRocks/paranoid).

## Спасибо

Если вы поддерживаете один из проектов выше и хотите скорректировать атрибуцию,
напишите в [t.me/AvoluxModz](https://t.me/AvoluxModz).
