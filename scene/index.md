# Scéna

{::options auto_ids="true" /}
1. TOC_TEST
{:toc}

## Světlo

Na počítači se bez něj obejít můžeme, ale Blender a většina jiných grafických programů, s ním v základu pracuje. Za účelem realizmu používáme tzv. RayTracing. Toto znamená, že počítač simuluje reálné chování světla zjednodušeným modelem. Spočítá čáry od každého zdroje světla a sleduje, kam dopadnou a jak se odrazí. Podle toho zjišťuje a nastavuje světlost daných bodů na povrchu. Pokud používáme RayTracing, každý povrch obsahuje nějakou informaci o tom, kolik světla pohltí (vlastní světlost), kolik ho odrazí (lesklost), atd. O tom v kapitolách objekty, nyní si spíše probereme trochu názvosloví.

### Typy světel

**Point (Bod) --** Vesměs žárovka

**Sun (Slunce)** -- Nyní trocha abstrakce. Slunce, aby mělo správný druh světla, musí ležet velmi vzdáleně. Slunce v Blenderu se počítá jako nekonečně daleký a nekonečně velký zdroj světla. Takže paprsky dopadají na scénu rovnoběžně, jdoucí po směru polopřímky zaznačené u objektu Slunce. Můžete si to představit jako obrovské stadionové světlo.

**Spot --** V podstatě se jedná o baterku. Je to kužel světla. Pod nastavením Spot Shape můžete nastavit Size, což mění šířku paprsku a Blend, určující rychlost tlumení světla na okrajích - tedy jakési jeho rozptýlení.

**Area (Plocha) --** Slunce akorát malé a usměrněné. Vydává rovnoběžné paprsky světla z plochy definované uživatelem.

### Ambient Occlusion \[AO\]

Velmi důležitá věc při pokusech o realistické rendery. Ambient occlusion je název pro odraz světla od každého objektu kolem nás. Při jeho absenci se světlo chová špatně a vypadá nereálně. Například pokud přiblížím ruku ke stěně, tak nejenom na ní vytvořím tmavší místa svým stínem, ale také se nějaká část světla odrazí od mé ruky a udělá opět jiná místa světlejšími nebo tmavšími. Tyto odražené paprsky se nazývají Ambient Occlusion.

(PlayCanvas)

### Fresnel

\[Frenel\] Tímto se myslí optická vlastnost, při které se od povrchů rovnoběžných s okem odráží do oka méně světla nežli od nakloněných. Nejlépe demonstrováno na takovéto kouli:

Čím bělejší, tím více světla se odráží.

### IOR (Index Lomu)

![](media/image24.png){width="3.3006135170603677in" height="1.9503630796150482in"}

(Cddwumich, 2011)

Každý průhledný předmět má tzv. Index Lomu. V Blenderu je užívána zkratka IOR (Index Of Refraction). Tato hodnota je definována jako poměr rychlosti světla ve vakuu k jeho rychlosti v daném materiálu. Co toto znamená, je, že světlo je zakřiveno ve chvíli, kdy přechází mezi hranicemi materiálů. Sílu a směr tohoto zakřivení definujete tedy jedním číslem. Pro představu můžete otevřít jakékoli fyzikální tabulky a najít si hodnoty pro všemožné materiály. Standartní sklo má většinou IOR okolo 1.45.

## Vykreslování (Rendering)

Dnešní výpočetní síla neumožňuje všechny vizuální efekty zobrazovat v reálnem čase. Tzv. Render bere vaši scénu a zpracuje tyto informace do obrazového výstupu, přehratelného na každém normálním zařízení. Vedle souboru 3D modelu je toto nejčastější výstup.

### Nastavení

Navrátíme se nyní ke kapitole Vlastnosti a popíšeme si, jaká nastavení jsou k této tématice relevantní.

#### Bloom

20 - Světlo s Bloom 21 - Světlo bez Bloom

Slouží k reprodukci efektu se stejným názvem nalézajícího se v kamerách. Jedná se o efekt, při kterém světlo o dostatečné intenzitě začne přetékat daleko za své obvyklé rámce. V našich očích přirovnatelný k oslnění. Avšak některé kamery se neumí přenastavit nebo snímají právě vnitřní scénu, a tak může tento efekt být i trvalý.

Co se týče nastavení. Threshold udává, jak jasné světlo musí být, aby mohlo začít vyvolávat tento efekt. Radius a Intenzita udávají plochu a potentnost efektu. Clamp udává tvrdý strop nad který už tento efekt nebude zobrazován - ať už bude světlo jakkoliv silné, jeho Bloom bude snížen na jednu fixní hodnotu. Pokud je Clamp 0, tento limit je nekonečně vysoký.

#### Screen Space Reflections

Blender 2.8 předělal kompletně způsob, kterým funguje lesk a průhlednost. Přidal masivní množství pokročilých možností, které umožňují tuto výpočetně velmi náročnou operaci zjednodušit až do úrovně Real-Time (Vteřina snímků se vykresluje rychleji než vteřinu).

22\. Lesk pomocí Gloss 23. Lesk pomocí Odrazové plochy

Standartní způsob býval nastavit materiál na Lesklý, nastavit hrubost lesku, a to bylo vše. Druhou možností v dnešní době jsou odrazové objekty. Pod menu přidání objektu jsou uvedeny jako Light Probe. Reflection plane a reflection cubemap si jsou velmi podobné. Dělají vesměs to samé. Pouze plane to dělá v jednom směru a cubemap je kostka, která tyto efekty bere ze všech směrů. Takovouto odrazovou plochu umístíte mezi to, co chcete odrazit a Váš objekt. Toť vše. Blender se o zbytek postará.

#### Motion Blur

Motion blur je opět efekt replikující chování našich očí. Způsobuje, že pohyb je rozmazaný. Protože vykreslovací systém Blenderu nemusí mít žádné informace o pohybu a s touto možností vypnutou skutečně vykreslí každý snímek jako dokonale ostrý statický obraz. Se zapnutou bude brát v potaz rychlost a pohyb objektů v obraze, a příslušně je bude rozmazávat. Což vypadá realističtěji a v dynamických scénách obecně i lépe. Vaše scéna začíná na snímku 1, takže pokud chcete, aby Váš první snímek již Motion Blur obsahoval, musíte jeho začátek nastavit na snímek 0.

![A picture containing building, bus, street, road Description automatically generated](media/image25.jpeg){width="2.643021653543307in" height="1.7633912948381452in"}

(E01, 2008)

#### Volumetric

Zapíná a vypíná vykreslování obsahových (anglicky. volume) shaderů. Při tvorbě materiálů máte tři výstupy, kdy druhý z nich je právě Volume. Toto nastavení je buďto vypíná nebo zapíná nebo nastavuje, jak daleko nebo blízko od kamery by mělo jejich vykreslování začít a skončit.

### CPU vs. GPU

GPU je na vykreslování obrazu doslova dělané. Pokud má Vaše grafická karta některý ze systémů, které Blender podporuje, bude ji moct velmi dobře využít. Klíčová slova, která hledáte, pokud chcete zjistit, jestli daná karta tyto systémy má, jsou CUDA a OpenCL. Samozřejmě je nejlepší najít tabulky a reference pro skutečnou jistotu. Pokud není možnost se k takové kartě dostat, není to problém. Vaše CPU zvládá vše, co umí karta, pouze mírně pomaleji. Tento rozdíl je v Blenderu 2.8 výrazně nižší.

### Další možnost -- Renderfarmy

Renderfarma je koncept, kde někdo jiný renderuje Vaše obrazy za Vás. Je několik způsobů, jak takovouto externí pomoc získat. Samozřejmě si ji lze zaplatit. Ceny se mohou odvíjet například od množství snímků, hodin, nebo množství výpočtu. Druhou možností jsou komunitní renderfarmy. Fungují na stejném principu, pouze platíte částí své výpočetní síly, kterou zrovna nepoužíváte, namísto penězi. Na Vašem počítači necháte spuštěn software takové farmy, který v dobách, kdy Váš hardware není pod zátěží, stahuje projekty jiných lidí a malinké kousíčky zpracuje. Později, když potřebujete Vy vykreslovat, rozdistribuuje se Váš projekt na stovky takovýchto neaktivních počítačů. Je to vzájemné propůjčení nepotřebné síly. Velkým háčkem je, že některé cizí počítače budou mít rozdílný hardware od toho Vašeho. To může způsobit malé nebo zásadní rozdíly ve výsledném vzhledu. Především pokud si dostatečně nehlídáte nastavení.

### Perspektivy

Říká, zda mají objekty být větší čím jsou bližší. Pokud toto nastavíte na ortografické, dva stejně velké objekty budou stejně velké, ať jsou jakkoli daleko. Ztrácí se perspektiva a kamera je jakoby bez čočky, jenom zaznamenávající plátno. Pro lepší představu je přiložen obrázek.

(Kuiper, 2008)

Přepínat mezi těmito perspektivami můžete buďto v nastavení kamery nebo pro viewport klávesou \[5\].