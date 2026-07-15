# 🧘 Mobilní masérna – Systém masérů ČR

## Soubory v repozitáři

| Soubor | Popis |
|--------|-------|
| `index.html` | Hlavní mapa systému s 77 okresy |
| `formular.html` | Registrační formulář pro kolegy |
| `data.json` | Databáze masérů (automaticky se plní) |
| `Mobilnimaserna.svg` | Mapa ČR |

## Jak to funguje

1. Kolega otevře `formular.html` a vyplní údaje
2. Data se uloží do `data.json` v tomto repozitáři
3. Zároveň se vytvoří GitHub Issue pro přehled
4. Mapa na `index.html` zobrazuje pokrytí

## Nastavení

V souboru `formular.html` nahraď:
```
const TOKEN = "VLOZ_SVUJ_GITHUB_TOKEN";
```

Token vygeneruješ na:
**github.com → Settings → Developer settings → Personal access tokens**

## Odkaz pro kolegy

```
https://coulcz.github.io/masaze/formular.html
```
