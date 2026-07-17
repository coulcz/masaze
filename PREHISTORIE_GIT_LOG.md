# 🕰 Prehistorie projektu — jako `git log`

Než jsme začali s Gitem, projekt se vyvíjel jako řada samostatných souborů. Tady je jejich historie zapsaná ve stylu, jak by ji zobrazil `git log --oneline`, kdybychom Git používali od začátku.

---

```
git log --oneline --all
```

**03bef1**  `2026-07-14`  SOUČASNÝ STAV — hlavní app (786KB)
　　　　　　　　　→ `masaze_mapa_v4.html` (785KB)

**03a002**  `2026-07-12`  Automatizovaná test suite
　　　　　　　　　→ `TEST_SUITE.html` (6KB)

**038113**  `2026-07-12`  Testovací minimal sw()
　　　　　　　　　→ `TEST_SW.html` (1KB)

**036224**  `2026-07-08`  Inventář a plánování (81KB)
　　　　　　　　　→ `bordel_masera.html` (82KB)

**034335**  `2026-07-04`  TODO systém
　　　　　　　　　→ `todo.html` (97KB)

**032446**  `2026-07-04`  Návod pro maséry
　　　　　　　　　→ `navod_maseri.html` (14KB)

**030557**  `2026-07-03`  Krajské členění
　　　　　　　　　→ `kraj.html` (29KB)

**02e668**  `2026-07-03`  Tisk pro akce
　　　　　　　　　→ `tisk_akce.html` (22KB)

**02c779**  `2026-07-02`  Poptávkový formulář
　　　　　　　　　→ `poptavka.html` (9KB)

**02a88a**  `2026-06-29`  Klientský modul
　　　　　　　　　→ `klient.html` (42KB)

**02899b**  `2026-06-29`  Síň slávy (Zlatý RAM)
　　　　　　　　　→ `ram.html` (12KB)

**026aac**  `2026-06-27`  Fronta na akce (QR, timer)
　　　　　　　　　→ `akce_fronta.html` (64KB)

**024bbd**  `2026-06-27`  Modul pro klientky
　　　　　　　　　→ `masaze_zeny.html` (26KB)

**022cce**  `2026-06-27`  Pracovní sešity
　　　　　　　　　→ `sesity.html` (36KB)

**020ddf**  `2026-06-27`  První masérna modul
　　　　　　　　　→ `prvni_maserna.html` (26KB)

**01eef0**  `2026-06-16`  Rezervační systém
　　　　　　　　　→ `rezervace.html` (14KB)

**01d001**  `2026-06-12`  Formulář finální
　　　　　　　　　→ `formular_final.html` (28KB)

**01b112**  `2026-06-12`  Mapa v3
　　　　　　　　　→ `masaze_mapa_v3.html` (58KB)

**019223**  `2026-06-10`  Formulář v3
　　　　　　　　　→ `formular_v3.html` (15KB)

**017334**  `2026-06-10`  Formulář zjednodušen
　　　　　　　　　→ `formular.html` (18KB)

**015445**  `2026-06-09`  Formulář v2
　　　　　　　　　→ `formular_maseri_v2.html` (16KB)

**013556**  `2026-06-09`  Registrační formulář
　　　　　　　　　→ `formular_maseri.html` (14KB)

**011667**  `2026-06-04`  Verzování začíná — v2
　　　　　　　　　→ `masaze_mapa_v2.html` (51KB)

**00f778**  `2026-06-04`  SVG mapa ČR (952KB)
　　　　　　　　　→ `masaze_svg_mapa.html` (951KB)

**00d889**  `2026-06-04`  Mapa podle okresů
　　　　　　　　　→ `masaze_mapa_okresy.html` (12KB)

**00b99a**  `2026-06-03`  Všech 77 okresů ČR
　　　　　　　　　→ `masaze_77okresu.html` (50KB)

**009aab**  `2026-06-03`  Verze "final" (první z mnoha :)
　　　　　　　　　→ `masaze_final.html` (51KB)

**007bbc**  `2026-05-18`  Přidány okresy ČR
　　　　　　　　　→ `masaze_okresy.html` (63KB)

**005ccd**  `2026-05-18`  První opravy
　　　　　　　　　→ `masaze_opraveny.html` (55KB)

**003dde**  `2026-05-17`  Základ projektu
　　　　　　　　　→ `masaze.html` (52KB)

**001eef**  `2026-05-16`  Genesis — první pokus
　　　　　　　　　→ `masaze_system.html` (58KB)

---

## 📊 Statistiky prehistorie

| | |
|---|---|
| Období | 2026-05-16 → 2026-07-14 |
| Počet "commitů" (souborů) | 31 |
| Trvání | necelé 2 měsíce |
| Největší skok | masaze.html (53KB) → masaze_mapa_v4.html (786KB) |

---

## 🌱 Co kdyby to bylo v Gitu od začátku?

Každý ten soubor výše by byl jeden `git commit`. Místo:

```
masaze.html
masaze_opraveny.html
masaze_final.html
masaze_mapa_v2.html
...
```

by existoval **jeden** soubor `masaze_mapa_v4.html`, a historie by žila v:

```bash
git log --oneline
```

S možností se kdykoliv vrátit:

```bash
git checkout <hash> -- masaze_mapa_v4.html
```

---

## 🚀 Od teď dál

Prehistorie skončila. Od chvíle, kdy soubor nahraješ do repa `coulcz/masaze` a uděláš první `git commit`, začíná **skutečná historie** — sledovatelná, prohledatelná, vratitelná.

Viz `GIT_PRIKAZY.md` pro konkrétní příkazy.

---

*Masážní/Wellness HUB CZ/SK · 14.7.2026* 🐘