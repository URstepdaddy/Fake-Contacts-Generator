# Fake-Contacts-Generator
Simple contacts creator, download, import to your phone, feed the machine wrong info.


```markdown
# 📇 Contact Generator

A fully client-side HTML tool to generate realistic random contacts — pick your countries, pick your fields, export to CSV or VCF. No server, no install, no dependencies. Just open the file.

---


## 📸 Preview

```
┌─────────────────────────────────────────────────────┐
│  ⚙️ Settings      [ 50 contacts ] [ +XX Intl ]  ⚡  │
├─────────────────────────────────────────────────────┤
│  🎛️ Fields    📱Minimal  👤Standard  📋Full         │
│  ✅ First Name 🔒  ☑ Last Name  ✅ Phone 🔒         │
│  ☐ Email  ☐ Gender  ✅ Country  ✅ Flag             │
├─────────────────────────────────────────────────────┤
│  🌍 Countries  [ Search... ]                        │
│  ── North Africa                                    │
│  🇹🇳 Tunisia  🇲🇦 Morocco  🇩🇿 Algeria  🇱🇾 Libya    │
│  ── Europe                                          │
│  🇫🇷 France  🇩🇪 Germany  🇬🇧 UK  🇪🇸 Spain ...     │
├─────────────────────────────────────────────────────┤
│  💾 [ 📄 CSV ]  [ 📱 VCF ]  [ 🗑️ Clear ]           │
└─────────────────────────────────────────────────────┘
```

---

## ✨ Features

### 🌍 30+ Countries across 7 regions
| Region | Countries |
|---|---|
| 🌵 North Africa | Tunisia, Morocco, Algeria, Libya, Egypt, Mauritania |
| 🏛️ Europe | France, Germany, UK, Spain, Italy, Portugal, Netherlands, Sweden, Poland |
| 🌏 Asia | China, Japan, South Korea, India, Indonesia, Pakistan |
| 🌎 Americas | USA, Canada, Brazil, Mexico, Argentina |
| 🕌 Middle East | Saudi Arabia |
| 🦘 Oceania | Australia |
| 🌍 Africa | Nigeria |

### 🎛️ Toggle Any Field
Choose exactly what data you want — nothing more, nothing less.

| Field | Locked | Default |
|---|---|---|
| First Name | 🔒 Always on | ✅ |
| Last Name | toggleable | ✅ |
| Phone | 🔒 Always on | ✅ |
| Email | toggleable | ❌ |
| Gender | toggleable | ❌ |
| Country | toggleable | ✅ |
| Flag | toggleable | ✅ |
| Dial Code | toggleable | ❌ |
| Country Code | toggleable | ❌ |

### ⚡ Presets
| Preset | Fields included |
|---|---|
| 📱 **Minimal** | First Name + Phone only |
| 👤 **Standard** | First Name, Last Name, Phone, Country, Flag |
| 📋 **Full** | Everything |

### 📤 Export Formats
- **CSV** — opens in Excel, Google Sheets, any spreadsheet tool. Only active fields are exported, clean plain text, no HTML artifacts.
- **VCF** — standard vCard 3.0 format. Import directly into iPhone Contacts, Android, Gmail, Outlook. Only active fields are written into the vCard.

---

## 🗂️ How It Works

```
User picks countries + fields + count
            │
            ▼
    Random country selected
    from chosen pool
            │
            ▼
    Gender randomly assigned
    → male or female name pool
            │
            ▼
    Name picked from country-specific
    database (50+ names per pool)
            │
            ▼
    Phone generated using
    country-accurate format
            │
            ▼
    Email built from name +
    country-local domain pool
            │
            ▼
    Rendered in table (live updates
    when you toggle fields)
            │
            ▼
    Export as CSV or VCF
```

---

## 🌐 Country Details

### Name Databases
Every country has its own curated name pools:
- **50+ male first names** per country
- **50+ female first names** per country  
- **40+ last names** per country

North African countries (Tunisia, Morocco, Algeria, Libya, Egypt, Mauritania) share a unified Arabic name pool since naming conventions are consistent across the MENA regions (i could be wrong, let me know if it's the case).

### Phone Number Formats
Each country generates numbers in its real-world format:

```
🇺🇸  +1 (555) 234-5678
🇬🇧  +44 7423 123 456
🇫🇷  +33 6 12 34 56 78
🇩🇪  +49 151 23456789
🇯🇵  +81 90-1234-5678
🇧🇷  +55 (11) 91234-5678
🇹🇳  +216 22 123 456
🇲🇦  +212 612-345-678
🇮🇳  +91 9812345678
🇨🇳  +86 138 1234 5678
```

### Email Domains
Emails are generated using country-aware domain pools:

| Country | Local domains used |
|---|---|
| 🇫🇷 France | orange.fr, laposte.net, free.fr, sfr.fr |
| 🇩🇪 Germany | web.de, gmx.de, t-online.de |
| 🇷🇺 Russia | mail.ru, yandex.ru, rambler.ru |
| 🇨🇳 China | qq.com, 163.com, 126.com, sina.com |
| 🇧🇷 Brazil | uol.com.br, bol.com.br, terra.com.br |
| 🇹🇳 Tunisia | topnet.tn, hexabyte.tn |
| 🇲🇦 Morocco | menara.ma, iam.ma |
| All others | gmail, yahoo, hotmail, outlook, icloud, protonmail |

---

## 📄 Export Examples

### CSV output (Minimal preset)
```csv
"#","First Name","Phone"
"1","Léo","+33 6 12 34 56 78"
"2","Fatima","+216 22 456 789"
"3","James","+1 (312) 555-4821"
```

### CSV output (Full preset)
```csv
"#","First Name","Last Name","Phone","Email","Gender","Country","Flag","Dial Code","Country Code"
"1","Léo","Martin","+33 6 12 34 56 78","leo.martin42@gmail.com","Male","France","🇫🇷","+33","FR"
"2","Fatima","Ben Ali","+216 22 456 789","fatima.benali@topnet.tn","Female","Tunisia","🇹🇳","+216","TN"
```

### VCF output
```
BEGIN:VCARD
VERSION:3.0
FN:Léo Martin
N:Martin;Léo;;;
TEL;TYPE=CELL:+33612345678
EMAIL:leo.martin42@gmail.com
ADR;TYPE=HOME:;;;;;;France
NOTE:Male
END:VCARD
```

---

## 🔒 Privacy

- **100% client-side** — nothing is sent anywhere
- **No tracking, no analytics, no cookies**
- **No external requests** — works fully offline
- All data is randomly generated and fictional

---

## 🛠️ Tech Stack

| | |
|---|---|
| **Language** | Vanilla HTML + CSS + JavaScript |
| **Dependencies** | None |
| **Bundle size** | ~1 file, ~70kb |
| **Frameworks** | None |
| **Build tools** | None |

---

## 🤝 Contributing

Pull requests are welcome. Some ideas if you want to contribute:

- [ ] Add more countries
- [ ] Add more name databases (Eastern Europe, Southeast Asia, West Africa)
- [ ] Add date of birth generation
- [ ] Add address generation per country
- [ ] Add profile photo placeholder (avatar initials)
- [ ] Dark/light mode toggle
- [ ] Pagination for large contact lists
- [ ] Copy single contact to clipboard

### Adding a new country

```javascript
{
    name: "YourCountry",
    code: "YC",           // ISO 3166-1 alpha-2
    dial: "+XX",          // International dial code
    flag: "🏳️",           // Emoji flag
    region: "YourRegion", // Groups in the UI
    maleNames:   [...],   // 30+ names recommended
    femaleNames: [...],   // 30+ names recommended
    lastNames:   [...],   // 30+ names recommended
    phoneFormat: () => `+XX ...` // Use ri(min,max) for random digits
}
```

Then add it to the `COUNTRIES` array — that's it.

---

## 📋 Use Cases

- **Testing** — populate a CRM, app, or database with realistic fake contacts
- **Design** — fill UI mockups with believable data instead of "John Doe"
- **QA** — test import flows in contact management apps
- **Education** — demonstrate data formats (VCF, CSV) to students
- **Privacy testing** — generate bulk contacts without using real personal data

---

## ⚠️ Disclaimer

All generated contacts are **entirely fictional**. Any resemblance to real persons is coincidental. Do not use generated data to impersonate real individuals or for any illegal purpose.


--- <p align="center">Made with ♥</p> ```
