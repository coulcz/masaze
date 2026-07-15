# 🗂 Co je SVN a "repo" — jednoduše

## Co to vůbec je?

**Verzovací systém** = program, který si pamatuje KAŽDOU změnu tvého kódu. Jako kdyby sis po každé úpravě uložil zálohu, ale automaticky a s popiskem "co jsem změnil a proč".

**Repo** (repozitář) = "trezor", kde se ta historie ukládá.

Existují dva hlavní typy:

| | SVN | Git |
|---|---|---|
| Stáří | starší (2000) | modernější (2005) |
| Jak funguje | jeden centrální server | každý má kopii celé historie |
| Populace dnes | málo se používá | naprostá většina |
| Příklad služby | vlastní SVN server | GitHub, GitLab |

👉 **Ten program, co jsi používal, měl pravděpodobně vestavěné SVN nebo Git připojení** — běžné u vývojářských programů (IDE).

---

## Co MÁŠ ty už teď

Ty už verzovací systém **částečně používáš** — jen ne přes žádný program, ale ručně:

```
masaze_mapa_v4.html
masaze_mapa_v4_ZALOHA_20260710_0917.html
masaze_mapa_v4_ZALOHA_20260712_0821.html
masaze_mapa_v4_ZALOHA_20260714_0435.html
...
```

Každá `_ZALOHA_` = jedna "verze" v čase. Přesně to samé dělá Git/SVN, jen **automaticky** a s možností napsat si poznámku typu *"opravil jsem mapu"* místo pamatování si co je v kterém souboru.

---

## Co bys získal navíc s Gitem/GitHubem

- ✅ Vrátit se k libovolné starší verzi jedním klikem
- ✅ Vidět přesně **co** se mezi verzemi změnilo (barevně podtržené řádky)
- ✅ Psát krátké poznámky ke každé změně
- ✅ Sdílet projekt s týmem (Lucie, Honza, Luboš, Eva)
- ✅ Nemuset si pamatovat, který ZALOHA soubor je ten "dobrý"

---

## Co doporučuju tobě konkrétně

**Git, ne SVN.** Máš totiž už repo `coulcz/masaze` na GitHubu (Git je za GitHubem), takže:

1. **GitHub Desktop** (zdarma, grafické rozhraní, žádné příkazy)
   → https://desktop.github.com

2. Nainstaluješ, přihlásíš se svým GitHub účtem

3. "Clone" tvého repa `coulcz/masaze`

4. Pak stačí: uprav soubor → v GitHub Desktop klikni "Commit" → napiš poznámku → "Push"

To je celé. Žádné příkazy do terminálu, jen klikání.

---

## Pojmy které uslyšíš (slovníček)

| Pojem | Co znamená |
|---|---|
| **Commit** | "Uložit tuhle verzi s poznámkou" |
| **Push** | "Nahrát moje změny na server (GitHub)" |
| **Pull** | "Stáhnout nejnovější změny ze serveru" |
| **Repo / repozitář** | Trezor s celou historií projektu |
| **Branch** | Paralelní vývojová větev (pro pokročilé, zatím neřeš) |

---

*Vytvořeno pro Masážní/Wellness HUB CZ/SK · 14.7.2026* 🐘
