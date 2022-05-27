# Download localization files from SimpleLocalize

This Github Actions uses official and open-source SimpleLocalize CLI.

Learn more: https://github.com/simplelocalize/simplelocalize-cli

Documentation: https://simplelocalize.io/docs/cli/download-translations/

## ☁️ Example download action

```yml
name: 'Download translations'
on:
  push:
    branches: [ main, master ]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Download translations
        uses: simplelocalize/download@lastest
        with:
          apiKey: <YOUR_API_KEY>
          downloadPath: ./{lang}/translations.json
          downloadFormat: single-language-json
          downloadOptions: "ESCAPE_NEW_LINES" # optional
          languageKey: en # optional, it accepts only one language key
```
