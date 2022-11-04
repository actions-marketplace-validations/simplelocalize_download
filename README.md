# Download localization files

This Github Action uses [official SimpleLocalize CLI](https://github.com/simplelocalize/simplelocalize-cli).

Learn more: https://simplelocalize.io/docs/integrations/github-actions/

## Usage

```yml
name: 'My project'
on:
  push:
    branches: [ main, master ]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Download translations
        uses: simplelocalize/download@v2.1
        with:
          apiKey: <YOUR_API_KEY>
          downloadPath: ./{lang}/translations.json
          downloadFormat: single-language-json
          downloadOptions: "ESCAPE_NEW_LINES" # optional
          languageKey: en # optional, it accepts only one language key
          customerId: ikea # optional, it accepts only one customer id
```
