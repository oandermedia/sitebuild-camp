# HTML

A HTML (HyperText Markup Language) egy leíró nyelv, ami a weboldal tartalom struktúrájáért felel, a vázát adja és a tartalom egyes elemeit jelentéssel látja el.

## A HTML elemek és azok szintaktikája

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

## A HTMl elemek csoportosítása

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

## A HTML elemek attribútumai

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

## A weboldalak alap felépítése

A HTML elemek szülő - gyermek kapcsolatban állnak egymással. Így jön létre egy szerkezet, a weboldal váza, amit DOM-nak (Document Object Model) hívunk. Tehát egy HTML elem vagy egy másik HTML elemet tartalmaz vagy már magát a szöveges tartalmat.

Létezik több olyan elem, amik szinte bárminek lehet szülője vagy gyermeke, viszont sok elem csak bizonyos elemeknek lehet szülője vagy gyermeke. Erre néhány példa:

```html
<ul>
  <li></li>
</ul>
```

Tehát itt az `<ul>` -be nem tehetünk másféle elemet és a `<li>` elemet sem használhatjuk ezen kívül, de pl. egy `<ol>` elembe bele lehet tenni ugyanígy a `<li>` elemet.

```html
<dl>
  <dt></dt>
  <dd></dd>
</dl>
```

Ezekről később egy nagyobb témánál lesz szó, mi minek lehet a gyermeke és szülője.

Egy website alap felépítése:

```html
<!DOCTYPE html>
<html lang="hu">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Hello World</title>
  </head>
  <body>
    <h1>Hello World</h1>
    <p>This is a web page.</p>
  </body>
</html>
```

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
