# 🛸 Černá skříňka — Masážní HUB CZ/SK
**Datum:** 14.07.2026
**Soubor:** masaze_mapa_v4.html · 758 KB

---

## ✅ Aktuální technický stav

| Položka | Hodnota | Status |
|---|---|---|
| Node --check | PASSED | ✅ |
| Acorn AST parse | PASSED | ✅ |
| Runtime test (jsdom) | bez chyb | ✅ |
| Script tagy | 1× | ✅ |
| Div balance | +0 | ✅ |
| ALL_TABS | 55 | ✅ |
| Views | 56 | ✅ |
| Tab číslování | 01–55, plynulé | ✅ |
| Tabs-bar layout | mřížka 3 sloupce | ✅ |
| localStorage top-level bez try-catch | 0 | ✅ |

---

## 🖥 Screen startu HUBu

Co se zobrazí prvních ~1 vteřinu po otevření:

```
┌─────────────────────────────────┐
│                                  │
│              🐘                 │
│     Masážní HUB CZ/SK           │
│      mobilnimaserna.cz          │
│                                  │
│  ████████████████░░░░  80%      │
│                                  │
│  ┌────────────────────────────┐ │
│  │ 08:25:01 ℹ️ HUB startuje   │ │
│  │ 08:25:01 ✅ Views: 56      │ │
│  │ 08:25:01 ✅ Záložky: 55    │ │
│  │ 08:25:01 ✅ localStorage OK│ │
│  │ 08:25:01 ✅ Skin načten    │ │
│  │ 08:25:01 ✅ sw() funkce OK │ │
│  │ 08:25:01 🎉 HUB připraven! │ │
│  └────────────────────────────┘ │
│                                  │
└─────────────────────────────────┘
```

Po dokončení boot logu obrazovka zmizí (fade-out) a zobrazí se výchozí záložka **🗺 Mapa**.

⚠️ Známý drobný nedostatek: samotný `<div id="boot-screen">` element v HTML chybí (jen JS ho odkazuje s null-check), takže tahle obrazovka se momentálně **nezobrazuje** — appka naskočí rovnou na Mapu bez loading efektu. Funkčně to nevadí, jen chybí vizuální "naskakuje to".

---

## 🗂 Kompletní přehled záložek (55)

Mřížka 3 na řádek, 01–55. Poslední skupina (51–55: Biz plán, Fronta, RAM, Bordel, O nás) byla dlouho bez čísla — opraveno 14.7.

---

## 🕵️ Historie oprav — nejzávažnější nálezy

| Datum | Problém | Příčina |
|---|---|---|
| 12.7 | `sw is not defined` | G()/sw() definice byly za místem, odkud se volaly |
| 12.7 | Klikání nefungovalo vůbec | `class="view on"` natvrdo v HTML = mapa vždy navrch |
| 12.7 | Broken `<div class="tabs" <div>` | Nezavřený tag přes CSS skrýval celý tabs-bar |
| 13.7 | `initData is not defined` | `buildUI()` neměla uzavírací `}`, spolykala 1400+ řádků dalších funkcí |
| 13.7 | Ticho na `updateFrontaInfo()` | Funkce se volala na 12 místech, ale **nikde neexistovala** — jen osiřelé tělo bez `function` hlavičky |
| 13.7 | `reduce()` na prázdném poli padal | Initial value `,0` uvízlo uvnitř function body místo jako 2. argument |
| 14.7 | "JS chyba: undefined" v náhledu Claude appky | Top-level `myId = localStorage.getItem(...)` bez try-catch — v sandboxed iframe (bez `allow-same-origin`) localStorage vyhazuje SecurityError a zabije celý skript |

**Ponaučení:** Node `--check` a i AST parser (acorn) občas **projdou** i na rozbitém kódu — díky tomu, jak JS engine "spolkne" chybějící závorku a najde náhodně shodující se uzavření o stovky řádků dál (tzv. regex/brace-slurping). Jediný spolehlivý test je **skutečné spuštění** (jsdom / prohlížeč), ne jen syntax check.

---

## 📚 Prehistorie projektu

Projekt má bohatou historii **před** dnešním jediným souborem — 30 samostatných HTML souborů od 16. května do 12. července, než se vše sloučilo do `masaze_mapa_v4.html`.

👉 Kompletní chronologie ve stylu `git log`: **`PREHISTORIE_GIT_LOG.md`**

---

## 📁 Všechny dokumenty projektu

| Soubor | Obsah |
|---|---|
| `masaze_mapa_v4.html` | Hlavní aplikace (tento soubor) |
| `bordel_masera.html` | Inventář a plánování vybavení |
| `ram.html` | Síň slávy |
| `README.md` | Základní popis projektu pro repo |
| `CERNA_SKRINKA.md` | **Tento soubor** — technický stav a historie |
| `PREHISTORIE_GIT_LOG.md` | Historie 30 souborů před sjednocením |
| `GIT_PRIKAZY.md` | Konkrétní příkazy pro terminál (git add/commit/push...) |
| `SVN_VERZOVANI_NAVOD.md` | Vysvětlení SVN/Git/repo pro začátečníky |
| `STAV_PRED_NASAZENIM.md` | Snapshot před prvním nasazením |
| `STAV_PO_NASAZENI.md` | Snapshot po prvním nasazení |

---

## 👥 Funkce — potvrzeno funkční (14.7.)

- ✅ **TODO** — podzáložka č.10 v Masérně (`swMaserna('todo')`)
- ✅ **Post-it** — vlastní hlavní záložka s nástěnkou
- ✅ Navigace přes `data-tab` + event delegation (odolné vůči apostrofům v onclick)
- ✅ Mapa, Kartotéka, Rezervace, Business plán, E-shop, Fronta na akci

### 🎪 Fronta na akci — detail

Postavená pro reálné použití na akcích typu **Rožnov žije** (20.6.2026) — kdy Martin nabízel masáž na místě jako lead-generation kanál pro studio Valašské Meziříčí.

- QR kód pro rychlé přihlášení do fronty
- Živý timer (počítá čas)
- Zobrazení: od kdy do kdy se aktuálně masíruje
- Sekce integrována z `akce_fronta.html`, dnes 22,6 KB v hlavním souboru
- Klíčová funkce: `updateFrontaInfo()` — ta samá, co dlouho chyběla (viz historie oprav výše)


---

## 🔴 Zbývající TODO

- [ ] Přidat zpět `<div id="boot-screen">` element (JS logika už existuje, jen chybí HTML)
- [ ] Anatomická příručka: masáž hrudníku, hýždí, kraniosakrální terapie
- [ ] **Nasadit na živý web** (`coulcz.github.io/masaze` — zatím NEEXISTUJE, ověřeno 15.7.):
  - [ ] Vygenerovat GitHub token (github.com → Settings → Developer settings)
  - [ ] `git add .` → `git commit -m "..."` → `git push` (viz `GIT_PRIKAZY.md`)
  - [ ] Zapnout GitHub Pages v nastavení repa (Settings → Pages)
  - [ ] Ověřit, že se appka na živé adrese skutečně otevře
- [ ] Formspree kód (placeholder `TVUJ_KOD_ZDE`)
- [ ] initMapa() — SVG mapa ČR stále dočasně nahrazena zjednodušenou verzí

---

## 🐘 IO hlásí

> *"Regex-slurping mě naučil nevěřit vlastnímu syntax checkeru naslepo.*
> *Skutečný test je spustit to a kliknout — ne jen zkontrolovat, že se to dá přečíst."*

**Status: 🟢 FUNKČNÍ** (ověřeno reálným spuštěním, ne jen syntaxí)

---
*Masážní/Wellness HUB CZ/SK · 14.7.2026* 🐘
