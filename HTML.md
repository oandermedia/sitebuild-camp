# HTML

A HTML (HyperText Markup Language) egy leíró nyelv, ami a weboldal tartalom struktúrájáért felel, a vázát adja és a tartalmat jelentéssel látja el.

## A HTML szintaktikája

A HTML építőkövei a HTML elemek. Egy elem a legtöbb esetben egy nyitó címkéből, egy záró címkéből és a közte lévő tartalomból épül fel. Valamint a nyitó címke attribútumokat tartalmazhat, amik többlet információval látják el az elemet.

`<a href="http://oander.hu" target="_blank">...</a>`

- az `<a>...</a>` maga az elem
- az `<a>` a nyitó címke
- az `</a>` a záró címke
- a `href="http://oander.hu"` az attribútum

Vannak olyan elemek, amik nem rendelkeznek záró címkével, így értelemszerűen tartalom sem lehet a két tag között. Ezek az elemek az attribútumok segítségével kapják meg az információt.

Ilyen elemek például:

- `<img>`
- `<input>`
- `<br>`
- `<hr>`
- `<link>`
- `<meta>`

A HTML elemek teljes listája (csoportosítva is):
https://www.w3schools.com/tags/ref_byfunc.asp
http://html5doctor.com/element-index/

## A HTMl elemek csoportosítása

A HTML elemeknek két fő csoportja van: block és inline elemek. A block elemek mindig 100% szélességben kitöltik a rendelkezésre álló teret, míg az inline elemek nem. Az elemek ezen tulajdonságát CSS-ből lehet módosítani.

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
- `<img>` - képet jeölő elem

Teljes lista:
https://www.w3schools.com/html/html_blocks.asp

## A HTML elemek attribútumai

Az attribútumok között vannak olyanok, amik globálisak, bármelyik elem tartalmazhatja.

Ilyen attribútumok például:

- `id` - egyedi azonosítóval látja el az elemet
- `class` - csoportosíthatjuk vele az elemet
- `style` - egyedi stílust tehetünk az elemre
- `title` - címmel láthatjuk el az elemet

Teljes lista a globális elemekről:
https://www.w3schools.com/tags/ref_standardattributes.asp

Valamint léteznek elem specifikus attribútumok, például

- `href` (link, a) - hivatkozás egy forrásra
- `src` (img, script) - megjelöljük mi a forrás
- `action` (form) - az űrlap feldolgozásának helyét állítja be

Teljes attribútum lista (az on-al kezdődőek kihagyhatóak, nagyon ritkán használjuk)
https://www.w3schools.com/tags/ref_attributes.asp

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
