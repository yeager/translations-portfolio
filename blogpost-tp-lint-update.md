# tp-lint v1.5.0 – Statistik och rapporter för Translation Project

Stor uppdatering av tp-lint med två nya funktioner: statistikläge och rapportgenerering!

## Nya funktioner i v1.5.0

### 📊 --stats: Translation Project-statistik

Hämta och analysera statistik direkt från Translation Projects matris:

```bash
# Statistik för svenska
tp-lint --stats sv

# Top 10 språk efter täckning
tp-lint --stats --top 10

# JSON-format för scripting
tp-lint --stats sv --format json
```

**Exempel på output:**

```
📊 Translation Project Statistics for Swedish (sv)

Coverage:        88% (131/148 packages translated)
Rank:            #1 of 85 active languages

Package Status:
  ✅ Complete:   98 packages
  🟡 Partial:    33 packages  
  ❌ Missing:    17 packages

Top packages by size:
  1. gcc              17086 strings (100%)
  2. util-linux-man    6964 strings (100%)
  3. gas               4952 strings (100%)
```

### 📝 --report: Generera rapporter

Skapa snygga rapporter i Markdown eller HTML:

```bash
# Markdown-rapport
tp-lint --report sv --output report.md

# HTML-rapport
tp-lint --report sv --format html --output report.html

# Inkludera lint-resultat
tp-lint --report sv --lint --output full-report.md
```

Rapporterna innehåller:
- Översikt med täckningsgrad och ranking
- Lista över alla paket med status
- Senaste uppdateringar
- Eventuella lint-fel (med --lint)

### 🌍 37 språk

Verktyget finns nu översatt till 37 språk.

## Användningsexempel

```bash
# Klassisk lint av svenska översättningar
tp-lint sv

# Granska specifika paket
tp-lint sv -p coreutils -p bash -p grep

# Fullständig rapport med lint
tp-lint --report sv --lint --format html -o swedish-report.html

# Jämför med andra språk
tp-lint --stats --top 20
```

## Installation

```bash
# Kräver l10n-lint
sudo dpkg -i l10n-lint_1.3.0_all.deb
sudo dpkg -i tp-lint_1.5.0_all.deb
```

## Ladda ner

🔗 **GitHub Release:** [github.com/yeager/tp-lint/releases/tag/v1.5.0](https://github.com/yeager/tp-lint/releases/tag/v1.5.0)

📦 **Paket:** .deb (all), .rpm (noarch), .pkg.tar.xz (Arch), .tar.gz

---

*tp-lint är en del av min översättningsverktygslåda. Se hela min [översättningsportfolio](https://yeager.github.io/translations-portfolio/) med 150+ projekt!*
