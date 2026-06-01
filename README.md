# EEG Bruck & Pinzgauer Zentralraum – Website

Grav CMS, Theme `eeg-bruck`, Sprache Deutsch.

---

## Offene Punkte vor Live-Gang

### Kritisch (rechtlich / funktional)

- [ ] **Impressum vervollständigen** (`pages/07.impressum/text.md`)
  - ZVR-Zahl des Vereins eintragen
  - Ladungsfähige Anschrift eintragen
  - UID-Nummer eintragen (falls vorhanden)
  - Datenschutzerklärung durch rechtlich geprüfte Version ersetzen (Platzhalter-Hinweis im Text)

- [ ] **E-Mail-Zieladresse anpassen** (`pages/05.kontakt/kontakt.md`, Feld `form.process.email.to`)
  - Aktuell: `eeg.bruck@gmail.com`
  - Wird geändert, sobald Domäne beim neuen Hoster liegt

- [ ] **SMTP konfigurieren** (`plugins/email/email.yaml`)
  - Mailserver des neuen Hosters eintragen (Server, Port, Verschlüsselung, User, Passwort)
  - Danach Kontaktformular testen und Mailzustellung prüfen

### Inhalt

- [ ] **Datenerhebungsblatt** als PDF bereitstellen
  - Datei in `user/pages/06.anmelden/` ablegen
  - Link in `pages/06.anmelden/text.md` auf die Datei setzen (z.B. `[Datenerhebungsblatt herunterladen →](datenerhebungsblatt.pdf)`)

- [ ] **OG-Bild** für Social Sharing hinterlegen
  - Bilddatei in `themes/eeg-bruck/images/` ablegen
  - In `themes/eeg-bruck/templates/partials/base.html.twig` eintragen:
    `<meta property="og:image" content="{{ url('theme://images/DATEINAME.jpg', true) }}">`

### Optional / Pflege

- [ ] Weitere News-Beiträge unter `pages/04.aktuelles/` anlegen
- [ ] Tarife aktualisieren, sobald neue Beschlüsse vorliegen (`pages/03.aktuelle-tarife/tarife.md`)

---

## Inhaltspflege

Alle Texte und Daten werden direkt in den Markdown-Dateien unter `pages/` gepflegt.
Jede Seite hat YAML-Frontmatter für strukturierte Felder (Tarife, Team, FAQ usw.)
und optionalen Markdown-Fließtext darunter.

Seiten:
| Ordner | URL | Inhalt |
|---|---|---|
| `01.home` | `/` | Hero, Zahlen, Leistungen, FAQ, Team, CTA |
| `02.leistungen` | `/leistungen` | Leistungsbeschreibung |
| `03.aktuelle-tarife` | `/aktuelle-tarife` | Tariftabelle |
| `04.aktuelles` | `/aktuelles` | Blog/News (Unterseiten = Beiträge) |
| `05.kontakt` | `/kontakt` | Kontaktformular + Ansprechpartner |
| `06.anmelden` | `/anmelden` | Anmeldeprozess |
| `07.impressum` | `/impressum` | Impressum & Datenschutz |
