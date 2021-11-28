# Download translation files from SimpleLocalize i18n editor

This Github Actions uses official and open-source SimpleLocalize CLI.

Learn more: https://github.com/simplelocalize/simplelocalize-cli

Documentation: https://simplelocalize.io/docs/cli/download-translations/

## ☁️ Example download action

```yml
name: 'Download translations'
on:
  push:
    branches: [ main ]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Download translations
        uses: simplelocalize/download@latest
        with:
          apiKey: <YOUR_API_KEY>
          downloadPath: ./output-sample.json
          downloadFormat: multi-language-json
```
