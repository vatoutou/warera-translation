# War Era Translations

This repository contains the translation files for [War Era](https://app.warera.io). Community contributions are welcome!

## Structure

Each locale has its own directory with a `messages.po` file:

```
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

1. **Fork** this repository
2. **Edit** the `.po` file for the language you want to translate
3. **Submit a Pull Request**


### If you want to add a new language

To add a new language, create a folder named with the language's **ISO 639-1** code and add a `messages.po` file inside it.

For example, to add **Catalan** (language code `ca` according to the ISO 639-1 standard):

1. Create a new folder named `ca/`
2. Copy an existing `messages.po` file into it (e.g. from `en/messages.po`)
3. Clear all the `msgstr` values and fill in your Catalan translations
4. Submit a Pull Request

The resulting structure should look like:

```
ca/messages.po   # Catalan
```

You can find the ISO 639-1 code for your language on [Wikipedia](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes).

### Editing `.po` files

Each `.po` file contains entries like this:

```po
#: src/components/SomeComponent.tsx:42
msgid "Hello, world!"
msgstr ""
```

- `msgid` is the original English string (do **not** modify this)
- `msgstr` is the translation — fill this in for your language
- Lines starting with `#:` are source references (do not modify)
- Lines starting with `#.` are developer comments providing context

An empty `msgstr ""` means the string is untranslated and will fall back to English.

### Tools

You can edit `.po` files with:
- Any text editor
- [Poedit](https://poedit.net/) — a dedicated `.po` file editor with a nice UI
- [Weblate](https://weblate.org/) or similar online tools

### Placeholders

Some strings contain placeholders like `{0}`, `{username}`, or XML-like tags `<0>...</0>`. Make sure to **keep all placeholders intact** in your translation:

```po
msgid "Welcome, {0}!"
msgstr "Bienvenue, {0} !"
```

```po
msgid "Click <0>here</0> to continue"
msgstr "Cliquez <0>ici</0> pour continuer"
```

## Guidelines

- Do not translate the `en/messages.po` file (it is the source locale, auto-generated)
- Keep the tone consistent with the game's style
- If you're unsure about a translation, leave a comment on your PR

## Adding a New Language

If you start translating a language, please open an issue to let people know you're working on it.

## License

These translation files are part of the War Era project.
