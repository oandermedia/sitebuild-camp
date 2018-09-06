# HTML

A HTML (HyperText Markup Language) egy leíró nyelv, ami a weboldal tartalom struktúrájáért felel, a vázát adja és a tartalom egyes elemeit jelentéssel látja el.

## A HTML elemek és szintaktikájuk

A HTML építőkövei a HTML elemek. Egy elem a legtöbb esetben egy nyitó címkéből, egy záró címkéből és a közte lévő tartalomból épül fel. Valamint a nyitó címke attribútumokat tartalmazhat, amik többlet információval látják el az elemet.

`<a href="http://oander.hu" target="_blank">...</a>`

- az `<a>... ide kerül a tartalom ...</a>` a HTML elem
- az `<a>` az elem nyitó címkéje
- az `</a>` az elem záró címkéje
- a `href="http://oander.hu"` az elem egyik attribútuma

Vannak olyan elemek, amik nem rendelkeznek záró címkével, így értelemszerűen tartalom sem lehet a két címke között. Ezek az elemek az attribútumok segítségével kapják meg az információt.

Ilyen elemek például:

- `<img>` - képet definiáló elem
- `<input>` - űrlap mezőt meghatározó elem
- `<br>` - sortörés egy szövegben
- `<hr>` - elválasztó vonalat jelölő elem
- `<link>` - külső stíluslap behúzására szolgáló elem
- `<meta>` - a weboldal head részében használható, meta információkat szolgáltató elem (SEO adatok, karakterkódolás stb.)

A HTML elemek teljes listája (csoportosítva is):
https://www.w3schools.com/tags/ref_byfunc.asp
http://html5doctor.com/element-index/

## A HTML elemek csoportosítása

A HTML elemeknek két fő csoportja van: block és inline elemek. A block elemek mindig 100% szélességben kitöltik a rendelkezésre álló teret, függetlenül attól milyen hosszú tartalom van az elemben. Az előttük és utánuk lévő elem mindig új sorban kezdődik a böngészőben. Ezzel szemben az inline elemek csak akkora szélességet foglalnak el, amekkora a tartalmuk, mellettük elhelyezkedhet további elemek. Az elemek block vagy inline tulajdonságát CSS-ből lehet módosítani.

Példa blokk elemre:

- `<div>` - általános blokk elem
- `<h1> - <h6>` - címsor elem
- `<p>` - bekezdés elem
- `<ul>` - rendezetlen lista elem

Példa inline elemre:

- `<span>` - általános inline elem
- `<a>` - hivatkozás elem
- `<strong>` - félkövér szöveget jelöl, jelentés tartalommal bír
- `<b>` - félkövér szöveget jelöl, nincs jelentés tartalma, csak stílust határoz meg
- `<img>` - képet jelölő elem

Teljes lista az elemek block / inline csoportosításáról:
https://www.w3schools.com/html/html_blocks.asp

## A HTML elemek attribútumai és szintaktikájuk

A HTML elemek egy vagy több attribútumot tartalmazhatnak, több esetén szóközzel elválasztva. Az attribútumok felépítése a következő:

`href="http://oander.hu" target="_blank"`

- a `href` az attribútum neve
- az `=` az összekapcsolás
- a `"http://oander.hu"` az attribútum értéke

Az attribútumok értéke nagyon változatos lehet. Tartalmazhat pl. egy url címet, egy szöveget, egy paramétert vagy több paramétert.

Néhány példa attribútumok érték típusaira:

- `alt="Ez itt egy kép leírása"` - szöveges érték
- `href="http://oander.hu"` - url érték
- `type="text"` - egy paraméter
- `class="button button-large button-red"` - több paraméter szóközzel elválasztva
- `content="width=device-width, initial-scale=1.0"` - több paraméter vesszővel elválasztva

## A HTML elemek attribútumainak csoportosítása

Az attribútumok között vannak olyanok, amik globálisak, bármelyik elemen el lehet helyezni:

- `id` - egyedi azonosítóval látja el az elemet
- `class` - osztály azonosítóval látja el az elemet
- `style` - egyedi stílust tehetünk az elemre
- `title` - címmel láthatjuk el az elemet

Valamint léteznek elem specifikus attribútumok (zárójelben azon elemek, ahol elhelyezhetőek):

- `href` (link, a) - hivatkozás egy forrásra
- `src` (img, script) - megjelöljük mi a forrás
- `action` (form) - az űrlap feldolgozásának helyét állítja be

Teljes attribútum lista (az on-al kezdődőek kihagyhatóak, nagyon ritkán használjuk)
https://www.w3schools.com/tags/ref_attributes.asp

Teljes lista a globális attribútumokról:
https://www.w3schools.com/tags/ref_standardattributes.asp

## A HTML elemek struktúrája, a DOM

Egy HTML elem (a záró címke nélküli elemek kivételével) tartalma lehet egy szöveg vagy egy másik HTML elem. Utóbbi esetben ezzel az egymásba ágyazással az elemek között egy szülő - gyermek kapcsolat, valamint az egy szinten lévő, egymást követő HTML elemek között egy testvér - testvér kapcsolat jön létre. Ezen kapcsolatok által kialakul egy szerkezet, ami a weboldal váza. Ezt nevezzük DOM-nak (Document Object Model).

Szabályozva van viszont, hogy az elemeknek milyen gyermek elemeik lehetnek, illetve mi lehet a szülő elemük. Ezeket a szabályokat a későbbi órák folyamán fokozatosan át fogjuk venni, amikor az elemek egy-egy csoportjáról tanulunk.

Említés szintjén néhány példa álljon itt:

```html
<ul>
  <li></li>
</ul>
```

Az `<ul>` elemnek csakis a `<li>` elemek lehetnek a gyermekei, a `<li>` elem viszont rendelkezhet másik szülővel, például az `<ol>` elembe is elhelyezhető.
A `<li>` elemnek viszont már nagyon sokféle gyermek eleme lehet, pl. egy `<a>` vagy egy `<div>` elem.

```html
<dl>
  <dt></dt>
  <dd></dd>
</dl>
```

Itt kicsit más a helyzet, a `<dl>` elem `<dt>` és `<dd>` elemeket tartalmazhat. Ezek az elemek pedig csak a `<dl>` elem gyermekei lehetnek.

## A weboldal alap felépítése

Minden weboldalnak a következő HTML szerkezettel kell kezdődnie:

```html
<!DOCTYPE html>
<html lang="hu">
  <head>
    ... nem látható, de fontos információk ...
  </head>
  <body>
    ... látható tartalom ...
  </body>
</html>
```

- a `<!DOCTYPE html>` mondja meg a böngészőnek, hogy a weboldalunk milyen szabálykönyv szerint íródott
- a `<html>` elem minden weboldal első HTML eleme, ez definiálja a teljes weboldalt
- a `lang="hu"` attribútum tájékoztatja a böngészőt az oldalunk nyelvéről
- a `<head>` elem tartalmazza a weboldalunk 'nem látható', de fontos információit
- a `<body>` elem tartalmazza a weboldal látható részét, tartalmát

## A head rész elemei

Az oldalunk `<head>` elemébe a következő elemek kerülhetnek:

```html
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  ... további meta elemek (pl. SEO keywords, description stb.)
  
  <title>Hello World</title>
  
  <link rel="stylesheet" href="style.css">
  <script src="script.js">Hello World</script>
  
  <style>
    ... belső stíluslap ...
  </style>
  <script>
    ... belső script ...
  </script>
</head>
```

- többféle meta elemet tartalmazhat a weboldalunk, de ezek között két nagyon fontos van. A charset meta az oldalunk karakterkódolásáról ad információt a böngészőnek. A viewport meta elemmel pedig jelezzük a böngészőnek, hogy reszponzív, mobilra optimalizált az oldalunk
- a `<title>` az oldalunk címe, ami a böngésző tab fülön meg is jelenik
- a `<link>` és `<script>` elemek segítségével külső forrásból húzhatunk be stíluslapokat és scripteket
- a `<style>` és `<script>` elemekkel belső stíluslap és script illeszthető az oldalba

## HTML5 új szemantikus elemei

A HTML5-el bejöttek új elemek a HTML-be, amik segítik szemantikusabban felépíteni a weboldalt. Ezek az elemek a következők:

- `<header>`
- `<footer>`
- `<main>`
- `<aside>`
- `<nav>`
- `<section>`
- `<article>`
- `<figure>`
- `<figcaption>`
- `<time>`

Ezekről található leírás a következő oldalon (jól le van az is írva mire használható egy-egy elem):
http://html5doctor.com/article-archive/
