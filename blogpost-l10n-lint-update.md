# l10n-lint v1.3.0 – Förbättrad hantering av pluralformer och längdkontroll

Ny version av l10n-lint är ute med viktiga buggfixar och förbättringar!

## Vad är nytt i v1.3.0?

### 🔧 Fixad pluralformshantering

Tidigare kunde parsern missa pluralformer i .po-filer. Nu kontrolleras `msgid_plural` korrekt innan `msgid`, vilket löser problem med strängar som:

```
msgid "Delete %d file"
msgid_plural "Delete %d files"
msgstr[0] "Ta bort %d fil"
msgstr[1] "Ta bort %d filer"
```

### 📏 Förbättrad längdkontroll

**length-ratio höjt till 3x:** Svenska sammansatta ord som "Förhandsgranskning" (Preview) är mycket längre än engelska originalet. Tidigare gav detta falsklarm – nu tillåts upp till 3x längd.

**too-long jämför med källan:** Regeln varnar nu endast om översättningen är >1.5x längre än originalet OCH >500 tecken. Korta strängar ger inte längre falsklarm.

### 🌍 45 språk

Verktyget finns nu översatt till 45 språk, inklusive alla stora europeiska språk samt kinesiska, japanska, koreanska, arabiska med flera.

## Installation

```bash
# Debian/Ubuntu
sudo dpkg -i l10n-lint_1.3.0_all.deb

# Fedora/RHEL  
sudo rpm -i l10n-lint-1.3.0-1.noarch.rpm

# Arch Linux
sudo pacman -U l10n-lint-1.3.0-1-any.pkg.tar.xz

# Från källkod
pip install l10n-lint
```

## Ladda ner

🔗 **GitHub Release:** [github.com/yeager/l10n-lint/releases/tag/v1.3.0](https://github.com/yeager/l10n-lint/releases/tag/v1.3.0)

📦 **Paket:** .deb (all), .rpm (noarch), .pkg.tar.xz (Arch), .tar.gz

---

*l10n-lint är en del av min översättningsverktygslåda tillsammans med [tp-lint](https://github.com/yeager/tp-lint) och [po-translate](https://github.com/yeager/po-translate). Se hela min [översättningsportfolio](https://yeager.github.io/translations-portfolio/).*
