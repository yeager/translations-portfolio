# po-translate – del av översättningsverktygslådan

po-translate fortsätter att vara mitt go-to-verktyg för att snabbt komma igång med nya översättningsprojekt.

## Översättningsverktygslådan

Jag har nu tre verktyg som kompletterar varandra:

| Verktyg | Funktion |
|---------|----------|
| **po-translate** | Batch-översätt .po/.ts-filer med AI eller gratis tjänster |
| **l10n-lint** | Hitta fel i översättningsfiler (placeholders, fuzzy, etc.) |
| **tp-lint** | Granska Translation Project-översättningar + statistik |

## Typiskt arbetsflöde

```bash
# 1. Översätt automatiskt som startpunkt
po-translate --service lingva --source en --target sv ./po/

# 2. Granska och rätta manuellt i Poedit/Lokalize

# 3. Kör lint för att hitta kvarvarande problem
l10n-lint ./po/sv.po

# 4. Fixa och upprepa tills allt är grönt!
```

## 10 översättningstjänster

### Gratis (ingen API-nyckel krävs)
- **Lingva** – Google Translate-proxy utan spårning
- **MyMemory** – 1000 ord/dag gratis, översättningsminne
- **LibreTranslate** – Öppen källkod, kan självhostas

### Betalda (högre kvalitet)
- **DeepL / DeepL Free** – Bäst för europeiska språk
- **Google Cloud Translation** – Snabb och pålitlig
- **OpenAI** – GPT-4, kontextmedveten, förstår teknisk terminologi
- **Anthropic** – Claude, bra på nyanser och formellt språk

## Smarta funktioner

- **Bevarar placeholders** – {0}, %s, %d, %(name)s hålls intakta
- **Fuzzy-markering** – Maskinöversättningar markeras som fuzzy
- **Batch-API** – Effektiv användning av API-kvoter
- **Dry-run** – Förhandsgranska utan att spara
- **Stöd för .po och .ts** – gettext och Qt Linguist

## Installation

```bash
# Debian/Ubuntu
sudo dpkg -i po-translate_1.0.0_all.deb

# Från PyPI
pip install po-translate
```

## Källkod

🔗 **GitHub:** [github.com/yeager/po-translate](https://github.com/yeager/po-translate)

---

*Se hela min [översättningsportfolio](https://yeager.github.io/translations-portfolio/) med 150+ projekt, 30+ emulatorer och 20 års översättningsarbete!*
