# Objekty

{::options auto_ids="true" /}
1. TOC_TEST
{:toc}

## Modelování

### Polygony

Je název pro způsob, jakým je valná většina objektů zapisována. Blender drží informaci o bodech a jejich spojích v prostoru. Body spojené tak, že mezi nimi vzniká stěna, se nazývají polygony. Blender tvoří tyto polygony vždy ze skupin právě tří spojených bodů. I krychle dodržuje toto pravidlo:

Má 8 bodů a každá strana je tvořena dvěma trojúhelníky. Ty se často přezdívají Tri \[traj\] (Tris \[trajs\] v množném čísle).

Blender toho mnohé skrývá a pro zjednodušení ukazuje strany klidně jako čtyř i více stěnné. Taková strana se nazývá Face \[fejs\]. Pod kapotou stejně ale funguje vždy za pomocí \[Tri\]. Toto může stěžovat některé úkony - jako například pokud chcete zvýraznit pouze to, co by normální člověk bral jako kostru této kostky. Standartní WireFrame nodou v materiálu je kostra kostky zvýrazněna právě tak, jako je na obrázku výše. ![A close up of a logo Description automatically generated](media/image18.png){width="1.3470538057742782in" height="0.27774278215223097in"} Tímto přepínáte styl zobrazení. Zleva je to Wireframe, kdy vidíte konstrukci jakoby drátěnou. Solid, což je klasický pohled, který již znáte. LookDev je odlehčený Render. Zobrazuje téměř stejně jako vykreslený obraz, ale používá zjednodušené osvětlení. Slouží spíše pro složité scény, které není praktické vykreslovat hned kvůli náročnosti nebo pokud váš projekt vyžaduje využití Cycles. Posledním je pak Rendered, neboli vykreslený styl, který zobrazuje scénu téměř jako vykreslenou.

### Cesty

Cesta je zvláštní typ objektu. Skládá se z několika mála bodů, mezi kterými vede vyhlazená čára, nemá tedy ostré hrany. U cesty typu Bezier, každým bodem prochází navíc úsečka definována dvěma dalšími body. Středový bod udává kudy cesta vede a přímky definují, jak má být Cesta vyhlazena.

Cesty se samy o sobě nezobrazují ve výsledném Renderu, ale mohou na ně být aplikovány různé věci. Jako například Bevel Modifikátor nebo naopak je na ně Modifikátorama a Omezovačema možné cílit. Například follow Path, který povede za nějakou dobu objekt po cestě.

### Sculpting

Sculpting neboli „sochařství" je alternativní způsob vytváření modelů. Tento způsob je méně přesný, ale běžně se používá pro vytváření postav nebo jakékoli aplikace, kde se pokoušíme dosáhnout jakési přírodnosti.

Sculpting také pouze upravuje mesh, takže je potřeba mít dostatečně kvalitní mesh (doporučuji pro toto Modifikátor multiresolution nastaven na Simple a po stisknutí tlačítka Subdivide se Vám zdvojnásobí počet stěn. Pokud máte problém s výkonem můžete snížit preview a nezobrazovat si jej v plné kvalitě až do renderu). Podobně, jako jsme probírali proporční editaci, je Sculpting vesměs podobný. Představme si ho jako pokročilou proporční editaci, u které máme mnohem specializovanější nástroje. Všechny tyto takzvané „štětce" mají velmi dobré popisky a náčrtky. V první záložce vlastností se Vám také zobrazuje nádherný piktogram a můžete zde nastavovat všechny možnosti daného štětce - jako sílu a velikost. Tato ikona vpravo nahoře znázorňuje menu symetrie. V základu je nastavena na symetrii v ose X.

Problémem je, že Sculpting často vytváří nečisté a moc složité meshe. Meshe vzniklé ze Sculptu se často předělávají, buďto tím, že se Scult Mesh bere jako předloha pro ručně vyrobený Mesh, nebo různými postupy, známé pod názvem Retopologizing, neboli Retopology. Toto je potřeba v branži dělat tak často, že na to vzniklo množství Add-onů, bezplatných i placených.

## Vzhled

### Render Engine

Výběr Render Enginu je velmi důležitý a silně závisí na druhu grafiky a její využití pro daný projekt. Render Engine je sada. Nyní rozeberme zabudované a pár stažitelných enginů, jejich výhody, nevýhody a využití.

#### EEVEE

V nové verzi Blenderu spolu s předchozími najdete také zbrusu nový EEVEE Engine - dříve pouze stažitelný doplněk. Roku 2019, v nové verzi 2.8, se stal hlavním enginem, na který je nastaven každý nově stažený Blender. První snadno poznatelný rozdíl - oproti předešlému standartu, je jeho násobná rychlost a ještě více nových možností a nastavení.

#### Cycles Render

Starší engine, který byl velmi dlouho používaný pro jeho jednoduchost a versatilitu. Kdokoli, kdo s ním pracoval, zná jeho hlavní nevýhodu, kterou je extrémně nízká rychlost. Před EEVEE se téměř nepoužíval jiný.

### Složení objektu

Zde se podíváme na to, co dává naší změti polygonů všechny vzhledové vlastnosti, kterými jsou například barva, lesk, průhlednost atd.

#### Mapy a UV Unwrap

Je více způsobů, jak dát objektu materiální vzhled. Prvním jsou tzv. Mapy. Fungují na jednoduchém principu - jako byste rozkládali papír. Každá mapa je prostý obrázek, jehož barva v každém pixelu spolu s tzv. UV unwrappem, dává počítači informaci o vzhledu daného objektu. Jako papírové tapety, které se snažíte dostat na kouli nebo sloup. UV Unwrap jsou instrukce, kde a jak střihnout, abyste tu placku dostali na 3D objekt.

Zde je možné upravovat, jak se aplikuje textura a vizualizovat objekty na 2D ploše.

Pokud máte v \[3D Viewport\] zvolený objekt v edit módu, promítne jeho rozložení sem. Nahoře si zvolíte obrázek, který se vám za rozložení promítne. Pokud ne, tak můžete jít dít do UV \> Smart UV Unwrap a rozložení se udělá za Vás. Toto rozložení lze volně editovat a změny se Vám budou promítat rovnou do scény.

Pokud chcete, aby se Vám nějaká část zafixovala a zůstala na stejném místě při automatickém rozložení, zvolte ji a stiskněte \[P\].

#### Textury

Textura je to, co dává objektu jeho barvu.

![IcoSphere-Texture0001](media/image19.png){width="1.2819444444444446in" height="1.2819444444444446in"}

Aplikují se v Shader Editoru především pomocí Nody Image Texture. To Vám vesměs stačí, ale pokud ji chcete ještě škálovat nebo s ní pohybovat, tak se před ní dává ještě Noda Mapping. V té mohu rotovat, škálovat a transformovat texturu dle libosti. Tato nastavení jsou dokonce rovněž animovatelná. Texture Coordinate je Noda, která za výstup dává současnou pozici něčeho na scéně. Generated výstup se často používá, protože Mapping je nejlepší způsob jak upravit pozici textury. V základu má ale všude nuly, což není ideál, protože tím plně rozhodí pozici textury, takže pokud do Vector napojím Generated z Texture Coordinate, tak Mapping bude vědět kam ji dát a změny se budou počítat proti její původní pozici, ne vůči nule.

Normál i dislokační mapa se používá stejně jako textura. Tedy stejné zapojení, ale akorát nahradím soubor otevřen v Nodě Textury. Vždy tu máme žlutý vývod, který nejčastěji bude veden do Base Color u Shaderu nebo Alpha, která se nejčastěji používá na Dislokaci a Color Ramp.

Informace o tom, jak je textura nebo cokoli jiného z Image Nody aplikována, se nachází v UV Unwrap. Blender má zabudovaných několik textur jako specifické Nody.

#### Normály

![Normal0001](media/image20.png){width="1.754488188976378in" height="1.0in"}![C:\\Users\\misa3\\AppData\\Local\\Microsoft\\Windows\\INetCache\\Content.Word\\Normal-Flat0001.png](media/image21.png){width="1.9116819772528435in" height="1.0737959317585302in"}![1024px-Normal\_map\_example\_-\_Map.png](media/image22.png){width="1.3541666666666667in" height="1.3541666666666667in"}

17\. Demonstrace Normály 18. Normál Mapa (Herzog, 2013)

Velmi často je zkrátka příliš složité nebo spíše výpočetně náročné vytvářet malé detaily pomocí modelování. Zde přichází na řadu normál mapa. Ta jednoduše říká programu, jak se má chovat světlo po nárazu na povrch objektu podle následující tabulky:

X: -1 až +1: Červená: 0 až 255

Y: -1 až +1: zelená: 0 až 255

Z: 0 až -1: Modrá: 128 až 255

Každý pixel v mapě obsahuje RGB data, o která se poté změní směr odrazu světla od očekávaných hodnot. Tedy odraz je pouze změněn oproti hodnotám již spočítaných programem. Tato změna trajektorie světla utvoří na objektu iluzi prostoru, hloubky a detailů za využití nepatrné výpočetní síly reagující i při změně světla a pohledu. Z tohoto důvodu se velmi často využívají ve hrách a jiných místech, kde je zapotřebí načítat a zobrazovat objekty velmi rychle. Jediný háček je samozřejmě fakt, že normál je pouze iluze, která se velmi rychle ztratí, především pokud je objekt prohlížen zblízka, pod velkým úhlem nebo pod špatným světlem.

##### Dislokace

Ve své podstatě dislokační mapa nese podobný výsledek jako normál mapa, ale dosahuje toho výrazně výpočetně náročnějším způsobem. Výhodou je, že efekt dislokace je „skutečný" a nikdy nedojde k jeho ztrátě pod vysokými úhly - jako u normál map. Mapa je černobílé vyjádření hloubky. Čím ***světlejší*** je pixel, tím vystouplejší bude bod na modelu.

#### Materiály

Pokud kreslení textur, map a normál není úplně pro Vás, můžete si práci ulehčit tím, že za Vás necháte vše dělat počítač. Materiál je soubor informací o tom, jak má vypadat povrch objektu. Vy pouze zadáte informace a zbytek za Vás může dopočítat a dotvořit, dynamicky a přizpůsobivě Blender. Blender je na materiálech tak založený, že i k aplikaci textury je třeba se s nimi setkat. Materiály fungují na tzv. Node systému.

![2019-04-13 (1)](media/image23.png){width="5.522916666666666in" height="2.377083333333333in"}

19\. Demonstrace Shader Editoru

Pro představu je Node v podstatě pracovník, co má jednu práci. Nějaká informace mu přijde, on s ní udělá X a pošle ji dál. V předešlém obrázku vidíme vlevo 3 čtverce - to jsou Nody a vpravo, co nám utváří. První Noda je Textura Vln (velmi jednoduchý matematicky daný vzor). V Blenderu je již jako samostatná Noda. Následuje Noda Difuzního Shaderu. Shaderové Nody jsou poslední a vlastně nejdůležitější část celku. Udává obecnou interakci světla s objektem. BSDF je zkratka pro matematickou funkci výpočtu dráhy světla. Pro naše účely to pouze znamená, že daná Noda je Shader - tedy převádí různé informace o lesklosti, barvě, průhlednosti, atd. na výstup. Příkladem Shaderu je skleněný, plně transparentní, lesklý, nelesklý a mnohé další. S EEVEE se nejčastěji používá tzv. „Principled BSDF", který většinu potřebných vlastností sjednotil do jednoho Shaderu s vysokým množstvím nastavení. V závěru se nachází Materiální Výstup. Poté, co provedete všechny potřebné operace, napojíte sem výstupy a ty jsou poté zobrazeny na Vašem objektu.

Možná jste si všimli různých zabarvení vstupů a výstupů. Ty mají důležitý význam pro zapojitelnost. Překvapivě Blender je schopen brát barvy jako vektor a provádět matematické operace na texturách. Je ale důležité vědět, co přesně máte za výstup, abyste s ním mohli dobře pracovat.

Tabulka Barev (gandalf3, 2015):

  Barva     Typ         Zapojitelnost (Případně úprava dat provedena při daném zapojení)
--------- ----------- ------------------------------------------------------------------
  Šedá      Číslo       Fialová a Žlutá (všechny tři hodnoty jsou tím samým číslem)
  Žlutá     RGB         Fialová, Šedá (konvertuje na BW)
  Fialová   3D Vektor   Žlutá, Šedá (konvertuje na BW)
  Zelená    Shader      Pouze zelená

Možná Vás překvapilo napojení celé textury pouze pomocí jednoho RGB výstupu. Nesmíte nikdy zapomenout na dosti abstraktní koncept, že každá informace v Shaderu platí vždy pro daný bod na objektu. Takže většinou vedu pouze jedno číslo, i když mám 3D objekt s obrovským množstvím bodů, na každý z nich se vztahuje právě ta jedna daná informace, kterou vedu.

**Volume** -- Materiál nemá pouze povrch ale také obsah. Ten funguje úplně identicky k Povrchu. V materiálním výstupu je druhou položkou právě Volume. Do něj se zapojují Volume Shadery.

**Subsurface Scattering --** Název pro světlo odrážející se uvnitř objektu. Nejčastěji se ukazuje pomocí svíček, kdy oheň z nich mírně prosvěcuje skrze vosk a září i na části, které by měly být plně odstíněné. Slabý Subsurface Scattering se používá i pokud chcete udělat rozumně vypadající materiál pleti.

Když přidáte nový materiál tlačítkem + napravo od seznamu Materiálů, můžete buď vytvořit Nový nebo kliknout nalevo od tlačítka New na ikonu materiálu, kde si můžete vybrat kterýkoli existující. Materiál takto přebraný je stejný u všech objektů, které jej využívají. Tedy pokud změním u jednoho nastavení Nody, v ostatních to bude stejné. Tam, kde bylo původně tlačítko New, je nyní název materiálu. Napravo od názvu jsou tři tlačítka. První zaručí uložení Materiálu i přesto, že jej nevyužívá žádný objekt. Druhé udělá novou kopii materiálu, takže pokud jste měli dříve jeden materiál ve dvou objektech a jeden z nich potřebujete změnit nezávisle na druhém. Třetí odstraní Materiál.

Když máte více materiálů v jednom objektu, můžete definovat, které stěny používají který. Pokud chcete přiřadit stěně Materiál, jděte do Edit módu a se zvolenými stěnami stiskněte tlačítko Assign.

## Pohyb

### Key-framing

Key-Framing se skládá ze dvou slov. Key tedy klíč a frame tedy snímek. Tzv. klíčové snímky se používají v celé animaci pro udání všeho, co si můžete představit. Snímek v Blenderu je jedna animační časová jednotka a do každé z těchto jednotek můžete zapsat nějaké dané úkony, „klíče". Tyto úkony jsou Blenderem brány jako osnova co v té chvíli má provést. V základu se používá 24 snímků za vteřinu, ale můžete si nastavit kolik je potřeba. Je však nutné upozornit, že zvýšením množství snímků za vteřinu se zrychlí vaše animace. Rychlost animace je totiž vázána na snímky a ne na čas. Do snímku lze zapsat libovolný počet klíčů - tak se nazývá informace o výši hodnoty v daném čase. Tato informace může být jakákoliv - od pozice objektu, až po jeho naklonění, aktivní kamery, dokonce i pózy postav a síly světel. V podstatě vše, co Vás napadne se dá keyframovat. V časové lince se keyframe vyznačuje jako žlutý bod. Vidět jsou pouze \[Keyframe\] zvolených objektů. Přidávají se buďto stisknutím pravého tlačítka myši na danou hodnotu nebo klávesou \[I\] v Objektovém módu okna 3D zobrazení. Ta Vám otevře menu, ve kterém máte na výběr veškeré Keyframeovatelné hodnoty zvolených objektů.

Napravo Start a End udává, v jakém úseku bude probíhat animace. Toto se vztahuje pouze na Render a zobrazení. Pokud necháte spočítat nějakou simulaci, má vlastní nastavení časových úseků.

### Kosti -- Rigging

Animovat zvlášť každý polygon by bylo peklo a právě k tomu slouží Rig. Skládá se z článků zvaných kosti. Každý polygon má nyní přidělené kosti a místo animování stovek polygonů můžeme říct pouze: „Pohni kyčlí." nebo v pokročilejších programech i: „Zvedni ruku." či dokonce „Poskoč a zamávej.". V herních enginech se používají většinou knihovny pohybů, které se aplikují na standardizovanou kostru u které je možné vyměňovat Mesh, takže jedna animace je možná použít pro více postav.

**Armature** -- neboli kostra, je objekt, který slouží k udání ohybu a pohybu jiného objektu. Po vytvoření Armatury zvolte objekt, který chcete Armaturou ovládat a přidejte mu modifikátor Armatura s tím, že nastavíte jako zdroj armaturu. Armatura má svůj vlastní mód vedle editačního a objektového, a tím je mód pózový. V něm nastavíte pózu, kterou v daném snímku chcete a uložíte celou pózu jako Keyframe tlačítkem „Whole character". Objekt, který má tento modifikátor, se poté následně bude deformovat tak, aby co nejblíže odrážel pohyb kostry. Další části kostry neboli tzv. kosti lze přidávat extrudováním \[E\]. Kosti lze upravovat jak celé, tak za konce. Počítají se jako vertexy a strany a přepíná se mezi nimi stejným způsobem.

### Fyzikální simulace

Překvapivou a velmi užitečnou schopností jsou simulace. Blender má velmi výkonné fyzikální simulace, přestože jsou samozřejmě zaměřeny na grafickou stránku a nemají sloužit jako přesné modely. Ale oheň, kouř, vlasy, látky i kapaliny, to vše se dá simulovat.

#### Rigid Bodies

Rigid Body je v 3D grafickém žargonu standartní pevný předmět. Nastavení Dynamic určuje, zda se tento objekt pohybuje při Vaší animaci. Takže se vypíná například u podlahy a stěn. Pokud je Animated vypnutý, objekt ignoruje všechny své \[keyframe\]. Výpočet kolize dvou předmětů však není úplně jednoduchá záležitost, a tak pod Collisions \> Shape můžeme zvolit jakým způsobem se dá tento problém zjednodušit. V základu je toto nastaveno na Konvexní Mesh, takže pokud Vám nevychází simulace, zkuste toto změnit na Mesh.

#### Kapalina

Typů objektů účastnících se simulací kapalin je několik:

**Doména** -- V objemu tohoto objektu se odehrává celá simulace. Jeho shell slouží jako hranice, za kterou kapalina nemůže jít. Materiál tohoto objektu je materiál, který bude použit pro kapalinu. Resolution mění kvalitu kapaliny. **Pozor** - Čas začátku a konce simulace je ve *vteřinách*.

V neposlední řadě je třeba stisknout tlačítko **Bake**. To řekne Blanderu, aby s tímto nastavením spočítal Vaši simulaci. Pokud dojde k nějaké změně, musíte nechat simulaci opět přepočítat.

**Kapalina** -- Tento objekt slouží jako počáteční objem kapaliny.

**Překážka** -- Vyznačuje, že s tímto objektem interaguje kapalina jako se solidní překážkou.

**Inflow a Outflow** -- Tudy kapalina vtéká a vytéká.
