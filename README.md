# mistecky_zvakova_nr_sas
Repozitář obsahuje finální terminologické hesláře, výsledky kvantitativních analýz a grafické výstupy výzkumu zaměřeného na zastoupení versologické a kvantitativnělingvistické terminologie v časopisech Naše řeč a Slovo a slovesnost v letech 1935–1943.

# Obsah repozitáře

## `grafy/`
- `01_BM25_boxplot.tif` – krabicový graf BM25 včetně odlehlých hodnot.
- `02_BM25_percentily_QL28.tif` – percentily BM25 pro QL28.
- `03_BM25_percentily_V230.tif` – percentily BM25 pro V230.
- 
## `heslare/`
- `QL28.txt` – 28 lemmat charakteristických pro kvantitativní, korpusovou a komputační lingvistiku.
- `V230.txt` – 230 versologických termínů.

## `vysledky/`
- `BM25_po_textech.txt` – BM25, četnosti a délky textů pro oba hesláře (2 660 řádků).
- `DIN_QL28.txt` – četnosti, relativní četnosti a DIN pro 28 lemmat QL28.
- `DIN_V230.txt` – četnosti, relativní četnosti a DIN pro 69 doložených položek V230.
- `logisticka_regrese_souhrn.txt` – společný souhrn dvou regresních analýz.
- `logisticka_regrese_predikce.txt` – modelové predikce pro oba hesláře (2 660 řádků).
- `zanry_nad_P75.txt` – zastoupení rubrik u textů nad 75. percentilem BM25.

## Zkratky a označení

- **NŘ / NR** – *Naše řeč*; **SaS** – *Slovo a slovesnost*. Podoba `NR` bez diakritiky se vyskytuje v názvech některých sloupců.
- **QL28** – heslář 28 lemmat kvantitativní, korpusové a komputační lingvistiky; **V230** – heslář 230 versologických položek.
- **TF** (*term frequency*) – celkový počet výskytů sledovaných termínů v textu; v souborech DIN počet výskytů konkrétního termínu v daném časopise.
- **TTB** – počet různých položek hesláře doložených v textu (bez ohledu na jejich opakování).
- **RF** (*relative frequency*) – relativní frekvence termínu; `RF_1000` je četnost na 1 000 analyzovaných jednotek. U versologických výpočtů se délka upravuje tak, aby víceslovný terminologický výskyt představoval jednu jednotku.
- **DIN** – diferenční index vypočtený z relativních frekvencí v NŘ a SaS; kladné hodnoty označují relativní převahu v SaS, záporné v NŘ (rozmezí −100 až +100).
- **BM25** (*Best Matching 25*) – skóre terminologického zastoupení textu se saturací opakovaných výskytů a délkovou normalizací; `bez_IDF` znamená variantu bez vážení podle vzácnosti termínů. **IDF** = *inverse document frequency* (inverzní dokumentová frekvence).
- **N** – délka analyzovaného textu (počet tokenů); **n** – počet textů; `median` = medián; `pos` = binární příznak přítomnosti alespoň jednoho termínu (0 = ne, 1 = ano).
- **pred** – pravděpodobnost výskytu termínu předpovězená logistickým modelem pro skutečný časopis textu; `pred_NŘ_stejna_delka` a `pred_SaS_stejna_delka` jsou predikce pro oba hypotetické časopisy při nezměněné délce.
- **beta** (β) – regresní koeficient; `beta_delka` se vztahuje k logaritmu délky, `beta_casopis_SaS` k příslušnosti k SaS.
- **OR / odds_ratio** (*odds ratio*) – poměr šancí na výskyt termínu v SaS oproti NŘ při zohlednění délky.
- **CI95** (*95% confidence interval*) – 95% interval spolehlivosti; `low` / `high` označují dolní / horní mez; `model` = interval z regresního modelu, `boot` = interval z bootstrapu (opakovaného převzorkování).
- **p** – p-hodnota statistického testu; **Wald** – Waldův test; **LRT** (*likelihood-ratio test*) – test poměrem věrohodností.
- **stand** – délkově standardizovaný modelový podíl (marginální standardizace); **pp** – procentní body; **AIC** (*Akaike information criterion*) – Akaikeho informační kritérium.
- **P75** – 75. percentil BM25 u textů s alespoň jedním výskytem; `n_nad_P75` je počet textů nad touto hranicí.

Tabulkové TXT používají tabulátory jako oddělovače sloupců a kódování UTF-8 s BOM (pro správné zobrazování české diakritiky ve Windows).

