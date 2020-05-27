# Interface

Blender se svou rozmanitou funkčností snaží poskytnout co nejvíce možností a do toho je musí udržet přístupné a přehledné. K tomuto využívá systém oken, o kterém si nyní něco můžeme říct.

Když poprvé spustíte Blender, tak vypadá následovně.

![UI-1.png](media/image4.png){width="6.147998687664042in" height="3.256517935258093in"}

4\. Po spuštění

Nejlépe je si přirovnat systém Blender k oknům u Vašeho počítače. Tak, jak máte na počítači otevřena mnohá okna vedle sebe (např.: prohlížeč, Word, mail atd.), stejně tak je to u Blenderu. Blender jako program má nespočet různých funkcí, které by byly absolutně nepochopitelné, kdyby byly ukázány všechny najednou. Proto jsou nástroje uvedeny do souvisejících oken, kdy každé z nich má sloužit k jednomu účelu - například okno pro umístění objektů do scény, okno pro jejich nastavení, okno pro editaci videa, okno pro práci s texturami atd.

![UI-1.png](media/image5.png){width="6.060199037620298in" height="3.2100120297462817in"}

5\. Po spuštění (obarvené)

Sledujme nyní obrázek 5. Modře je zaznačeno takzvané 3D zobrazovací okno, ve kterém budete pravděpodobně trávit nejvíce času. Zeleně je zvýrazněna Ćasová osa, která se používá hlavně při animacích. Napravo je červeně většina nastavení. Žlutě je Seznam objektů a skupin. Nakonec vršek lemuje informační panel, který obsahuje většinu ukládání, otvírání souborů a také se zde zobrazují procesy na pozadí jako vykreslování a fyzikální simulace.

**Pohyb s okny** -- Pokud najedete myší mezi dvě okna změní se Vám kurzor a můžete měnit jejich velikosti. Najetím na roh okna, kde se vám kurzor změní na kříž, je možné okna zavřít nebo otevřít.

Obsah okna lze změnit v malém menu obsaženém v každém z oken. Na začátku jsou nejlépe vidět dva v obou rozích levé strany programu. Poznají se podle obrázku, vedle nějž se nachází šipka dolů. Po kliknutí na toto menu se Vám otevře výběr všech druhů oken, které si nyní projdeme.

![UI-WINDOWS.png](media/image6.png){width="6.023389107611549in" height="2.0337576552930883in"}

6\. Výběr oken

## 3D Zobrazení

Zde budou Vaše oči trávit nejvíce času. Okno 3D zobrazení Vám zobrazuje celou scénu. Můžete v něm nejjednodušeji přepínat mezi objekty, modelovat je, pohybovat a točit s nimi. Také se Vám zde promítnou veškeré změny z jiných oken. Dále v něm můžete nahlížet do kamer a vidíte v něm, jak vypadá Vaše scéna.

K pohybu v 3D zobrazení slouží nejlépe numpad. Klávesy 4, 8, 6 a 2 otáčí kameru kolem aktuálního středu. Stejný pohyb je dosažitelný přidržením kolečka myši. 1, 7 a 3 nastaví pohled dle globálních os - přesně na pohled shora, ze strany nebo zepředu. 9 invertuje pohled o 180°, takže pohled zepředu otočí na pohled zezadu. K přiblížení a oddálení pohledu slouží Klávesy \[+\] a \[-\] nebo kolečko myši.

Klávesa \[Shift\] změní 4 a 6 na klávesy otáčející pohled ze strany na stranu, jako byste nakláněli hlavu. \[Ctrl\] změní všechny směrové klávesy tak, aby posouvaly pohled ze strany na stranu, bez rotace.

### Módy

Uvnitř tohoto okna se nalézá několik módů. Nejdůležitější z nichž jsou objektový a editační. Tyto dvě možnosti máme oddělené a přepínáme mezi nimi stisknutím klávesy \[Tab\]. Další módy jsou přístupné z menu v levém horním rohu.

#### Objektový

Tento mód slouží především k pohybu objektů a jako mezikrok k dalším módům a oknům. V objektovém módu můžete libovolně zvolit kterýkoliv objekt, který poté v dalších módech a oknech budete editovat, protože všechny ostatní módy vždy pracují pouze s tímto jedním zvoleným objektem.

Objekt zvolíte stisknutím levého tlačítka myši kdekoli na něm.

Pokud chcete zvolit více objektů najednou, přidržte k jejich volbě \[Shift\].

7\. Transformovaná Kostka (translace, rotace, škálování)

**Zvolení objektů** - Žlutým okrajem je zvýrazněn zvolený objekt. Ten je zobrazován a upravován v ostatních oknech. Oranžově jsou zvýrazněny další zvolené objekty, na které se také budou aplikovat translace nebo seskupování či další hromadné úpravy. Hlavním zvoleným objektem je vždy objekt, který byl do výběru přídán jako poslední. Blender referuje ke všem zvoleným objektům jako Selected a k hlavnímu zvolenému objektu jako active. Klávesou \[,\] zacentrujete pohled na zvolené objekty.

8\. Volba objektů

**Pohyb** - Zde se rovnou hodí zmínit o klávesových zkratkách, těch má Blender nespočetně, ale nyní jich budeme využívat jen několik. Nebojte, bude to jednoduché.

  G   translace
--- -----------
  R   rotace
  S   rozměr

Poté, co jste zvolili, co chcete s objektem dělat, můžete říct přímo ve kterém směru. Tím, že stisknete jednu klávesu korespondující k jedné z os \[X, Y, Z\], změna se bude projevovat pouze na té ose. Pokud stisknete klávesu ještě jednou, tak zvolíte lokální osu namísto globální. Další stisknutí osu opět odemkne.

Jsou tři osy pohybu - podle toho, k čemu jsou tyto osy kolmé, je dělíme především na lokální a globální. Lokální osa zahrnuje předešlé změny. Například krychle zobrazena níže má lokální osu X o 45 stupňů odkloněnou od globální osy X. Globální jsou totiž stacionární a vždy zůstávají stejné, osy X a Y jsou rovnoběžné s čárami zaznačenými kolem objektů, osa Z je na obě kolmá.

Pokud chcete změnu provést o specifickou hodnotu, můžete ji napsat na klávesnici. Všechny změny se potvrzují levým tlačítkem myši a ruší se pravým.

Příklad:

9\. Ukázka rotace

Když mám zvolený objekt, stisknu R, napíšu 45 a stisknu Z. Krychle se mi otočí, jak vidíte výše, o 45 stupňů dle svislé osy Z.

10\. Informace o změně

Vlevo nahoře poté máme informace o současné probíhající změně, pokud ji chcete dodatečně měnit. Hodnotu lze dokonce standartně přepisovat klávesou \[Backspace\] a šipkami. Změna se potvrdí klávesou \[Enter\] nebo levým tlačítkem myši. Vráti lze klávesou \[Esc\] nebo pravým tlačítkem myši.

Nové objekty lze přidávat z menu dostupného klávesovou zkratkou \[Shift+A\].

![](media/image7.png){width="0.5889566929133858in" height="1.0539206036745408in"}

11\. Výběr/3D Kurzor Spínač

**3D Kurzor** - Vlevo vidíte tento spínač, pokud je nastaven na spodní hodnotu, levé tlačítko myši namísto volení objektů, začne přemisťovat tzv. 3D Kurzor. Tento kurzor slouží k pár účelům. Jednak je to místo, kde se objevují nově přidané objekty, ale především slouží jako arbitrární přemístitelný bod v prostoru. Pomocí menu na zkratce \[Shift+S\] můžete přemístit 3D Kurzor na nějaké specifické místo nebo přemístit objekt na 3D Kurzor.

**Origin** -- neboli počáteční bod, vyznačen na objektech malou žlutou tečkou, určuje jakousi jednotnou definici pro daný objekt. Protože objekt je často složen i ze stovek bodů, je potřeba jeden jasný bod, ke kterému lze referovat - například při zapisování jeho pozice. Pokud nahlédnete do vlastností objektu, vidíte zde pouze souřadnice jediného bodu, definující pozici celého objektu - tímto bodem je právě pivotový bod. Všechny transformace se také provádí se středem v pivotovém bodu, pokud není řečeno jinak. Nejlépe se nastavuje v menu Object \> Set Origin.

Na vrchu okna poté máte několik dalších nástrojů. Nejdříve popišme ty uprostřed.

**Pivotovým bodem** - (Pivot point) se rozumí bod, vůči kterému jsou prováděny operace.

![A screenshot of a cell phone Description automatically generated](media/image8.png){width="1.8799464129483814in" height="2.08882874015748in"}

12\. Menu pivotového bodu 13. Ukázka pivotového bodu

Například výše byly umístěny dvě krychle, jedna nalevo a jedna napravo, od středu na stejnou úroveň. Obě byly otočeny o 45°, ta vlevo kolem Originu a ta napravo kolem 3D Kurzoru.

**Snap** - Další je menu něčeho nazývané Snap. Nejlépe by toto bylo přeloženo jako záchytné body. Magnetem se zapíná a vypíná, napravo vybíráte na co se změny chytají. Pokud máte například zapnutý Snap na Face, tak kdykoli provádíte změnu, například přemisťujete objekt, a vaše myš narazí na jakoukoli stěnu, objekt se na ni přichytí. Většinou to provede tak, že jeho nejbližší bod nastaví přesně na daný záchytný bod.

**Proporční editace** - Při standartní editaci jsou ovlivněny pouze zvolené části (první obrázek níže), ale to často není co potřebujete. Proporční editace je vcelku jasná z názvu - ovlivňuje i nezvolené části meshe, silou odvíjející se dle jejich vzdálenosti od zvolených částí meshe. Pro zvětšení nebo zmenšení ovlivněné části točíte kolečkem myši. „Connected only" bude ovlivňovat pouze části meshe, které jsou direktně spojené se zvolenými částmi. „Projected from view" určuje střed, od kterého se počítá vzdálenost, a následně tedy i síla změny pro daný bod. Pokud je vypnutý, změny se odvíjí od standartního středu definovaného pivotovým bodem. Pokud je zapnutý, střed je nejlépe popsán jako polopřímka začínající z místa vašeho pohledu a procházející pivotovým bodem.

14\. Proporční editace (Bez, s, změna velikosti)

**/** - Lomítkem schováte všechny nezvolené objekty. Opětovným stisknutím je pak zase zobrazíte.

#### Editační

Zde - namísto editování celé scény, máte možnost zvlášť upravovat zvolený objekt včetně meshe. Zde můžete nastavovat i související věci jako \[Vertex Group\] nebo \[Material\], každé jednotlivé strany.

V tomto menu si vybíráte, zda volíte roh, hranu nebo stěnu. Zatím nechme toto nastavené na stěny a ukažme si úkony, které lze dělat. Tyto jsou nejlépe ilustrované na stěnách, ale všechny platí také pro hrany a rohy.

Volí se stejně jako u objektů - levým tlačítkem myši a přidržením \[Shift\] na zvolení více najednou. Rozdíl je, že hlavní zvolená stěna je zabarvena stejně jako ostatní, pouze je opatřena bílým obtažením.

Máme zde navíc možnost zvolit „nejkratší" cestu mezi dvěma body. Zvolíme počáteční a poté se stisknutým \[Ctrl\] zvolíme konečný bod.

Kombinace \[Alt + Shift\] se pokusí nalézt jakousi cykličnost ve Vašem objektu a zvolit ji. Například pokud máte válec a stisknete na hranu jeho horní stěny, zvolí se celý okraj kolem dokola. Na obrázku 15 jsou tyto volby žlutě.

Co se týká translace, rotace atd. vše je stejné jako u celých objektů. Fungují zde stejné zkratky a principy.

Dva úkony, které slouží jako základ pro pokročilejší editaci, jsou Inset a Extrude. Nalezneme je na klávesách \[I\] a \[E\]. Inset vesměs utvoří novou stěnu napojenou stranami na tu původní a nechá Vás ji škálovat. Po stisku klávesy \[I\] a posunutí myši, Vám zůstane kostka z obrázku výše nalevo. Extrude udělá stejné napojení, ale posléze je nová stěna posunována, ne škálována. Tyto dvě operace lze aplikovat i na více stěn najednou. Pokud jsou to stěny sousedící, akce bude provedena jako by se jednalo pouze o jednu stěnu.

\[Shift + A\] funguje i v edit módu a přidá nový mesh do stejného objektu. Může se to zdát jako přidání nového objektu, ale všechny tyto části zastřešeny pod jedním objektem mají jediný Origin a sdílí mezi sebou všechny Omezovače a Modifikátory. Pro zvolení celé jedné spojené meshe je dobrá klávesová zkratka \[Ctrl + L\].

15\. Loop Cut

**Loop Cut** - Zkratkou \[Ctrl+R\] můžete provézt takovýto řez. Myší zvolíte, kde se má provést a napsáním čísla zvolíte na kolik částí takovýto řez rozdělí objekt. Výše bylo užito rozdělení na pět částí.

**Oddělování a Slučování** -- Stisknutím klávesy \[P\] se Vám otevře menu, ve kterém si můžete vybrat, dle čeho oddělíte část Vašeho současného objektu do objektu nového.

### Kamera

![](media/image9.png){width="3.374233377077865in" height="2.3263746719160103in"}

16\. Kamera

Stejné jako v realitě na scéně musí být kamera, která zaznamenává světlo odrážející se od scenérie. Pro vykreslování budeme většinou v Blenderu používat něco podobného. Pokud děláme cokoliv složitější než jeden model, který si otáčíme uprostřed obrazovky, je potřeba počítači říct, jak má scénu zobrazovat. Kamer může být více a každá obsahuje spoustu informací - například ohledně její pozice, rotace, perspektivy, objektivu a mnohé další.

#### Kamerový pohled

V \[Okno 3D zobrazení\] můžeme vidět buď volně nebo pohledem kamery

Scéna má většinou nastavenou jednu kameru jakožto výchozí. Při stisku \[Klávesy 0\] je náš pohled nastaven na ten skrze výchozí kameru.

\[Ctrl+Alt+0\] nastaví kameru na Váš aktuální pohled.

#### důležitá nastavení

##### Lens

Pod nastavením čočkou máte čtyři důležité možnosti:

1.  Typ: Perspektivní nebo Ortografická (viz. Perspektivy str.48)

2.  Focal Length: V podstatě optické přiblížení - zoom

3.  Shift: Toto se týká fotografického efektu zvaného Tilt-shift. Je moc náročné to zde vysvětlit, ale jsou na něj mnohé jiné zdroje.

4.  Clip: Říká kameře jaké rozpětí vzdáleností má zobrazit. Pokud je start nastaven na 10m a konec na 20m, kamera neuvidí nic blíže než 10m a vzdálenější než 20m. Pokud objekt leží přesně na hranici, zobrazí se pouze jeho část.

##### Viewport Display

Pro výsledek irelevantní, ale při práci velmi užitečný. Kamera je dosti komplexní záležitost a bylo by kontraproduktivní mít stále zobrazeny všechny informace o ní. Tady si vybíráme přesně ty, které chceme vidět v \[Okno 3D zobrazení\].

1.  Size: velikost ikony kamery

2.  Limits: zobrazuje odkud kam je nastaven \[Clip\]

3.  Name: pro účel přehlednosti větších kamerových sestav si můžeme vždy nechat zobrazit jméno kamery, jejíž pohled máme zobrazen

Toto nastavení má většina objektů. Má rozdílné parametry dle příslušného objektu, ale stejný účel.

## Vlastnosti

Zobrazuje veškerá nastavení pro zvolený objekt a scénu. Například jeho lokace, užité materiály, fyziku atd. Pozor zobrazuje pouze hlavní zvolený objekt, nijak zde neovlivňuji sekundárně zvolené objekty (označeny oranžově).

### Render

Popsáno v kapitole Render str. 45.

### Výstup (Output)

**Dimenze** - (Dimensions) Resolution samozřejmě udává velikost výstupního obrazu. Hodí se zde poukázat na procentuální slider, neboť ve většině velkých projektů nebudete chtít vykreslovat v plné kvalitě hned od začátku, protože je to plýtvání časem - pokud potřebujete pouze rámcově zkontrolovat výstup.

**Aspect** - mění skutečnou šířku nebo výšku pixelů - pokud nemáte jasný záměr, nechte zde 1:1.

**Render Region** - Vám umožní renderovat pouze část obrazu. Toto nejlépe zvolíte v pohledu kamery zkratkou \[Ctrl + B\] a přetažením myší přes čtvercový region, který chcete renderovat.

**Frame Start a End** - indikuje, od kterého do kterého časového bodu bude Blender renderovat. Můžete zde nastavit, abyste přeskakovali snímky.

Ke **Frame Ratu** je třeba podotknout, že mění celkovou rychlost animace. Může tím pádem velmi změnit konečný vzhled animace, obzvláště v případech fyzikálních simulací.

**Výstup** - (Output), zde se volí, kam a v jakém formátu chcete, aby byl výstup zapsán. Vesměs můžete vše nechat tak jak je, kromě File formátu.

Pokud vykreslujete pouze snímek, na výběr máte standartní \[.png\], \[.jpg\], etc. Však pokud vykreslujete animaci, tak se spíše dává ve formě \[.PNG\], protože standartní video formáty mají problémy s přerušováním a úpravami uprostřed. Zkrátka pokud byste našli uprostřed nějakou chybu, museli byste začít Render od začátku. Pokud je Vaším formátem \[.PNG\], již vykreslené snímky Vám zůstanou a můžete poté pouze překreslit ty potřebné. Stačí najít kterou část je třeba překreslit a nechat renderovat jenom danou část. Jednoduché animace si pro pohodlí je samozřejmě možné vykreslovat do videa, ale udělat ze snímků video není těžké a je to možné udělat i v Blender oknu Video Sequencing.

### Svět (World)

Navzdory prvotním pozorováním si všimneme, že není pozadí Vaší scény jen prázdný kanvas. Má materiál jako každý jiný objekt, využívá se převážně jako pozadí scény a pro osvětlení.

Nastavit tento materiál lze pod Shader Editor \> World.

Z mé osobní zkušenosti nedoporučuji u komplexnějších scén používat k osvětlení pouze Svět, protože toto světlo vypadá velmi uměle, neboť působí ze všech směrů identicky, což nevypadá dobře.

### Object

Zde se nachází standartní data pro objekt - umístění rotace, velikost atd. Pokud chcete jednu osu uzamknout, aby se v ní s objektem nedalo manipulovat, učiníte tak stisknutím zámku vedle příslušné hodnoty.

Následuje velké množství různých nastavení, která jsou důležitá, ale výrazně jednodušeji a přehledněji přístupná z jiných míst. Později se sem můžete vrátit. Pokud Vám tato zobrazení vyhovují více, můžete je také použít.

Krom Viewport Display, kde volím, které informace o daném objektu se mi zobrazují ve \[3D Viewport\].

### Materiály

Popsáno v kapitole Materiály na straně 37.

### Omezovače (Constraints)

Omezovače jsou definovaný vztah mezi dvěma objekty.

Tyto vztahy sahají od kopírování rotace a pohybu po limitaci vzdálenosti mezi dvěma objekty. Aplikují se na objekt, se kterým se nehýbe -- ten, který má být omezovačem upraven. Výše byl aplikován omezovač „Limit Distance" na sféroid a s cílem na krychli. Nyní pohyb krychle zdánlivě pohne sféroidem, pokud je dostatečně vzdálená. Zdánlivě, protože jeho origin se nezmění, vypadá, že se pohnul, avšak pokud se podíváte do jeho vlastností, zjistíte, že jeho souřadnice se nezměnily.

Často používaný omezovač je „Follow Path", kdy definujete objektu cestu a čas, a on se po ní bude v daném čase pohybovat.

### Modifikátory (Modifiers)

Modifikátory jsou procedurální efekty aplikované většinou na Mesh daného objektu. Jako příklady lze uvést nakopírování objektu za sebe, odečtení jednoho objektu od druhého, zarovnání rohů nebo zvýšení a snížení množství \[Tri\]. Celý smysl spočívá v tom, že tyto změny nejsou hned aplikovány, ale setrvávají na objektu. Takže pokud změním mesh, modifikátor se okamžitě přizpůsobí - dokud nestisknu Aplikovat, což natrvalo změní mesh a smaže Modifikátor. Modifikátorů mohu mít více najednou. Aplikují se vždy od vrchního tak, že každý následující pracuje již s meshem upraveným modifikátory předchozími.

Nalevo je jednoduchá ukázka „Subsurface Modifier", který se pokouší vyhlazovat meshe. Jako nafouknout uvnitř nich balónek a použít tento nový tvar jako tvar objektu. Napravo je pak kombinace „multiresolution", který zvýší jednoduché ploše množství stěn, aby poté „displace" mohl aplikovat z textury vzor.

Nad nastavením každého modifikátoru, vedle jména, je nastavení zobrazení a dvě šipky, které vám umožňují posouvat jej nahoru nebo dolu v pořadí aplikování. Toto je důležité, protože například na obrázku výše napravo, pokud bych aplikoval nejdříve Displace, tak by se aplikoval na jednoduchý plain o čtyřech vertexech, což by akorát jeden z nich pozvedlo a Multiresolution by poté nebyl moc platný, protože by stejně zůstala placatá Plane.

### Data \> Vertex Groups

Pokud potřebuji označit určitou část objektu -- například, aby měla nějaké specifické vlastnosti, používají se k tomu Vertexové skupiny. Všechny funkce od simulace vlasů, až po částice pro znehybnění částí objektů, se ptají, na kterou skupinu se mají aplikovat. Tyto nastavení se poznají dle ikony: ![](media/image10.png){width="0.21528871391076115in" height="0.26390201224846893in"}.

Skupiny se tvoří a mažou zde ve „Vertex Groups" - plusem a mínusem. Když máte zvolenou skupinu a vertexy na Vašem objektu, tlačítky Assign a Remove je připisujete a mažete z dané skupiny. Select a Deselect přičte nebo odečte vertexy z dané skupiny k Vašim právě zvoleným vertexům.

Výše vidíte látku, kde tři z jejíž rohů byly přidány do skupiny, která poté byla nastavena jako nepohyblivý záchytný bod látkové simulace.

## Hierarchie (Outliner)

Zde se Vám vypisuje seznam všech objektů na scéně. Všechny tyto objekty mají hierarchii. Mají nadřízený objekt a můžou mít podřízené objekty. Seznam podřízených objektů je vždy pod svým nadřízeným objektem (tzv. parent objekt) odsazen doprava. Hierarchie se nastavuje přetažením objektu, který si přejete přiřadit na objekt, který se má stát nadřízeným. Pokud nedržíte žádnou klávesu, můžete tímto přesouvat objekty pouze z kolekce do kolekce. Při držení klávesy \[Ctrl\] se vytvoří nový odkaz (tzv. link). Na ten samý objekt v dané kolekci a za držení klávesy \[Shift\] se nastaví daný objekt jako nadřízený.

Každý podřízený objekt je nějak ovlivněn svým rodičem (tzv. parentem). Pokud s parentem pohnu, pohne se mi také objekt podřízený. Pokud vypnu jeho zobrazení, všechny podřízené objekty také přestanou být viditelné.

Toto se používá hlavně pro zjednodušení práce. Například mám velmi složité auto skládající se z mnoha součástek, pro které tak mohu nastavit v hierarchii jednu část jako nadřízenou. Když ji zvolím, pohybuji celým autem a není potřeba vždy pohybovat každou součástkou zvlášť.

Jak nyní vidíte nejvýše v hierarchii máte \[Kolekci\]. Tyto jsou vyznačeny ![](media/image11.png){width="0.2569575678040245in" height="0.25001312335958004in"}. \[Kolekce\] slouží k uspořádání a napomáhají k přehlednosti. Zatržítko vedle kolekce zobrazí nebo schová všechny obsažené objekty. Objekt je viditelný, pokud existuje jeho Link alespoň v jedné zobrazené kolekci. U kolekcí je na pravém tlačítku myši, kromě možnosti přidat novou kolekci, také množství úprav známé z objektů, ale zde se dají aplikovat na každý objekt v kolekci naráz. V neposlední řadě je tu tlačítko „Instance to Scene", které vytvoří novou \[Instanci\] této kolekce a přidá jí do scény.

**Instance kolekce** -- se značí ![](media/image12.png){width="0.24306758530183728in" height="0.2777919947506562in"} a je jakýmsi odrazem původní kolekce. \[Instance\] je neupravitelná, ale budou se v ní projevovat změny z původní kolekce. Toto se nejvíce hodí například pokud pracujete ve skupině a importujete jinou \[Kolekci\] z externího souboru.

## Timeline

Pokud budete animovat nebo pracovat s časem. Toto okno zobrazuje časovou linku veškerých pohybů a změn, které nastanou za dobu trvání vaší animace.

Rozebráno v Kapitole Key-Framing na straně 39.

## Uživatelská Nastavení

Zde se nalézá obrovské množství možností, ale většina z nich nás nezajímá. S nejvyšší pravděpodobností budete chodit do následujících tří míst.

### Interface

Zvětšení, zmenšení textu a nastavení zobrazení. Většina je vcelku jasná.

### Add-ons

Kdyby Blender měl při prvním otevření obsahovat veškeré funkce, nebylo by v něm k vyznání, a tak je potřeba většinu mít vypnutou. Zde můžeme zapínat a vypínat užitečné funkce, jak vestavěné, tak stažené z internetu.

### Systém

Pokud máte v počítači grafickou kartu od Nvidia nebo AMD musíte přepnout Cycles Render Devices do CUDA nebo OpenCL respektive. Pokud kdykoli budete používat Cycles render viz. Render Engines a nebudete toto mít správně nastaveno, Blender Vaši kartu nevyužije, což může být pomalejší ve stovkách procent.

## Shader Editor

Domov pro veškeré materiály.

Toto je rozebráno v kapitole Materiály na straně 37.

## UV/Obrazový Editor

Místo pro textury.

Toto je rozebráno v kapitole Mapy a UV Unwrap na straně 34.

## Grafový Editor

Každá informace označena jako animovatelná (Animovatelná nastavení str. 31) nebo která má nastaven alespoň jeden Keyframe, bude mít své hodnoty zakresleny zde. Můžeme zde pozorovat jakoukoli z těchto hodnot v grafu za čas nebo naopak na ně nějaký graf aplikovat.

Pro příklad můžu nastavit, aby Z souřadnice této krychle vykreslovaly Sinusoidu. Nejdříve přidám krychli keyframe pohybu, takže se mi v levé části zobrazí její pozice jako 3 grafy. Tedy jeden pro X, Y a Z. Když nějaký z grafů zvolím, tak se označí a zobrazí ve střední části. Je to standartní graf. Čára reprezentuje hodnotu proměnné v daném čase. Vlevo vpravo je čas, nahoru dolů je hodnota a žluté tečky jsou \[Keyframe\]. V základu jsou \[Keyframe\] zakulacené a plynulé, tato plynulost se nastavuje dvěma čárami na každé straně všech \[Keyframe\]. Zde je nejjednodušší si s nimi trochu pohrát, aby člověk pochopil, jaký efekt mají.

Po pravé straně máme menu, které obsahuje nejzajímavější část tohoto okna. Pod Modifiers máte možnost namísto \[Keyframe\] použít funkce. Na výběr jsou sinusoidy a šumy všeho druhu.

## Částicové systémy

Částicové systémy spočívají v náhodném rozmístění objektů v nějaké oblasti. Částicových systémů máme dva druhy „Částicové" a „Vlasové", dle toho, jestli výsledný objekt zůstává součástí původního objektu, který ho emitoval (Vytvořil). Je to tak důležité rozdělení, že ve chvíli, kdy vytvoříte nový systém, prvním nastavením určíte, který typ tento systém je. Oba jsou velice složité, proto zde zevrubně bude popsán pouze systém vlasů.

Pokud máte slabší počítač, nyní najděte nastavení ViewPort Display \> Amount. Procento zde určuje, kolik procent vlasů se bude zobrazovat v okně 3D Zobrazení. Jelikož jsou tyto systémy vysoce výpočetně náročné, pokud jdete s množstvím nad nízké stovky, měli byste zde mít výrazně méně než 100.

Zpět nahoru, **Emission** - Number určuje množství vlasů, Length určuje jejich délku - pokud se jedná o Cestu a jejich velikost jestliže se jedná o objekty. Segmenty určují z kolika bodů je složena cesta. Ty jsou samozřejmě vyhlazovány, ale je to určitá maximální komplexnost tvaru cesty.

**Render** -- Render As určí, zda vlas je Cesta, Objekt nebo objekty z Kolekce. Ano, vlasem může být jakýkoliv objekt, který se na scéně nachází. Toto se hodí například pokud máte kolekci stromů a louku a potřebujete je náhodně po louce rozmístit. Pokud si zvolíte objekt nebo kolekci pod Render, objeví se Vám další menu, které umožní vybrat danou Kolekci nebo Objekt, a nastavit, jak se vybírá z kolekce, jestli náhodně nebo cyklením a jestli se má brát v potaz transformace objektu.

**Particle Edit (Mód)** -- Pokud máte na objektu částicový systém, objeví se Vám při jeho zvolení v 3D Viewportu nový mód. Tímto je Particle Edit mírně podobný Sculptingu se svými „Hřebeny", ale tím podobnost končí. V Particle Edit můžete vesměs učesat svůj částicový systém do libovolného tvaru. **Důležité** - jakákoliv změna v tomto módu Vám znemožní dělat změny v nastavení Systému. Pokud chcete udělat úpravu v jeho nastavení, musíte na jeho vrcholu stisknout tlačítko Zahodit změny.

## Praktické Informace

### Animovatelná nastavení

Vedle překvapivého množství nastavení v Blenderu uvidíte malou bílou tečku. Stejně tak, jako se mohou při animaci pohybovat objekty a kamery, můžeme měnit kterékoliv z těchto nastavení. Pokud stiskneme toto tlačítko, zapneme tím animovatelnost příslušného nastavení a tím je nyní tečka nahrazena kosočtvercem. Pokud má v daném čase (viz. Timeline str.27) nastavení zatržítko v tomto kosočtverci, znamená to, že pro tento čas je nastaven keyframe (viz. Key-Framing str.39).

![](media/image13.png){width="2.3649136045494314in" height="0.6980139982502187in"}

### Chytré vstupy

Kdykoliv v Blenderu vepisujete čísla, ať už při transformaci nebo u nastavení, je velmi pohodlné využít vestavěnou kalkulačku. Kdekoliv můžete zadávat desetinná čísla, odčítat, sčítat, násobit i dělit.

![](media/image14.png){width="1.9472222222222222in" height="0.26032917760279967in"} \>\> ![](media/image15.png){width="1.989861111111111in" height="0.2604527559055118in"}

![](media/image16.png){width="1.9169346019247595in" height="0.2396172353455818in"} \>\> ![](media/image17.png){width="1.999996719160105in" height="0.2708333333333333in"}
