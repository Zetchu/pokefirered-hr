# pokefirered-hr

Hrvatski fan prijevod Pokémon FireRed/LeafGreen, na bazi [pret/pokefirered](https://github.com/pret/pokefirered) dekompilacije.

- `origin` → https://github.com/Zetchu/pokefirered-hr (fork)
- `upstream` → https://github.com/pret/pokefirered
- Referenca za lokalizaciju: španjolski fork [SomeRandomSponge/pokefireredlatino](https://github.com/SomeRandomSponge/pokefireredlatino)

## Pravila prijevoda

- **Ostaje na engleskom:** imena Pokémona, napada (moves) i abilityja.
- **Prevodi se:** dijalozi, meniji, opisi (Pokédex, itemi, napadi), sistemske poruke.
- **Terminologija:** `docs/pojmovnik.md` je izvor istine za pojmove (Torba, GYM, obraćanje s „ti“, velika slova kao u EN).
- **Dijakritici:** č ć š ž đ i Č Ć Š Ž Đ su u fontu i `charmap.txt`, na mjestima bivših njemačkih/španjolskih znakova: Č Ć Š = F1 F2 F3, č ć š = F4 F5 F6, Ž ž = 14 29, Đ đ = 15 2A (`CHAR_C_CARON` itd. u `include/characters.h`). Španjolski/njemački znakovi su uklonjeni iz charmapa. Tipkovnica za upis imena (`src/naming_screen.c`) još nema naša slova.
- **Dinamička imena:** igra ubacuje `{PLAYER}`, `{RIVAL}`, `{STR_VAR_1}`, imena Pokémona i slično u runtimeu. Rečenice oblikovati tako da ime stoji u nominativu i da ne ovisi o rodu (npr. „Pokémon {STR_VAR_1} je naučio…“ izbjegavati; bolje „{STR_VAR_1}: naučen novi napad!“ ili neutralne konstrukcije).
- **Prostor je ograničen:** tekstni okviri imaju fiksnu širinu, a `\n` / `\l` / `\p` kontroliraju prijelome. Nakon prijevoda provjeriti u emulatoru da tekst ne izlazi iz okvira.

## Build (macOS, Apple Silicon)

Preduvjeti: Homebrew `make` (gmake), `gnu-sed`, `libpng`, `pkg-config`, devkitARM u `/opt/devkitpro` (`DEVKITPRO`/`DEVKITARM` u `~/.zshrc`), agbcc instaliran u `tools/agbcc` (iz `~/decomps/agbcc`: `gsed 's/^make/gmake/g' build.sh | sh && ./install.sh ../pokefirered-hr`).

```sh
gmake -j$(sysctl -n hw.ncpu)            # pokefirered.gba
gmake leafgreen -j$(sysctl -n hw.ncpu)  # pokeleafgreen.gba
gmake compare_firered compare_leafgreen # provjera SHA1 prema originalu (samo za neizmijenjen kod)
open -a mGBA pokefirered.gba
```

Na macOS-u uvijek koristiti `gmake`, ne `/usr/bin/make` (stari BSD/GNU 3.81).

## Gdje su tekstovi

- `data/maps/<Mapa>/text.inc`: dijalozi po mapama (`scripts.inc` sadrži logiku)
- `data/text/*.inc`: zajednički skriptni tekstovi (PC, Poké Mart, trade, save, help system…)
- `src/strings.c`: tekstovi menija i UI-ja (`gText_*`)
- `src/data/pokemon/pokedex_text.h` (FR) / `pokedex_text_lg.h` (LG), `pokedex_categories.h`: Pokédex
- `src/move_descriptions.c`: opisi napada
- `src/data/items.json`: imena i opisi itema (`description_english`)
- `src/data/text/*.h`: imena (species, moves, abilities, natures, trainer classes; ostaju EN osim natures/klasa po dogovoru), Teachy TV, Quest Log
- `src/data/region_map/region_map_sections.json`: imena mjesta (`"name"`). Predlošci `*.json.txt` izvode nazive C varijabli iz ID-a (`sMapsecName_MAPSEC_*`), ne iz teksta, pa se imena smiju slobodno mijenjati.
- `charmap.txt`: mapiranje znakova na bajtove
- `graphics/fonts/latin_*.png` + `src/text.c`: font i širine glifova

## Git

- Ne commitati/pushati bez odobrenja.
- Nikad ne dodavati `.gba` / `.sav` / savestateove (pokriva `.gitignore`; `data/mb_*.gba` su upstream multiboot binarke i ostaju).
