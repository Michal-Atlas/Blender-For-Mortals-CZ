# Ostatní

## Soubory

### Typy souborů

1.  \[.blend\] -- proprietární typ užívaný pouze Blenderem. Pokud jej podporuje jiný software, vědomě podporuje Blender

    a.  Pokud máte pod File\>External Data\>Pack into .blend zaškrtnuto ano, externí soubory jako textury atd. jsou vloženy přímo do .blend souborů

2.  \[.blend1\] -- Záložní .blend soubor. Po stisknutí tlačítka uložit, se starý .blend soubor přepíše na .blend1 a změny se uloží do starého \[.blend\].

3.  \[.obj\] -- univerzální soubor obsahující pouze Meshe

4.  \[.stl\] -- univerzální soubor obsahující pouze textury/materiály, téměř vždy přichází v páru s .obj souborem

### Import a Export

K Exportu a Importu slouží menu File. Nacházíme zde čtyři možnosti Link, Append, Import a Export. Import a Export slouží pochopitelně při práci s jinými programy a umožňují například pracovat s výše zmíněným \[.obj\] a \[.stl\] soubory. Zajímavějšími jsou Append a Link, které pracují pouze a jenom s jinými \[.blend\] soubory. Append přidá jakýkoli objekt, materiál nebo kolekci z jiného souboru do současného. Append pouze přidá **kopii** dané věci, která je v novém souboru editovatelná a plně nezávislá na původním souboru. Link se chová podobně jako instance zmiňovaná u Kolekcí v kapitole Outline na str. 27. Link není upravitelný v novém souboru, ale reflektuje změny ze souboru původního.

### Jak správně předat SOUBOR tak, aby ho Každý otevřel

Toto může být některým jasné, ale stále se potkávám s lidmi, kteří toto nedodržují, takže si to zopakujme.

1.  Zeptám se člověka, v jakém formátu bude/chce pracovat.

2.  Nejlépe pošlu formát, o který požádal nebo nějaký ze standardů, které otevře co nejvíce programů - např. \[.obj\] a \[.stl\]

3.  Je dobré přiložit i originální \[.blend\] soubor pro přidanou kompatibilitu. Toto také umožní dotyčnému vyexportovat projekt do čehokoli potřebuje

4.  Hlavně nezapomeňte přiložit důležité soubory ze kterých jsou brány informace. Blender umí zabudovat veškeré soubory textur, materiálů, animací atd. do svého \[.blend\] souboru, a dokonce je také exportuje a upravuje dle potřeby při exportu do jiných formátů, ale ty jsou většinou hůře nebo pracně upravitelné. Často je dobré zkrátka originální soubory také přiložit

## Suzanne

![Suzanne.svg.png](media/image26.png){width="2.3344717847769028in" height="1.9444444444444444in"}

(Inductiveload, 2008)

V komunitě běhá takový vtípek, tato opice je jedním ze symbolů Blenderu. Když bylo jasné, že NaN zkrachuje, vydali poslední update, ve kterém byla přidána tato opičí hlava. Od té doby je tak trochu maskotem, a hlavně se velmi často používá na rychlé testování světel, textur, animací atd. Dodnes vydržela a je obsažena i v nejnovějších verzích.