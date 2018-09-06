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

## A HTML elemek attribútumai

Az attribútumok között vannak olyanok, amik globálisak, bármelyik elem tartalmazhatja.

Ilyen attribútumok például:

- `id` - egyedi azonosítóval látja el az elemet
- `class` - csoportosíthatjuk vele az elemet
- `style` - egyedi stílust tehetünk az elemre
- `title` - címmel láthatjuk el az elemet

https://www.w3schools.com/tags/ref_standardattributes.asp

Valamint léteznek elem specifikus attribútumok, például

- `href` (link, a) - hivatkozás egy forrásra
- `src` (img, script) - megjelöljük mi a forrás
- `action` (form)

https://www.w3schools.com/tags/ref_attributes.asp

## A weboldalak alap struktúrája

A HTML elemek szülő - gyermek kapcsolatban állnak egymással. Így jön létre egy szerkezet, a weboldal váza, amit DOM-nak (Document Object Model) hívunk.

Léteznek olyan elemek, ami szinte bárminek lehetnek szülei vagy gyermekei, viszont vannak speciális esetek. Ilyen például:

```html
<ul>
  <li></li>
</ul>

<dl>
  <dt></dt>
  <dd></dd>
</dl>
```

Weboldal alap struktúra:

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
