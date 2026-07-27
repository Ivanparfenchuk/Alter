**English** · [Русский](../ru/features/regex-manager.md)

# Regex Manager

A dedicated workspace for the regular expressions you use while modding. Instead
of keeping patterns in scattered notes, Alter gives you an organized, searchable
library you can carry between devices.

## Why Alter exists

Alter started from a frustration with existing regex tools in the modding space.
Those tools ship a fixed, read-only set of pre-approved patterns and give the
user no way to add their own, so the real problem is never solved: your own
patterns still end up scattered and disorganized. Alter is the answer to that.
Your regexes are yours. You add them, you organize them, and you take them with
you.

## What it does

- **Add your own patterns.** Store as many patterns as you like, each with a
  name and a search/replace pair. There is no approved list and no gatekeeping;
  the library is yours to build.
- **Group into folders.** Organize patterns into named folders by purpose, for
  example `remove ads`, `anti analytics`, `safety`, or `freemium`. Folders show
  up as filter chips at the top of the Regex tab.
- **Search on submit.** Type your query and confirm it to run the search. The
  list is not rebuilt on every keystroke, so scrolling and typing stay smooth on
  large collections.
- **Copy in one tap.** Copy either side of a pattern (search or replace) to the
  clipboard instantly.

## Backup and import

Your whole collection can be exported and restored as a portable archive.

- **Format:** a `.zip` archive containing plain `JSON` files plus one signature
  file. The archive is left readable so other tools can open it.

Inside the archive:

| File | Purpose |
| --- | --- |
| `folders_meta.json` | The index. A `JSON` array describing every folder in the collection: how many there are, and each folder's `id` and `name`. |
| `regex_folder_<id>.json` | One file per folder, named after that folder's `id`. A `JSON` array of the folder's patterns. |
| `backup.sig` | The archive's signature (a hash of its contents). Alter uses it to verify integrity on import. |

### File shapes

`folders_meta.json`:

```json
[
  { "id": "1784926869621_0", "name": "remove ads" },
  { "id": "1784926869624_1", "name": "anti analytics" }
]
```

`regex_folder_<id>.json`:

```json
[
  { "name": "pattern name", "search": "<search value>", "replace": "<replace value>" }
]
```

### The signature file

`backup.sig` holds a signature hash of the archive's contents. The point is to
keep the `.zip` structure plain and openable by other tools, while still letting
Alter confirm the archive has not been altered outside the app. On import, Alter
recomputes the signature and compares it with `backup.sig`. If an archive was
edited outside Alter, the signature will not match and Alter refuses to import
it, which keeps broken or malformed collections from being loaded.

To back up or import, use the backup/restore control on the Regex tab.

## Why it's different

Two capabilities set Alter apart, and one principle ties them together:

1. **You can add your own patterns.** Alter is a home for the patterns you
   collect, not a locked list of someone else's approved ones.
2. **Folder organization.** Arrange your collection into named folders rather
   than one flat pile.
3. **Manual backup and import.** Full control over exporting and restoring your
   collection as a portable, shareable archive.
