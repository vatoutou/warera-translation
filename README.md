# Traducciones de War Era

Este repositorio contiene los archivos de traducción para [War Era](https://app.warera.io). ¡Las traducciones de la comunidad son bienvenidas!

## Estructura

Cada locale tiene su propio directorio con un archivo `messages.po`:

```
en/messages.po   # Inglés (locale original)
es/messages.po   # Español
fr/messages.po   # Francés
it/messages.po   # Italiano
lv/messages.po   # Letón
pl/messages.po   # Polaco
pt/messages.po   # Portugués
ro/messages.po   # Rumano
sr/messages.po   # Serbio
tr/messages.po   # Turco
uk/messages.po   # Ucraniano
```

## Cómo contribuir

1. Haz un **Fork** de este repositorio.
2. **Edita** el archivo`.po` para el idioma al que quieres traducir.
3. **Envia una Pull Request.**


### Si quieres añadir un nuevo idioma

Para añadir un nuevo idioma, crea una carpeta y nombrala con el código **ISO 639-1** del idioma y agrega un archivo `messages.po` dentro.

Por ejemplo, para añadir **catalán** (código de idioma `ca` de acuerdo al estándar ISO 639-1):

1. Crea una nueva carpeta y nombrala `ca/`
2. Copia un archivo `messages.po` ya existente en ella (por ejemplo: `en/messages.po`)
3. Borra los valores `msgstr` y llénalos con tus traducciones al catalán.
4. Envía una Pull Request.

La estructura resultante debería verse así:

```
ca/messages.po   # Catalan
```

Puedes encontrar el código ISO 639-1 para tu idioma en [Wikipedia](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes).

### Editando archivos `.po`

Cada archivo`.po` contiene entradas así:

```po
#: src/components/SomeComponent.tsx:42
msgid "Hello, world!"
msgstr ""
```

- `msgid` es la string original en inglés (**no** modifiques esto)
- `msgstr` es la traducción — llena esto en tu idioma
- Las lineas que empiezan con `#:` son las referencias originales (no las modifiques)
- Las lineas que empiezan con `#.` son comentarios de desarrollador que proveen contexto

Un `msgstr ""` vacío significa que la string está sin traducir y quedará en inglés.

### Herramientas

Puedes editar archivos `.po` con:
- Cualquier editor de texto
- [Poedit](https://poedit.net/) — un editor de archivos `.po` dedicado con una buena IU
- [Weblate](https://weblate.org/) o herramientas online similares

### Placeholders

Algunas strings contienen placeholders como `{0}`, `{username}`, o etiquetas tipo XML `<0>...</0>`. Asegúrate de  **mantener todos los placeholders intactos** en tu traducción:

```po
msgid "Welcome, {0}!"
msgstr "Bienvenido, {0} !"
```

```po
msgid "Click <0>here</0> to continue"
msgstr "Clic <0>aquí</0> para continuar"
```

## Lineamientos

- No traduzcas el archivo `en/messages.po` (es el locale original, auto-generado)
- Mantén el tono consistente con el estilo del juego
- Si no estás seguro de una traducción, deja un comentario en tu PR

## Añadir un idioma nuevo

Si comienzas a traducir en un idioma, por favor abre un issue para que la gente sepa que estás trabajando en él.

## Licencia

Estos archivos de traducción son parte del proyecto War Era.
