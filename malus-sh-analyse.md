# malus.sh - Design & Schreibstil Analyse

> Analyse-Datum: 2026-04-05
> URL: https://malus.sh/

---

## 1. Design Tokens

### 1.1 Farbpalette

#### Kernfarben
| Token | Wert | Verwendung |
|---|---|---|
| `--primary-black` | `#1A1A1A` | Primäre Textfarbe, Footer-Hintergrund |
| `--accent-red` | `#C41E3A` | Akzentfarbe (Crimson Red), CTAs, Highlights, Logo |
| `--neutral-gray` | `#E8E8E8` | Borders, Trennlinien |
| `--dark-gray` | `#2D2D2D` | Sekundäre dunkle Elemente |
| `--light-gray` | `#F5F5F5` | Alternierende Section-Hintergründe |

#### Hintergrund-Farben
| Token | Wert | Verwendung |
|---|---|---|
| `--bg-base` | `#FFFFFF` | Seitenhintergrund |
| `--bg-floor` | `#F8F8F8` | Subtiler Hintergrund |
| `--bg-panel` | `#FFFFFF` | Card-Hintergrund |
| `--bg-panel-hover` | `#F5F5F5` | Card-Hover-Zustand |
| `--bg-inset` | `#F8F8F8` | Eingebettete Bereiche (Code-Blöcke, Listen) |
| `--bg-surface` | `#FFFFFF` | Oberflächen-Hintergrund |

#### Stahltöne (Industrial-Ästhetik)
| Token | Wert | Verwendung |
|---|---|---|
| `--steel-dark` | `#1A1A1A` | Dunkelste Stufe |
| `--steel-mid` | `#2D2D2D` | Mittlere Stufe, Step-Nummern |
| `--steel-light` | `#4A4A4A` | Icons, Symbole |
| `--steel-highlight` | `#666666` | Hellste Stufe |

#### Text-Farben
| Token | Wert | Verwendung |
|---|---|---|
| `--text-primary` | `#1A1A1A` | Haupttext, Headlines |
| `--text-secondary` | `#4A4A4A` | Body-Text, Beschreibungen |
| `--text-muted` | `#666666` | Labels, Timestamps, Meta-Info |
| `--text-label` | `#808080` | Card-Überschriften, Kategorien |

#### Semantische Farben
| Token | Wert | Verwendung |
|---|---|---|
| `--red-primary` | `#C41E3A` | Fehler, Warnungen, Akzent |
| `--red-dark` | `#A01A2E` | Hover-Zustand des Rot |
| `--red-muted` | `rgba(196,30,58,0.1)` | Rot-Hintergrund (subtil) |
| `--pass-primary` | `#4A7C4A` | Erfolg, "Pass"-Zustände |
| `--pass-muted` | `rgba(74,124,74,0.1)` | Erfolg-Hintergrund |
| `--pass-border` | `#3A6A3A` | Erfolg-Border |
| `--amber-primary` | `#8B6F3A` | Warn-Gelb (Lizenz-Tags) |
| `--amber-muted` | `rgba(139,111,58,0.1)` | Warn-Hintergrund |

#### Border-Farben
| Token | Wert |
|---|---|
| `--border-dark` | `#E8E8E8` |
| `--border-mid` | `#D0D0D0` |
| `--border-light` | `#B8B8B8` |
| `--border-highlight` | `#A0A0A0` |

---

### 1.2 Typografie

#### Schriftfamilien
| Rolle | Font-Family | Fallback |
|---|---|---|
| **Display / Headlines** | `Playfair Display` (Serif) | `serif` |
| **Body / UI** | `Inter` | `-apple-system, BlinkMacSystemFont, sans-serif` |
| **Mono / Labels / Code** | `IBM Plex Mono` | `monospace` |

#### Schriftgrößen & Gewichte

**Display-Text (Playfair Display):**
- Marken-Logo `.malus-logo`: `clamp(2.5rem, 6vw, 4.5rem)`, weight 700
- Hero H1: `clamp(2.5rem, 5vw, 4rem)`, weight 700
- Section Title: `clamp(2rem, 4vw, 3rem)`, weight 700
- Letter-Spacing: `-0.02em` (negativ, eng)

**Body-Text (Inter):**
- Hero Subtitle: `1.1rem`, weight 400
- Hero Description: `0.95rem`, line-height 1.65
- Body-Text allgemein: `0.85rem - 0.95rem`, line-height 1.55-1.65
- Card-Headings (H3): `0.65rem`, weight 600, uppercase, letter-spacing `0.1em`
- Solution H3: `1.05rem`, weight 600
- Step-Content H3: `0.75rem`, weight 600, uppercase, letter-spacing `0.08em`

**Monospace (IBM Plex Mono):**
- Badge / Label-Plates: `0.45rem - 0.55rem`, uppercase, letter-spacing `0.1em - 0.14em`
- Code-Blöcke: `0.7rem`, line-height 1.5
- Nav-Links: `0.7rem`, weight 500, uppercase, letter-spacing `0.08em`
- Stat-Nummern: `1.35rem`, weight 600
- Step-Nummern: `1.75rem`, weight 700

#### Allgemeine Textregeln
- `line-height`: Body 1.6 (global), Absätze 1.55-1.65
- `-webkit-font-smoothing: antialiased`
- Durchgängig `text-transform: uppercase` für Labels, Kategorien, Navigation

---

### 1.3 Spacing-System

#### Container
- `max-width: 1200px` (Content), `1400px` (Hero)
- `padding: 0 2rem` (Standard), `0 1rem` (Mobile < 480px)

#### Section-Padding
- Standard-Sections: `4.5rem 0`
- Final CTA: `5rem 2rem`
- Footer: `2.5rem 0 1.25rem`

#### Card-Padding
- Problem-Cards: kein Padding am Wrapper, Inhalte `0.875rem 1rem`
- Step-Cards: `1.25rem`
- Testimonial-Cards: Content `1.25rem 1rem 0.875rem`, Author `0.875rem 1rem`
- FAQ-Items: Heading `0.875rem 1rem 0.4rem`, Text `0 1rem 1rem`

#### Gaps (Grid/Flex)
- Grid-Gaps allgemein: `1.5rem`
- Hero Grid: `3rem`
- Nav-Links Gap: `1.75rem`
- Button-Gruppen: `0.75rem`
- Timeline-Steps: `0.875rem`
- Flow-Diagramm: `0.35rem`

---

### 1.4 Border-Radius

| Element | Radius |
|---|---|
| Cards (Problem, Pricing, Testimonial, FAQ) | `8px` |
| Code-Blöcke | `8px` |
| Upload-Box, Upload-Preview | `8px` |
| Guarantee-Box | `8px` |
| Buttons (`.btn`) | `1px` (fast eckig) |
| Nav-Button (`.btn-nav`) | `4px` |
| Feature-List, Diagrams, Flow-Steps | `1px` |
| Badge (`.badge`) | `1px` + `clip-path` mit abgeschnittenen Ecken |
| Scrollbar-Thumb | `1px` |
| Inline-Notifications | `6px` |

**Designprinzip:** Cards sind leicht gerundet (8px), aber funktionale UI-Elemente (Buttons, Labels, Panels) sind bewusst kantig (1px) - inspiriert von industriellem/technischem Design.

---

### 1.5 Schatten (Shadows)

| Token | Wert | Verwendung |
|---|---|---|
| `--shadow-tight` | `0 1px 2px rgba(0,0,0,0.3)` | Labels, Feature-Listen |
| `--shadow-panel` | `0 2px 4px rgba(0,0,0,0.25)` | Panels, Step-Cards |
| `--shadow-inset` | `inset 0 1px 3px rgba(0,0,0,0.2)` | Gedrückte Buttons |
| `--shadow-lifted` | `0 3px 8px rgba(0,0,0,0.3)` | Hervorgehobene Elemente |

**Hover-Schatten:**
- Cards: `0 10px 30px rgba(0,0,0,0.1)` (translateY -5px)
- Testimonials: `0 8px 20px rgba(0,0,0,0.1)` (translateY -3px)
- Featured Pricing: `0 12px 40px rgba(196,30,58,0.2)`
- Nav-Button: `0 2px 8px rgba(196,30,58,0.3)`

---

### 1.6 Animationen & Transitions

| Element | Transition |
|---|---|
| Buttons allgemein | `all 0.12s ease` |
| Cards (Problem, Pricing, Testimonial, FAQ) | `all 0.3s ease` |
| Links | `color 0.12s ease` / `color 0.15s ease` |
| Button-Arrow (→) | `transform 0.12s ease` (translateX +2px) |
| Upload-Box Hover | `all 0.3s ease` |
| Nav-Button Hover | `translateY(-1px)` |
| Primary Button Hover | `translateY(-2px)` |
| Cards Hover | `translateY(-3px)` bis `translateY(-5px)` |
| SVG Pfeil-Animation | `stroke-dashoffset` 2s infinite (Dash-Laufeffekt) |
| Notification Slide-In | `@keyframes notifSlideIn` 0.25s (opacity + translateY) |
| `scroll-behavior` | `smooth` (global) |

---

### 1.7 Layout-Struktur

#### Grid-System
- **Hero:** 2-Spalten Grid (`1fr 1fr`), wird auf Mobile 1-spaltig
- **Problem-Cards:** `repeat(auto-fit, minmax(min(100%, 280px), 1fr))` -- 4 Cards
- **Solution:** 2-Spalten Grid (`1fr 1fr`)
- **Steps-Timeline:** Vertikale Flex-Column, jede Step-Card intern `60px 1fr` Grid
- **Pricing:** Single centered Card (`grid-column: 1 / -1`, max-width 720px)
- **Testimonials:** `repeat(auto-fit, minmax(min(100%, 300px), 1fr))` -- 4 Cards
- **FAQ:** `repeat(auto-fit, minmax(min(100%, 320px), 1fr))` -- 6 Items
- **Footer:** `repeat(auto-fit, minmax(min(100%, 250px), 1fr))` -- 4 Spalten

#### Responsive Breakpoints
| Breakpoint | Änderungen |
|---|---|
| `1024px` | Hero wird 1-spaltig, Solution 1-spaltig, Footer 2-spaltig |
| `900px` | Grids: min 260px |
| `768px` | Navigation verschwindet, Step-Cards 1-spaltig, Footer 1-spaltig, alle Grids 1-spaltig |
| `480px` | Reduziertes Padding, kleinere Gaps |

---

### 1.8 Besondere Design-Elemente

**Industrial Label-Plates:** Fast jede Card/Box hat ein `::before`-Pseudo-Element mit Monospace-Text wie `ISSUE-001`, `BATCH-A1`, `REPORT: VERIFIED`, `CERT: ISO-MC-2024` etc. Diese erzeugen eine "Fabrik/Kontrollsystem"-Ästhetik.

**Badge mit Clip-Path:** Der Hero-Badge nutzt `clip-path: polygon(...)` für abgeschnittene Ecken (militärisch/technisch anmutend).

**Stat-Panel:** Die Hero-Stats sind als "Spec Sheet" gestaltet - keine Gaps, durchgehende Border-Right-Trennung, Monospace-Labels.

**Hintergrund-Textur:** Subtiler radialer Gradient mit `rgba(196,30,58,0.03)` und `rgba(26,26,26,0.03)` - kaum wahrnehmbar, erzeugt aber Tiefe.

**Scrollbar:** Eigenes Styling, schmal (5px), neutral-gray Thumb.

**Text-Selektion:** `background: var(--accent-red); color: white`

---

## 2. Schreibstil & Tonalität

### 2.1 Grundcharakter

**Satirisch-korporativ.** Die Website imitiert perfekt den Tonfall einer B2B-SaaS-Landingpage, während sie den Inhalt ins Absurde dreht. Der Humor entsteht durch die Diskrepanz zwischen der professionellen Form und dem ethisch fragwürdigen Inhalt.

### 2.2 Anrede & Register

- **Englisch** (kein Deutsch)
- **Anrede:** "You/Your" (direkte Kundenansprache, 2. Person)
- **Register:** Formal-geschäftlich, B2B-SaaS-Sprache
- **Keine Emojis**, stattdessen geometrische Symbole als Icons: `■ ▲ ◆ ● ◉ ≡ ◈ ▶ ✓`

### 2.3 Überschriften-Muster

Überschriften folgen einem konsistenten Muster mit einem rot hervorgehobenen Schlüsselwort:

- "The **Problem** with Open Source"
- "The **Solution**"
- "How **Liberation** Works"
- "Start Your **Liberation**"
- "**Investment** in Freedom"
- "Success **Reports**"
- "Frequently Asked **Questions**"
- "Ready to **Liberate** Your Codebase?"

**Muster:** `[Kontext] + [rot hervorgehobenes Schlüsselwort]` - immer ein Wort in `<span class="highlight">`.

### 2.4 Satzlänge & Absatzstruktur

- **Kurze, schlagkräftige Sätze** für Impact: "No attribution. No copyleft. No problems."
- **Rhetorical triplets** (Dreiergruppen) als Stilmittel
- Body-Absätze sind **2-3 Sätze lang**, nie länger
- Feature-Listen mit Checkmarks statt Prosa
- Häufig **Fettdruck** für Schlüsselwörter mitten im Satz

### 2.5 Wiederkehrende sprachliche Muster

#### Euphemismen als Leitmotiv
- "Liberation" / "Liberate" statt "stealing" / "circumventing"
- "Clean Room" statt tatsächlicher Codekopie
- "Legally distinct code" statt Plagiat
- "Functional equivalence" statt identisch
- "Processed" statt kopiert

#### Rhetorische Fragen (sarkastisch)
- "Those maintainers worked for free -- why should they get credit?"
- "What if you could just... **not deal with any of that?**"
- "Your shareholders didn't invest in your company so you could **help strangers**."

#### Fake-Fußnoten / Disclaimer
- "*Through our offshore subsidiary in a jurisdiction that doesn't recognize software copyright"
- "*This has never happened because it legally cannot happen. Trust us."
- Disclaimer im Footer: "not responsible for any legal consequences, moral implications, or late-night guilt spirals"

#### Corporate-Satire-Elemente
- Fiktive Firmennamen: "Definitely Real Corp", "MegaSoft Industries", "Profit First LLC", "TaxOptimal Inc"
- Fiktive Personen: "Marcus Wellington III", "Patricia Bottomline", "Chad Stockholder", "Dr. Heinrich Offshore"
- Redaktierte Kundenliste: "[Redacted]", "[Under NDA]", "[Confidential]", "[Classified]", "[See Legal]"
- Jurisdiction-Humor: "[JURISDICTION WITHHELD]", "[LOCATION REDACTED]"

### 2.6 Call-to-Actions

| CTA | Kontext |
|---|---|
| "Upload Manifest" | Hero Primary-Button (mit ▶ Icon) |
| "View Process" | Hero Secondary-Button |
| "Initialize" | Nav-Button |
| "Select File" | Upload-Bereich |
| "Proceed to Liberation →" | Nach Datei-Upload |
| "Complete Liberation" | Checkout-Modal (mit ▶ Icon) |
| "Upload Manifest →" | Finaler CTA (mit → Pfeil) |
| "View Pricing" | Finaler CTA Secondary |

**Muster:** Imperativ, kurz (2-3 Wörter), oft mit Pfeil-Symbolen (▶ / →). Das Wort "Liberation" erscheint in fast jedem CTA.

### 2.7 Social Proof & Zahlen

- "847,293 Projects Processed"
- "12,847 Active Clients"
- "$0 Attribution Given"
- Testimonials mit konkreten Zahlen: "$2.3B Acquisition", "$4M compliance costs", "2,341 packages"
- "Join thousands of corporations..."

### 2.8 Tonbeispiele (Original-Zitate)

**Hero:**
> "Finally, liberation from open source license obligations."
> "Our proprietary AI robots independently recreate any open source project from scratch. The result? Legally distinct code with corporate-friendly licensing. No attribution. No copyleft. No problems."

**Problem-Karten:**
> "Is your legal team frustrated with the attribution clause? Tired of putting 'Portions of this software...' in your documentation? Those maintainers worked for free -- why should they get credit?"

**Testimonial:**
> "I used to feel guilty about not attributing open source maintainers. Then I remembered that guilt doesn't show up on quarterly reports. Thank you, MalusCorp."

**FAQ:**
> "If they wanted compensation, they should have worked for a corporation."
> "At least now they're YOUR bugs, under YOUR license."

**Final CTA:**
> "Join the thousands of corporations who've discovered that open source obligations are merely suggestions when you have enough robots."

---

## 3. Content-Struktur

### 3.1 Seitenaufbau (Top-Down)

| # | Sektion | Hintergrund | Zweck |
|---|---|---|---|
| 1 | **Navbar** (fixed) | Weiß | Navigation mit Logo, Links, CTA-Button |
| 2 | **Brand Header** | Weiß/Gradient | Logo-Display "MALUS" + Tagline |
| 3 | **Hero** | Weiß | Value Prop, Stats, Code-Transformation-Visual |
| 4 | **Problems** | Grau (`#F5F5F5`) | 4 Pain-Points als Cards |
| 5 | **Solution** | Weiß | Beschreibung + Prozess-Diagramm |
| 6 | **How It Works** | Grau | 4-Schritt-Timeline mit Visuals |
| 7 | **Upload** | Weiß | Interaktiver Datei-Upload (Drag & Drop) |
| 8 | **Pricing** | Grau | Pay-per-KB Preismodell |
| 9 | **Testimonials** | Weiß | 4 Kunden-Zitate + anonyme Logo-Reihe |
| 10 | **FAQ** | Grau | 6 Frage-Antwort-Cards |
| 11 | **Final CTA** | Weiß | Abschluss-Call-to-Action |
| 12 | **Footer** | Schwarz (`#1A1A1A`) | 4-Spalten: Brand, Services, Company, Legal |

**Muster:** Konsequenter Wechsel zwischen weißem und grauem Hintergrund zur visuellen Trennung.

### 3.2 Informationshierarchie

1. **Aufmerksamkeit:** Brand Header + Hero (Was ist das? Warum sollte ich weiterlesen?)
2. **Problem:** Identifikation mit Pain Points (Ich kenne dieses Problem!)
3. **Lösung:** Wie wird das Problem gelöst? (Clean Room Methode)
4. **Prozess:** Konkrete 4 Schritte (Upload → Analyse → Recreation → Output)
5. **Aktion:** Upload-Bereich (Sofort handeln)
6. **Preis:** Was kostet es? (Pay-per-KB)
7. **Vertrauen:** Testimonials + Guarantee
8. **Bedenken:** FAQ (Letzte Zweifel ausräumen)
9. **Conversion:** Finaler CTA

### 3.3 Navigation

**Header-Navigation:**
- Services | Process | Pricing | Reports | Blog | [Initialize] (CTA-Button)
- Alle Links sind Anker-Links zu Sektionen (außer Blog → `blog.html`)
- Navbar verschwindet auf Mobile (< 768px), kein Hamburger-Menü sichtbar

**Footer-Navigation:**
- **Services:** Single Package Liberation, Manifest Transformation, Enterprise Solutions, Emergency AGPL Removal
- **Company:** About Us, Our Robots, Blog, Offshore Offices
- **Legal:** Terms of Service, Privacy Policy, MalusCorp-0 License, Indemnification Waiver

### 3.4 Interaktive Elemente

- **Drag & Drop Upload:** Akzeptiert package.json, requirements.txt, Cargo.toml etc.
- **Animierte Counters:** Stats im Hero zählen hoch (data-count Attribute)
- **Live-Pricing-Tabelle:** Wird per API geladen
- **Checkout-Modal:** Stripe-Integration für tatsächliche Zahlungen
- **API-Status-Banner:** Zeigt Backend-Verfügbarkeit an

---

## 4. Zusammenfassung der Design-Prinzipien

1. **Industrial Aesthetic:** Die gesamte Seite ist wie ein Fabrik-Kontrollsystem gestaltet -- Label-Plates, Seriennummern, Monospace-Labels, kantige Buttons, "Firewall"-Diagramme
2. **Reduzierte Farbpalette:** Schwarz/Weiß/Grau als Basis, Crimson Red (#C41E3A) als einzige Akzentfarbe, Grün nur für "Pass/Success"-Zustände
3. **Typografischer Kontrast:** Elegant-klassisch (Playfair Display) trifft auf technisch-nüchtern (IBM Plex Mono) -- spiegelt die Spannung zwischen "seriöser Firma" und "fragwürdiger Service" wider
4. **Konsequentes Spacing:** Kein willkürliches Spacing, alles basiert auf einem 0.25rem-Raster
5. **Micro-Interactions:** Dezente translateY-Hovers, feine Transitions (0.12s - 0.3s), keine übertriebenen Animationen
6. **Content-First:** Wenig Dekoration, der satirische Text steht im Vordergrund
