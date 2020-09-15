# Předmluva

## Informace o dokumentu - Cílová skupina, Styl a Záměr

Psáno pro Blender 2.8. Tento dokument má zahrnovat základní znalosti potřebné k rozumné práci ve 3D grafických programech se zaměřením na Blender.

Je důležité vědět, že cílem této práce je seznámit čtenáře s Blenderem do takové míry, aby byl schopen sám začít prozkoumávat tento rozsáhlý program. Mnohé části jsou přeskočeny nebo vysvětleny povrchně za účelem nezahltit čtenáře.

Účelem je vysvětlit, jak funguje Blender spíše v jeho principech a s některými nuancemi, které mohou nováčkům dělat problém. Je mnoho lidí, kteří se již do modelování v Blenderu chtěli pustit, ale poté, co si našli na internetu nějaké tutoriály, stejně nevěděli, co dělali, protože jenom slepě sledovali tutoriál bez hlubšího pochopení. Pochopení problematiky, schopnost stavby na předešlých znalostech a zkoušení si sám nových věcí, je stav, který je právě záměrem této práce.

## Kde všude se používá

*„Používám Blender protože je silný, ne protože je zdarma"*, řekl Max Puliero v rozhovoru s CGCookie.com v roce 2017. (Karon, 2017)[^Karon_2017] Od té doby, především během několika posledních pár let, se Blender přeměnil z komerčně téměř nepoužívaného programu v extrémně výkonný kus softwaru, který by mohl konkurovat mnohým placeným alternativám.

Příklady, kde Blender byl použit:

Max Puliero uvedl, že při práci na hře Dark Souls III, používal na design postav Blender, přestože jeho studio standartně užívalo jiné programy. (Karon, 2017)[^Karon_2017] Ubisoft Animation Studio má v průběhu roku 2020 adoptovat Blender jako svůj hlavní software. (Ubisoft, 2019)[^Ubisoft_2019] Unity Game Engine nativně podporuje \[.blend\] soubory.

Již dlouho existovaly filmy tvořené pomocí Blenderu, ale Next Gen (Netflix, 2018)[^Netflix_2018] od Netflix je jeden z prvních komerčních filmů, které byly skutečně animovány čistě v Blenderu (Veldhuizen, 2018)[^Veldhuizen_2018]. Pokud nebereme celý film, ale stačí využití, pak ve filmu Warcraft byl narychlo přidán Murloc s jeho pomocí. (Failes, 2016)[^Failes_2016]

Pokud se zajímáte spíše o vesmír, NASA vydala některé z jejích modelů v \[.blend\] formátu. Dokonce projekt Experience Curiosity nějakou dobu běhal na Blender Enginu, dokud nebyl zrušen.

Takže jak sami vidíte, není toho málo.

![Next Gen film od Netflix](next-gen.jpg)

## Blender FOUNDATION -- Trocha Historie

(Blender (software), n. d.)[^Blender]

![Ton Roosendaal](ton-roosendaal.jpg)![Stránka Manuálu pro Blender circa 2002](man03.jpg)

NeoGeo bylo dánské animační studio, které roku 1994 začalo vytvářet Blender pro firemní použití. Hlavním autorem byl Ton Roosendaal -- tehdejší spolumajitel firmy. V roce 1995 už měli funkční verzi 1.0 a 1. ledna 1998 byl jejich program vydán jako freeware -- volně dostupný na internetu. Ještě ten samý rok byla firma NeoGeo zanikla a Roosendaal založil svoji vlastní firmu Not a Number Technologies (NaN), za účelem dále rozvíjet projekt Blender. NaN roku 2002 zkrachovala a Roosendaal ještě téhož roku založil neziskovou organizaci Blender Foundation.

Blender Foundation se během následujících let pokoušel udělat Blender Open-Source (prozatím byl Blender pouze volně dostupný jako celý program, open-source znamená, že bude i volně upravitelný a bude na něm moct pracovat kdokoli). Roosendaal vybral svůj cíl 100 000 euro od lidí a dosáhl svého cíle. Dodnes je Blender vyvíjen hlavně jeho komunitou a čtyřmi programátory zaměstnanými u Blender Foundation.

## Blender není jen na 3D modelaci

Ačkoli začal svůj život jako animační program, vyvíjen pro potřeby animace, rozsáhlá komunita mu přidala množství různých dalších funkcí. Dnes zvládá editovat video, zvuk, zvládá sledovat objekty na kameře a nedávno se objevily i fotogrammetrické pluginy. Rozšířila se také podpora jiných programů. Není vzácné, aby herní engine měl podporu pro proprietární \[.blend\] soubory nebo podporoval přímé napojení pomocí pluginů.

## Pluginy

Roztroušenost vývoje donutila Blender využívat tzv. pluginy. Plugin je funkce programu taková, že není brána jako součástí jeho jádra, ale bere se jako jeho rozšíření. Lze jej například i vypnout nebo stáhnout z internetu. Příkladem je třeba podpora dalších formátů, předpřipravené nové objekty a zjednodušený přístup k některým nastavením. Takových pluginů je obrovské množství a dají se doinstalovat do Blenderu podle potřeby. On sám už nějaké obsahuje, a i když jsou některé v základu vypnuty, není kolikrát potřeba je stahovat a lze je pouze zapnout v nastavení.


[^Karon_2017]: (Karon, 2017): Karon, Pavla. 2017. CGCookie. Max Puliero: "I Use Blender Because It's Powerful, Not Because It's Free". [Online] 19. 9 2017. https://cgcookie.com/articles/max-puliero.
[^Ubisoft_2019]: (Ubisoft, 2019): Ubisoft. 2019. Ubisoft News. Ubisoft Joins Blender Development Fund to Support Open Source Animation. [Online] 22. 6 2019. https://news.ubisoft.com/en-us/article/1Fse1XyXzj76UJ1gKFohbz/ubisoft-joins-blender-development-fund-to-support-open-source-animation.
[^Netflix_2018]: (Netflix, 2018): Netflix. 2018. Netflix. Next Gen. [Online] 2018. https://www.netflix.com/cz-en/title/80988892.
[^Failes_2016]: (Failes, 2016): Failes, Ian. 2016. MovieMaker. Building the World of Warcraft: An In-Depth Conversation With Visual Effects Supervisor Bill Westenhofer. [Online] 22. 6 2016. https://www.moviemaker.com/creating-warcraft-interview-visual-effects-supervisor-bill-westenhofer/.
[^Veldhuizen_2018]: (Veldhuizen, 2018): Veldhuizen, Bart. 2018. BlenderNation. "Next Gen" - Blender Production by Tangent Animation soon on Netflix! [Online] 20. Srpen 2018. https://www.blendernation.com/2018/08/20/next-gen-blender-production-by-tangent-animation-soon-on-netflix/.
[^Blender]: Blender (software), Wikipedia. n. d.. Blender (software). Wikipedia. [Online] n. d.. n. d. n. d. https://en.wikipedia.org/wiki/Blender_(software).
