# 💻 Git příkazy — do terminálu

Návod pro ty, co chtějí místo klikání v GitHub Desktop používat příkazovou řádku (terminál / Příkazový řádek / PowerShell).

---

## 1️⃣ Jednorázové nastavení (uděláš jen jednou)

```bash
git config --global user.name "Martin"
git config --global user.email "tvuj@email.cz"
```

Řekne to Gitu, kdo jsi — objeví se to u každé změny.

---

## 2️⃣ Stažení repa poprvé (clone)

```bash
git clone https://github.com/coulcz/masaze.git
```

Stáhne se ti celý projekt do složky `masaze` tam, kde v terminálu zrovna jsi.

---

## 3️⃣ Denní pracovní cyklus (tohle použiješ nejčastěji)

```bash
# 1. Přejít do složky s projektem
cd masaze

# 2. Podívat se co se od minule změnilo
git status

# 3. Přidat změněné soubory k uložení
git add masaze_mapa_v4.html

# nebo úplně všechny změněné soubory najednou:
git add .

# 4. Uložit s poznámkou co jsi udělal
git commit -m "Opravena mapa, pridany skiny"

# 5. Nahrát na GitHub
git push
```

---

## 4️⃣ Stažení nejnovější verze (než začneš dělat změny)

```bash
git pull
```

Vždycky spusť **před** tím, než začneš upravovat — kdyby mezitím Lucie/Honza/Luboš/Eva něco změnili.

---

## 5️⃣ Zjistit historii změn

```bash
# Krátký přehled
git log --oneline

# S detaily
git log
```

Uvidíš seznam všech uložených verzí s poznámkami.

---

## 6️⃣ Vrátit se k dřívější verzi

```bash
# Zjistit ID starší verze (z git log --oneline, např. "a1b2c3d")
git checkout a1b2c3d -- masaze_mapa_v4.html
```

Vrátí JEDEN soubor do stavu, jaký měl v té verzi. Neztratíš tím historii, jen se soubor "přepíše" na starou verzi.

---

## 7️⃣ Když se něco pokazí (záchranná brzda)

```bash
# Zahodit VŠECHNY neuložené změny, vrátit se k poslední uložené verzi
git checkout -- .

# Zjistit, co přesně se v souboru změnilo oproti poslední verzi
git diff masaze_mapa_v4.html
```

---

## 📋 Rychlá referenční tabulka

| Příkaz | Co dělá |
|---|---|
| `git status` | Co je změněné |
| `git add .` | Připravit vše k uložení |
| `git commit -m "text"` | Uložit s poznámkou |
| `git push` | Nahrát na GitHub |
| `git pull` | Stáhnout nejnovější verzi |
| `git log --oneline` | Historie změn |
| `git diff` | Co přesně se změnilo |

---

## 💡 Tip na začátek

Pokud ti příkazy přijdou složité, klidně zůstaň u **GitHub Desktop** (grafické rozhraní) — dělá přesně totéž jen klikáním. Tenhle soubor si nech jako referenci, až budeš chtít zkusit terminál.

---

*Pro Masážní/Wellness HUB CZ/SK · repo: coulcz/masaze* 🐘
