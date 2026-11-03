# Pojmovnik

Stalni prijevodi pojmova. Isti engleski pojam uvijek se prevodi isto. Novi pojam prvo dodaj ovdje, pa tek onda koristi u tekstu.

## Način rada (za Claude Code)

- **Ne pitaj za pojedinačne prijevode.** Prevodi samostalno prema ovom pojmovniku i pravilima.
- Ako pojam nije pokriven, **sam odluči** u duhu pravila, dodaj ga u odgovarajuću tablicu s oznakom `(prijedlog)` i nastavi raditi.
- Na kraju svake veće cjeline (npr. jedna datoteka ili jedna skupina mapa) daj **jedan skupni popis** novih `(prijedlog)` pojmova i upitnih rečenica. Ne prekidaj rad zbog njih.
- Pitaj odmah samo ako odluka utječe na više od ~20 stringova ili mijenja pravilo iz ovog dokumenta.
- Prije prijevoda provjeri ograničenje duljine za tu vrstu stringa u kodu (npr. `ITEM_NAME_LENGTH`, `TRAINER_CLASS_NAME_LENGTH`, širina prozora u pikselima). Ako hrvatski ne stane, skrati prema pravilima ispod, a ne mijenjaj kod.

## Ton

- Jednostavan, prirodan, suvremen hrvatski za djecu (otprilike 7 do 12 godina). Kratke rečenice, poznate riječi.
- Standardni jezik, bez dijalekta. Iznimka su likovi koji u originalu govore izrazito ležerno (npr. rival), oni mogu biti razgovorniji.
- Šale i igre riječi prilagodi tako da budu smiješne na hrvatskom. Doslovan prijevod nije cilj.

## Opća pravila

- **Obraćanje:** igraču se svi obraćaju s „ti“.
- **Velika slova:** kao u engleskoj verziji: `POKéMON`, `POKé LOPTA`, imena mjesta i likova (`OAK`, `GRADIĆ PALLET`) ostaju velikim slovima.
- **Ostaju na engleskom:** imena Pokémona, napada (moves), abilityja i likova (BROCK, MISTY, GIOVANNI…).
- **Dinamička imena** (`{PLAYER}`, `{RIVAL}`, `{STR_VAR_1}`…): uvijek u nominativu, bez slaganja po rodu.
- **Dinamički POKéMON** (`{B_ATK_NAME_WITH_PREFIX}`, ime Pokémona u varijabli i sl.): gramatički uvijek **muški rod**, jer je riječ POKéMON muškog roda. Vrijedi i za ženke i za nadimke („{X} se onesvijestio!“, „{X} je otrovan!“).
- **Dinamički predmeti** (`{ITEM}` i sl.): predmeti mogu biti ženskog roda (POKé LOPTA → POKé LOPTU), pa ih ne stavljaj u akuzativ. Koristi dvotočku ili nominativ: „{PLAYER} pronalazi: {ITEM}!“, „Dobiveno: {ITEM}!“, „{ITEM} je spremljen/a“ ne, nego „Spremljeno u TORBU: {ITEM}.“
- **Dinamički treneri** (`{TRAINER}`): mogu biti oba spola. Koristi prezent i nominativ: „{TRAINER} šalje {X}!“, „{TRAINER} gubi borbu!“
- **Spol igrača:** dok igrač ne odabere spol (Oakov uvod), i u tekstu koji vrijedi za oba spola, izbjegavati rod („Ulaziš u svijet…“, a ne „Dobro došao“; „Ne boj se“, a ne „Budi hrabar“).
- **Radnje igrača bez roda:** „{PLAYER} dobiva KARTU…“ (prezent) umjesto „je dobio/dobila“; „Opet ti ovdje?“ umjesto „Vratio si se?“.
- **Posvojnost uz dinamičko ime:** dvotočka ili zagrada umjesto genitiva. „Kuća: {PLAYER}“, „{X}: NAPAD raste!“, „{ABILITY} ({X}) sprječava otrov!“
- **Brojevi:** „Broj uhvaćenih: {STR_VAR_2}“, „{X} dobiva iskustvo: {N}!“ umjesto slaganja imenice s brojem.
- **POKéMON se sklanja** u fiksnom tekstu: POKéMONA, POKéMONI, POKéMONE, POKéMONIMA. U složenicama ostaje nesklonjen: POKéMON PROFESOR, POKéMON legenda.
- **Imena Pokémona, napada, abilityja i likova se ne sklanjaju** („tvoj izbor je VATRENI POKéMON CHARMANDER“, „{X} koristi TACKLE!“).
- **Mjerne jedinice:** metričke (m, kg). Provjeri podržava li kod metričke jedinice (europske verzije su ih koristile); ako ne, javi prije mijenjanja koda.
- **Širina retka:** provjeriti u pikselima da redak stane u prozor. Opisi tipki imaju 192 px, a dijaloški okvir najviše 202 px (najširi engleski redak).
- **Dijaloški okvir ima 2 retka:** prvi prijelom je `\n`, svaki sljedeći unutar iste stranice mora biti `\l` (pomakne tekst), nova stranica je `\p`.
- **Navodnici:** „ ne postoji u fontu, za sada se koriste “ ”.
- **Tri točke:** koristi znak … iz fonta, kao original.

## Pojmovi

| EN | HR | Napomena |
|---|---|---|
| POKéMON | POKéMON | ostaje |
| POKéDEX | POKéDEX | ostaje |
| TRAINER | trener | |
| POKéMON TRAINER | POKéMON TRENER | |
| GYM | GYM | ostaje |
| GYM LEADER | GYM LEADER | ostaje |
| ELITE FOUR | ELITE FOUR | ostaje, kao GYM |
| CHAMPION | PRVAK | |
| BADGE | BEDŽ | BEDŽA, BEDŽEVI, BEDŽEVE, osam BEDŽEVA |
| BOULDERBADGE itd. | BEDŽ BOULDER | uzorak „BEDŽ + engleski naziv“: BOULDER, CASCADE, THUNDER, RAINBOW, SOUL, MARSH, VOLCANO, EARTH |
| TEAM ROCKET | TIM RAKETA | sklanja se samo TIM: TIMA RAKETA, TIMU RAKETA; član je RAKETAŠ (RAKETAŠI) |
| POKé MART | POKé MART | ostaje |
| POKéMON CENTER | POKéMON CENTER | ostaje |
| POKéMON LEAGUE | POKéMON LIGA | sklanja se: POKéMON LIGE |
| PC | PC | ostaje |
| BOX | BOX | ostaje |
| PROFESSOR / PROF. | PROFESOR / PROF. | |
| MOM | MAMA | |
| LAB | LABORATORIJ | |
| AIDE | POMOĆNIK | |
| EGG | JAJE | |
| HELP | POMOĆ | |
| TM / HM | TM / HM | ostaje, opisi se prevode |
| Gramps | djed / Djede! | rival tako zove Oaka |
| Smell you later! | Vidimo se, papci! | rivalova uzrečica |
| whited out / blacked out | gubi svijest | „{PLAYER} gubi svijest!“ |

## Tipovi

- **U sučelju** (ikone tipova, sažetak, popis napada) nazivi tipova **ostaju na engleskom**. Velik dio su grafike, a kratki su i djeci poznati.
- **U dijalogu** se koriste hrvatski pridjevi, muški rod uz POKéMON:

| EN | HR |
|---|---|
| NORMAL | NORMALNI |
| FIRE | VATRENI |
| WATER | VODENI |
| GRASS | TRAVNATI |
| ELECTRIC | ELEKTRIČNI |
| ICE | LEDENI |
| FIGHTING | BORILAČKI |
| POISON | OTROVNI |
| GROUND | ZEMLJANI |
| FLYING | LETEĆI |
| PSYCHIC | PSIHIČKI |
| BUG | KUKČJI |
| ROCK | KAMENI |
| GHOST | SABLASNI |
| DRAGON | ZMAJSKI |
| DARK | MRAČNI |
| STEEL | ČELIČNI |

## Statusi i statistike

Kratice statusa (PAR, SLP, PSN, BRN, FRZ) i LV. **ostaju**, to su grafike. U tekstu:

| EN | HR | Primjer |
|---|---|---|
| paralyzed | paraliziran | „{X} je paraliziran!“ |
| asleep / fell asleep | spava / zaspao je | „{X} čvrsto spava.“ |
| poisoned | otrovan | „{X} je otrovan!“ |
| badly poisoned | teško otrovan | |
| burned | opečen | |
| frozen | smrznut | |
| confused | zbunjen | |
| fainted | se onesvijestio | „{X} se onesvijestio!“ |

| EN | HR | Napomena |
|---|---|---|
| HP | HP | ostaje |
| ATTACK | NAPAD | |
| DEFENSE | OBRANA | |
| SP. ATK | SP. NAPAD | |
| SP. DEF | SP. OBRANA | |
| SPEED | BRZINA | |
| ACCURACY | PRECIZNOST | |
| EVASIVENESS | IZBJEGAVANJE | |
| EXP. POINTS | iskustvo | „{X} dobiva iskustvo: {N}!“ |
| NATURE | NARAV | nazivi naravi: zasebna odluka kasnije |

## Borba

| EN | HR |
|---|---|
| Wild {X} appeared! | Pojavljuje se divlji {X}! |
| Wild / Foe {X} | Divlji {X} / Protivnički {X} |
| {TRAINER} would like to battle! | {TRAINER} te izaziva na borbu! |
| {TRAINER} sent out {X}! | {TRAINER} šalje {X}! |
| Go! {X}! | Naprijed, {X}! |
| {X}, come back! | {X}, vrati se! |
| {X} used {MOVE}! | {X} koristi {MOVE}! |
| It's super effective! | Vrlo je učinkovito! |
| It's not very effective… | Nije baš učinkovito… |
| It doesn't affect {X}… | Ne djeluje na {X}… |
| A critical hit! | Kritičan udarac! |
| {X}'s attack missed! | {X} promašuje! |
| But it failed! | Ali ne uspijeva! |
| {X}'s ATTACK rose! | {X}: NAPAD raste! |
| …rose sharply! | …naglo raste! |
| …fell! / harshly fell! | …pada! / naglo pada! |
| …won't go higher! | …ne može više rasti! |
| {X} grew to LV. {N}! | {X} dostiže LV. {N}! |
| Got away safely! | Uspješno bježiš! |
| Can't escape! | Ne možeš pobjeći! |
| {PLAYER} defeated {TRAINER}! | {TRAINER} gubi borbu! |
| {PLAYER} got ¥{N} for winning! | {PLAYER} dobiva nagradu: ¥{N}! |
| {PLAYER} is out of usable POKéMON! | {PLAYER} nema više POKéMONA za borbu! |
| It started to rain! | Počinje kiša! |
| The sunlight got bright! | Sunce jako sja! |
| A sandstorm brewed! | Diže se pješčana oluja! |
| It started to hail! | Počinje tuča! |

## Izbornici i sučelje

| EN | HR |
|---|---|
| MENU / SAVE | IZBORNIK / SPREMI |
| OPTION | POSTAVKE |
| EXIT | IZLAZ |
| NEW GAME / CONTINUE | NOVA IGRA / NASTAVI |
| YES / NO | DA / NE |
| CANCEL | ODUSTANI |
| FIGHT / BAG / RUN | BORBA / TORBA / BIJEG |
| BAG | TORBA |
| USE / GIVE / TOSS | KORISTI / DAJ / BACI |
| REGISTER | OZNAČI |
| TAKE / ITEM / MAIL | UZMI / PREDMET / PISMO |
| SUMMARY | SAŽETAK |
| SWITCH / SHIFT | ZAMIJENI |
| POKéMON INFO / SKILLS / MOVES | PODACI / VJEŠTINE / NAPADI |
| TEXT SPEED: SLOW / MID / FAST | BRZINA TEKSTA: SPORO / SREDNJE / BRZO |
| BATTLE SCENE: ON / OFF | ANIMACIJE: UKLJ. / ISKLJ. |
| SAVING… DON'T TURN OFF THE POWER. | SPREMANJE… NE GASI KONZOLU. |
| SEEN / OWN | VIĐENO / ULOVLJENO |
| HT / WT | VIS. / TEŽ. |
| Pokédex category (SEED, LIZARD…) | prevodi se jednom riječju: SJEMENKA, GUŠTER… |

Džepovi torbe:

| EN | HR |
|---|---|
| ITEMS | PREDMETI |
| KEY ITEMS | VAŽNO |
| POKé BALLS | POKé LOPTE |
| TM CASE | TM KUTIJA |
| BERRY POUCH | VREĆICA BOBICA |

## Itemi

- **Balli:** POKé BALL → POKé LOPTA, ostali po uzorku „naziv + LOPTA“.
- **Bobice:** BERRY → BOBICA, prva riječ ostaje engleska (ORAN BERRY → ORAN BOBICA).
- **Ostaju na engleskom:** ostali „Poké“ itemi (POKé FLUTE…) i jedinstveni ključni predmeti s vlastitim imenom (SILPH SCOPE…).
- **Prevode se:** generički predmeti. Paziti na maksimalnu duljinu imena predmeta u kodu.

| EN | HR | Napomena |
|---|---|---|
| POKé BALL | POKé LOPTA | ženski rod: POKé LOPTE, POKé LOPTU, POKé LOPTAMA, pet POKé LOPTI |
| GREAT BALL | SUPER LOPTA | |
| ULTRA BALL | ULTRA LOPTA | |
| MASTER BALL | MASTER LOPTA | |
| SAFARI BALL | SAFARI LOPTA | |
| POTION | NAPITAK | |
| SUPER POTION | SUPER NAPITAK | |
| HYPER POTION | HIPER NAPITAK | |
| MAX POTION | MAX NAPITAK | |
| FULL RESTORE | PUNI OPORAVAK | |
| REVIVE | OŽIVLJAČ | |
| MAX REVIVE | MAX OŽIVLJAČ | |
| ANTIDOTE | PROTUOTROV | |
| PARLYZ HEAL | ANTIPARALIZ | |
| AWAKENING | BUDILICA | |
| BURN HEAL | MELEM | za opekline |
| ICE HEAL | GRIJAČ | za smrzavanje |
| FULL HEAL | POTPUNI LIJEK | |
| ESCAPE ROPE | UŽE ZA BIJEG | |
| REPEL | REPELENT | |
| SUPER REPEL | JAČI REPELENT | |
| MAX REPEL | MAX REPELENT | |
| RARE CANDY | SUPER BOMBON | |
| FRESH WATER | SVJEŽA VODA | |
| SODA POP | GAZIRANI SOK | |
| LEMONADE | LIMUNADA | |
| TOWN MAP | KARTA | |
| OAK'S PARCEL | OAKOV PAKET | |
| BICYCLE | BICIKL | |
| OLD / GOOD / SUPER ROD | STARI / DOBAR / SUPER ŠTAP | |

## Klase trenera

Prevode se, kratko (provjeri `TRAINER_CLASS_NAME_LENGTH`). Ako ista klasa vrijedi za oba spola, odaberi oblik koji paše većini ili neutralan naziv.

| EN | HR |
|---|---|
| YOUNGSTER | DJEČAK |
| LASS | DJEVOJČICA |
| BUG CATCHER | KUKCOLOVAC |
| HIKER | PLANINAR |
| CAMPER | IZVIĐAČ |
| PICNICKER | IZLETNICA |
| SWIMMER | PLIVAČ |
| SAILOR | MORNAR |
| FISHERMAN | RIBIČ |
| BEAUTY | LJEPOTICA |
| GENTLEMAN | GOSPODIN |
| SUPER NERD | ŠTREBER |
| SCIENTIST | ZNANSTVENIK |
| BIKER | MOTORIST |
| CUE BALL | ĆELAVAC |
| JUGGLER | ŽONGLER |
| TAMER | KROTITELJ |
| BIRD KEEPER | PTIČAR |
| BLACK BELT | KARATIST |
| ENGINEER | INŽENJER |
| ROCKER | ROKER |
| GAMBLER | KOCKAR |
| CHANNELER | MEDIJ |
| PSYCHIC | VIDOVNJAK |
| BURGLAR | PROVALNIK |
| COOLTRAINER | SUPERTRENER |
| POKéMANIAC | POKéMANIJAK |
| TEAM ROCKET | TIM RAKETA |

## Napadi i abilityji

Imena ostaju na engleskom, opisi se prevode. Ideja: u opisu kratko navesti i hrvatski smisao imena, da ga igrač može vidjeti ako želi.

## Mjesta

- **Opća riječ ide ispred imena:** TOWN → GRADIĆ, CITY → GRAD, ROUTE → CESTA, ISLAND → OTOK… Vlastiti dio imena ostaje na engleskom i ne sklanja se. U rečenici se sklanja samo opća riječ: „u GRADU VIRIDIAN“, „iz GRADIĆA PALLET“, „na CESTI 1“.
- **Ime mjesta u varijabli** (`{STR_VAR_1}` i sl.): samo nominativ, s dvotočkom („Susret: {STR_VAR_1}“).
- **Ograničenja:** najviše 18 znakova (spremnik na karti) i 104 px (pregled špilje), odnosno 112 px (natpis pri ulasku). Izvor: `src/data/region_map/region_map_sections.json`.

| Engleski | Hrvatski | Napomena |
|---|---|---|
| PALLET TOWN | GRADIĆ PALLET | (prijedlog) |
| VIRIDIAN CITY | GRAD VIRIDIAN | (prijedlog) |
| PEWTER CITY | GRAD PEWTER | (prijedlog) |
| CERULEAN CITY | GRAD CERULEAN | (prijedlog) |
| LAVENDER TOWN | GRADIĆ LAVENDER | (prijedlog) |
| VERMILION CITY | GRAD VERMILION | (prijedlog) |
| CELADON CITY | GRAD CELADON | (prijedlog) |
| FUCHSIA CITY | GRAD FUCHSIA | (prijedlog) |
| CINNABAR ISLAND | OTOK CINNABAR | (prijedlog) |
| INDIGO PLATEAU | VISORAVAN INDIGO | (prijedlog) |
| SAFFRON CITY | GRAD SAFFRON | (prijedlog) |
| ROUTE 1 | CESTA 1 | (prijedlog) |
| VIRIDIAN FOREST | ŠUMA VIRIDIAN | (prijedlog) |
| MT. MOON | PLANINA MOON | (prijedlog) |
| S.S. ANNE | S.S. ANNE | (prijedlog) |
| UNDERGROUND PATH | PODZEMNI PROLAZ | (prijedlog) |
| DIGLETT'S CAVE | ŠPILJA DIGLETT | (prijedlog) |
| VICTORY ROAD | PUT POBJEDE | (prijedlog) |
| ROCKET HIDEOUT | SKROVIŠTE RAKETA | (prijedlog) |
| SILPH CO. | SILPH CO. | (prijedlog) |
| POKéMON MANSION | POKéMON VILA | (prijedlog) |
| SAFARI ZONE | SAFARI ZONA | (prijedlog) |
| POKéMON LEAGUE | POKéMON LIGA | (prijedlog) |
| ROCK TUNNEL | KAMENI TUNEL | (prijedlog) |
| SEAFOAM ISLANDS | OTOCI SEAFOAM | (prijedlog) |
| POKéMON TOWER | POKéMON TORANJ | (prijedlog) |
| CERULEAN CAVE | ŠPILJA CERULEAN | (prijedlog) |
| POWER PLANT | ELEKTRANA | (prijedlog) |
| ONE ISLAND | PRVI OTOK | (prijedlog) |
| TWO ISLAND | DRUGI OTOK | (prijedlog) |
| THREE ISLAND | TREĆI OTOK | (prijedlog) |
| FOUR ISLAND | ČETVRTI OTOK | (prijedlog) |
| FIVE ISLAND | PETI OTOK | (prijedlog) |
| SIX ISLAND | ŠESTI OTOK | (prijedlog) |
| SEVEN ISLAND | SEDMI OTOK | (prijedlog) |
| KINDLE ROAD | PUT KINDLE | (prijedlog) |
| TREASURE BEACH | PLAŽA BLAGA | (prijedlog) |
| CAPE BRINK | RT BRINK | (prijedlog) |
| BOND BRIDGE | MOST PRIJATELJSTVA | (prijedlog) |
| THREE ISLE PORT | LUKA TREĆEG OTOKA | (prijedlog) |
| SEVII ISLE 6 | OTOK SEVII 6 | (prijedlog) |
| SEVII ISLE 7 | OTOK SEVII 7 | (prijedlog) |
| SEVII ISLE 8 | OTOK SEVII 8 | (prijedlog) |
| SEVII ISLE 9 | OTOK SEVII 9 | (prijedlog) |
| SEVII ISLE 22 | OTOK SEVII 22 | (prijedlog) |
| SEVII ISLE 23 | OTOK SEVII 23 | (prijedlog) |
| SEVII ISLE 24 | OTOK SEVII 24 | (prijedlog) |
| RESORT GORGEOUS | RAJSKO ODMARALIŠTE | (prijedlog) |
| WATER LABYRINTH | VODENI LABIRINT | (prijedlog) |
| FIVE ISLE MEADOW | LIVADA PETOG OTOKA | (prijedlog) |
| MEMORIAL PILLAR | SPOMEN-STUP | (prijedlog) |
| OUTCAST ISLAND | OTOK IZGNANIKA | (prijedlog) |
| GREEN PATH | ZELENA STAZA | (prijedlog) |
| WATER PATH | VODENA STAZA | (prijedlog) |
| RUIN VALLEY | DOLINA RUŠEVINA | (prijedlog) |
| TRAINER TOWER | TORANJ TRENERA | (prijedlog) |
| CANYON ENTRANCE | ULAZ U KANJON | (prijedlog) |
| SEVAULT CANYON | KANJON SEVAULT | (prijedlog) |
| TANOBY RUINS | RUŠEVINE TANOBY | (prijedlog) |
| NAVEL ROCK | STIJENA NAVEL | (prijedlog) |
| MT. EMBER | PLANINA EMBER | (prijedlog) |
| BERRY FOREST | ŠUMA BOBICA | (prijedlog) |
| ICEFALL CAVE | LEDENA ŠPILJA | (prijedlog) |
| ROCKET WAREHOUSE | SKLADIŠTE RAKETA | (prijedlog) |
| DOTTED HOLE | RUPA S TOČKAMA | (prijedlog) |
| LOST CAVE | IZGUBLJENA ŠPILJA | (prijedlog) |
| PATTERN BUSH | ŠARENO GRMLJE | (prijedlog) |
| ALTERING CAVE | ŠPILJA PROMJENA | (prijedlog) |
| TANOBY CHAMBERS | ODAJE TANOBY | (prijedlog) |
| THREE ISLE PATH | STAZA TREĆEG OTOKA | (prijedlog) |
| TANOBY KEY | KLJUČ TANOBY | (prijedlog) |
| BIRTH ISLAND | OTOK ROĐENJA | (prijedlog) |
| MONEAN CHAMBER | ODAJA MONEAN | (prijedlog) |
| LIPTOO CHAMBER | ODAJA LIPTOO | (prijedlog) |
| WEEPTH CHAMBER | ODAJA WEEPTH | (prijedlog) |
| DILFORD CHAMBER | ODAJA DILFORD | (prijedlog) |
| SCUFIB CHAMBER | ODAJA SCUFIB | (prijedlog) |
| RIXY CHAMBER | ODAJA RIXY | (prijedlog) |
| VIAPOIS CHAMBER | ODAJA VIAPOIS | (prijedlog) |
| EMBER SPA | TOPLICE EMBER | (prijedlog) |
| CELADON DEPT. | ROBNA KUĆA CELADON | (prijedlog) |
| ROUTE 2…25 | CESTA 2…25 | (prijedlog) |

## Prijedlozi iz borbe i izbornika

| EN | HR | Napomena |
|---|---|---|
| Ally / Foe (cijela strana) | Tvoj tim / Protivnički tim | (prijedlog) „Protivnički tim: REFLECT prestaje djelovati!“ |
| {X}'s {ABILITY} / {ITEM} | {ABILITY} ({X}) | (prijedlog) posljedica u drugom retku, u nominativu |
| in love with {X} | Simpatija: {X} | (prijedlog) |
| GHOST (Pokémon Tower) | DUH | (prijedlog) |
| ANNOUNCER | NAJAVLJIVAČ | (prijedlog) |
| old man | starac | (prijedlog) |
| SAFARI GAME | SAFARI IGRA | (prijedlog) |
| COINS | ŽETONI | (prijedlog) „ŽETONI: {N}“ |
| MAILBOX | SANDUČIĆ | (prijedlog) |
| ITEM STORAGE | SPREMIŠTE | (prijedlog) |
| TRAINER CARD | KARTICA | (prijedlog) kod dodaje ime ispred: „RED: KARTICA“ |
| SPA | TOPLICE | (prijedlog) |
| BUY / SELL / SEE YA! | KUPI / PRODAJ / BOK! | (prijedlog) |
| WITHDRAW / DEPOSIT (PC) | UZMI / OSTAVI | (prijedlog) |
| BATTLE STYLE: SHIFT / SET | STIL BORBE: ZAMJENA / STALNO | (prijedlog) |
| {NATURE} nature. | Narav: {NATURE}. | (prijedlog) |
| MYSTERY GIFT, HALL OF FAME, DAY-CARE, ITEMFINDER, POKé FLUTE | ostaju | (prijedlog) |

Širine izbornika (provjereno u kodu):

- START izbornik: 48 px teksta (POSTAVKE je točno 48).
- DAJ / UZMI / ODUSTANI u ekipi: 48 px (ODUSTANI je točno 48).
- Poruke na dnu ekipe: 168 px; opisi poteza na terenu (CUT, FLY…): 144 px.
- Postavke: nazivi od x=8 do 130, vrijednosti od 130, najviše 70 px.

## Otvoreno (odlučiti kasnije)

- Nazivi naravi (HARDY, LONELY…)
- Zamjena za „ u fontu
