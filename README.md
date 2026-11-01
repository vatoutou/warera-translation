# War Era Translations

This repository contains the community translation files for [War Era](https://app.warera.io).

Contributions are welcome! You can help improve an existing translation, fix mistakes, or contribute a new language. Please read the guidelines below before submitting a Pull Request.

## Repository Structure

Each language has its own directory containing a `messages.po` file.

```text
en/messages.po   # English (source locale)
es/messages.po   # Spanish
fr/messages.po   # French
it/messages.po   # Italian
lv/messages.po   # Latvian
pl/messages.po   # Polish
pt/messages.po   # Portuguese
ro/messages.po   # Romanian
sr/messages.po   # Serbian
tr/messages.po   # Turkish
uk/messages.po   # Ukrainian
nl/messages.po   # Dutch
```

## How to Contribute

To improve an existing translation:

1. **Fork** this repository.
2. Open the directory for the language you want to translate.
3. Edit its `messages.po` file, following the guidelines below.
4. Review your changes to ensure you haven't modified source strings, placeholders, or file formatting.
5. Submit a Pull Request describing your changes.

Please keep translation changes limited to the language you're working on.

## Translation Guidelines

### 1. Only Translate `msgstr`

Each translation entry contains an original string (`msgid`) and its translation (`msgstr`).

```po
#: src/components/SomeComponent.tsx:42
msgid "Hello, world!"
msgstr "¡Hola, mundo!"
```

- **`msgid`** — The original source string. **Never modify it.**
- **`msgstr`** — The translated string. This is where your translation belongs.
- `#:` — Source-code references indicating where the string is used.
- `#.` — Developer comments that may provide useful translation context.

For translation contributions, edit the `msgstr` values only. Do not rewrite, delete, or reformat source strings, comments, references, flags, or other PO metadata.

If a string is already translated, improve its `msgstr` only when necessary.

### 2. Preserve Placeholders and Formatting

Some strings contain placeholders, tags, or formatting instructions that the game needs to display text correctly.

Common examples include:

| Type | Example |
| --- | --- |
| Numbered placeholder | `{0}`, `{1}` |
| Named placeholder | `{username}`, `{count}` |
| Component tag | `<0>...</0>` |
| Special variable | `{MIN_REGISTRATIONS}` |
| ICU plural | `{count, plural, one {...} other {...}}` |

**Preserve every placeholder and structural tag exactly as required by the source string.**

For example:

```po
msgid "Welcome, {0}!"
msgstr "¡Bienvenido, {0}!"
```

```po
msgid "Click <0>here</0> to continue"
msgstr "Haz clic <0>aquí</0> para continuar"
```

You may translate the text around placeholders, but do not rename variables, remove tags, change their order when it affects meaning, or break their opening and closing structure.

Pay particular attention to:

- Missing or altered placeholders.
- Unmatched or incorrectly nested tags.
- ICU plural expressions and their required branches.
- Escaped characters, quotation marks, and multiline strings.
- Formatting flags and special syntax required by the source.

A translation can sound correct while still breaking the game if its placeholders or formatting are damaged.

### 3. Handle Plural Entries Correctly

Plural entries must retain their original structure and use the correct plural forms for the target language.

Do not replace plural entries with a single translation or remove required plural branches. The number and meaning of plural forms depend on the language and the entry's format.

### 4. Translate Naturally and Accurately

Translations should communicate the same meaning as the original while sounding natural in the target language.

- Keep terminology consistent throughout the game.
- Preserve the original meaning, tone, and context.
- Use developer comments and source references to understand ambiguous strings.
- Avoid literal translations that sound unnatural or change the intended meaning.
- Do not add advertisements, personal contact information, or unrelated content to translations.
- Do not insert comments or messages intended for players unless they are part of the original text.

If you're unsure about a string, check its context or ask for clarification in your Pull Request or in WarEra discord

### 5. Leave Untranslated Strings Empty

An empty `msgstr` indicates that a string has not yet been translated.

```po
msgid "New feature"
msgstr ""
```

If you cannot translate a string confidently, it is better to leave it untranslated than to submit an incorrect or misleading translation.

Do not fill missing translations with guesses or unrelated text.

## Adding a New Language

If you want to contribute a language that does not yet have its own directory, please open an issue first to let others know you're working on it.

To add a new language:

1. Create a directory using the language's **ISO 639-1 code**, where applicable.
2. Copy an existing `messages.po` file, such as `en/messages.po`, into the new directory.
3. Keep the original `msgid` values and PO structure unchanged.
4. Translate the `msgstr` values into your language.
5. Preserve placeholders, plural structures, and formatting.
6. Submit a Pull Request.

For example, to add Catalan:

```text
ca/messages.po
```

You can find language codes in the [ISO 639-1 list](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes).

Do not translate `en/messages.po`. It is the source locale and is maintained separately from community translations.

## Recommended Tools

You can edit `.po` files using:

- **Any text editor**.
- **Weblate** — or similar online tools.

Regardless of the tool you use, review the final diff before submitting your Pull Request. Translation editors can sometimes modify metadata or formatting beyond the strings you intended to change.

## Before Submitting a Pull Request

Please check that:

- [ ] Only the intended language's `msgstr` values have been changed.
- [ ] No `msgid` values or source strings have been modified.
- [ ] Placeholders and component tags are preserved.
- [ ] Plural entries and their required branches remain intact.
- [ ] PO syntax, quotation marks, and multiline strings are valid.
- [ ] Translations are accurate, natural, and consistent.
- [ ] No unrelated content, advertisements, or personal contact information has been added.
- [ ] The diff contains no accidental changes to comments, references, or metadata.

Small, focused Pull Requests are easier to review and merge.

## License

These translation files are part of the War Era project.
