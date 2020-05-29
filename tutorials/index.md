# Ukázky / Cvičení

{::options auto_ids="true" /}
1. TOC_TEST
{:toc}

Možná jste právě dočetly tuto práci a nevíte kde začít s nápadem, nevíte kde začít s Meshem, jediné co na toto pomůže jsou zkušenosti, ale pro rámcovou představu kde začít, následuje několik velmi jednoduchých ukázek Renderů. U kterých v rychlosti rozeberu, jak byly dělány, abyste si mohli vytvořit trochu představu o tom, jak začít, co z čeho dělat a za pomocí jakých nástrojů. Záměrně jsou vynechány specifické detaily se záměrem neukázat jednoduše opsatelný postup, na konci kterého vlastně nemáte ponětí, co jste udělali.

## Vaporwave

1. zapněte bloom
2. přidejte si plane s dvěma Materiály tmavým a Emission
    1. dejte na něj několik Multiresolution Simple Subdivide s materiál Offset 1, vypnutý Replace Original a zvýšený Thickness
    1.  přidejte na něj displace s Texturou hluku nejlépe s Texture Coordinate nastaveno na nový Plane Axis objekt
    1.  přidejte dvakrát Modifier Array, jednou Relative offset podle osy X a poté Y
    1.  Nyní můžete animovat Plane Axis a Displace se Vám bude v průběhu animace měnit
3. silnice je udělaná pomocí jedné cesty do tvaru S
    1.  poté Plane s Modifikátory Solidify, Bevel a Curve s Object nastaveným na cestu (pokud vám Curve nefunguje, zkontrolujte si Deformation Axis a zkuste ji změnit)
    1.  světla podél silnice jsou z malé Plane se stejným Solidify a Bevel Modifikátorem s Array Modifikátorem na zdvojení, aby světla byla na obou stranách. Druhý Array, který jich vytvoří takové množství, aby sahala po celé délce silnice. Nakonec přidáme Curve modifier stejný jako předtím
    1.  dejte si pozor na pořadí Modifikátorů
4. slunce, může být pouze koule s Emission Materiálem, ale abychom dosáhli té pruhovanosti ve stylu Vaporwave, je třeba něčeho trochu složitějšího.
    1.  Texture Coordinate vezme souřadnice bodu na Slunci a Separate XYZ vyseparuje svislou osu Z. Poté provedeme Modulo operaci, což způsobí, že ve chvíli, kdy hodnota přesáhne nějakou hranici, je resetována zpět na nulu
    1.  Takže máme číslo, které se pohybuje mezi 0 a 0.1 podle výšky. To můžeme napojit do ColorRamp, která převede tuto hodnotu na danou barvu
    1.  Fresnel dává hodnotu dle úhlu pohledu. V tomto případě to znamená, že Slunce bude svítit na krajích více. Fresnel dává ale moc nízké hodnoty, a tak je vynásobíme konstantou, abyste ji mohli napojit přímo do síly záře
5. Kruhy kolem slunce mají základ v Extrudované kružnici, která poté byla opakované Extrudována a Insetována
    1.  Poté jim byl přidán keyframe na všechny osy rotace a v grafovém editoru v pravém menu pod modifiers byla na každou osu přidána Built-In Function Sine s různými Amplitudami a Offsety, aby měly zdánlivě „náhodnou" rotaci po celou dobu animace
6.  Portál na konci silnice je velmi placatý válec s ozdobně Extrudovaným a Insetovaným pláštěm
    1.  Seshora a zespoda má Voronoi Texture nodu obarvenou s pomocí Color Rampy
    1.  Poté má připojen Mapping na svůj Vector, aby mohla být v Mapping nodě animovaná Rotace, která způsobí pohyb naší textury
    1.  Nezapomeňte u Mapping Nody použít Texture Coordinate nodu
7. Auto má na sobě stejný Wireframe Modifier jako síť. Poté jsem udělal dvojitý loop cut, škáloval vertikálně dolů krajní stěny, a tím máme zevrubný tvar. Poté si jej můžete vyzdobit jak moc nebo jak málo se vám líbí
    1.  Na auto byl přidán Omezovač Follow Path, nastaven na cestu z kroku 3. Přidal jsem několik málo Keyframe na rotaci, aby byla hezčí v té zatáčce a skutečně tam byl pocit rychlosti
8. Pokud chcete, můžete dále experimentovat a přidělat kameru například na auto. Zde se mi nejvíce osvědčil Limit Distance Modifier
9.  Můžete zkusit přidat jakousi mlhu s pomocí kostky, která svým obsahem zabírá celou scénu a má Volume Shader

## Jednoduchá krajina z výšky

1. přidejte Mesh \> Plane objekt
2. přidejte Light \> Sun
3. posuňte Slunce na pozici \[2;2;2\]
    1.  může mít zářivost okolo 20
4. přidejte Ploše materiál
5. přidejte Vlnovou Texturu \[Wave Texture\]
    1.  s nastavením \[1;79.2;11.1;1\]
6.  přidejte druhou Vlnovou Texturu
    1.  nastavení \[47.2;78.3;16;7.4\]
7. spojte výstup Barvy do Matematické nody
    1.  nastavení, minimum
    1.  tuto nodu napojte na Displacement
8. přidejte druhý Principled BSDF
    1.  prudce zvyšte u obou Kovovost \[Metallic\]
9. původní Principled nastavte do modra
    1.  a snižte mu Hrubost \[Roughness\] asi na 0.3
10. druhý nastavte do zelena
11. barvu Textury z kroku 5 napojte na hrubost druhého Shaderu
12. přidejte Mix Shader Nodu, jejímž faktorem je barva z Textury z kroku 5 a sčítá naše dva shadery

A vznikne nám takováto pěkná texturka, mapka.

## Káva a Svačina

> Poznámky: Render Engine -- Cycles, Textury Přebrány z cc0Textures.com od (Demes, 2019)

1. deska stolu je jednoduchá plane s materiálem z image nod z volně stažitelné textury o třech částech - tedy textura, normál mapa a dislokační mapa
2. pro talíře je ideální Subsurface Modifiier přidán na velmi široký a nízký válec se zvednutými okraji, případně extrudovaný střed dolů
3. šálek je další Subsurface Modifier s tím, že ucho je válec, jehož konce byly střídavě točeny a Extrudovány, dokud neměl správný tvar
4. nejlepší výsledky u objektů, jenž mají být kapaliny uvnitř nádob, mám, když Shell objektu je mezi vnitřní a vnější stěnou nádoby
5. pěna má aplikovaný tupý Proporční Editace \> Random nebo Displace pro ten jakýsi pěnovitý tvar. Poté je dobré opět proporční editací snížit střed s širokým rozsahem a se sníženým opět zvednout. To vytvoří takový ten tvarový artefakt jejího tvoření
    1.  posyp na pěně je jednoduchý Particle Systém, který odkazuje na objekt malé hnědé kuličky. Aplikován je na několik středových vertexů
6.  donut je klasický tórus, trocha Displace \> Noise pro nerovný povrch
    1.  s polevou je několik možností. Navrhuji zkopírovat vrchní polovinu vertexů donutu a aplikovat na ně Solidify a Bevel modifier s vysokou kvalitou
    1.  posyp je další particle systém, tentokrát odkazující na skupinku různobarevných válců
7. v neposlední řadě, nezapomeňme někam pěkně umístit slunce

## Metro

> Poznámky: Render Engine -- Cycles, Textury Přebrány z cc0Textures.com od (Demes, 2019) a (Demes, 2018).

1. zde jde nejvíce o aplikování textur
2. schody jsou kvádrem s Array Modifier a jednoduchou texturou
3. na nich leží jako dlažba pouze plane
4. kovové zarážky jsou ze spláclého kvádru s Loop Cut na jedné straně a pak Extrudovanou jednou ze vzniklých stěn
5. stěny jsou kostka, která měla dvě stěny odstraněny a poté byla zešikmena. Edge na jednom konci byly Extrudovány rovně, poté toto bylo pouze zopakováno
    1.  stěny jsou s Noise Mapou na Displace, aby měly ten zrnitý tvar a velká Voronoi texture spojena s Color Ramp, aby utvořily ty skvrny zbývající oranžové barvy
6. zábradlí je ze tří skleněných válců spojeny pomocí Pipe Joints \> Pipe Elbow z Add-onu Add Mesh: Extra Objects a válcem ve stěně
7. světla jsou válec s Emission shaderem, „drženy" z každé strany válcem, napojeny na větší válec, který má polovinu svých Edges pomocí Snapu dané na pozici stropu
8. na konci chodby je opět ze stejného Add-onu, Extras \> Wall Factory

> Pomáhejte si tu s 3D kurzorem. Pokud Vám například nejde pořádně zarovnat k sobě zábradlí, jděte do Edit módu zvolte nějakou stěnu a dejte 3D kurzor to Selection a poté můžete zvolit svůj objekt a použít Selection to 3D kurzor. Tím se Vám dají na správné místo ve dvou osách a stačí je pouze posunout.
