# HTML

A HTML (HyperText Markup Language) egy leíró nyelv, ami a weboldal tartalom struktúrájáért felel, a vázát adja és a tartalmat jelentéssel látja el.

## A HTML szintaktikája

A HTML építőkövei a HTML elemek. Egy elem a legtöbb esetben egy nyitó tagből, egy záró tagból és a közte lévő tartalomból épül fel. Valamint a nyitó tag attribútumokat tartalmazhat, amik többlet információval látják el az elemet.

`<a href="http://oander.hu" target="_blank">...</a>`

- az `<a>...</a>` maga az elem
- az `<a>` a nyitó tag
- az `</a>` a záró tag
- a `href="http://oander.hu"` az attribútum

Vannak olyan elemek, amik nem rendelkeznek záró taggel, így értelemszerűen tartalom sem lehet a két tag között. Ezek az elemek az attribútumok segítségével kapják meg az információt.

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

- `<div>`
- `<h1> - <h6>`
- `<p>`
- `<ul>`

Példa inline elemre:

- `<span>`
- `<a>`
- `<strong>`
- `<img>`

## A HTML elemek attribútumai

Az attribútumok között vannak olyanok, amik globálisak, bármelyik elemr tartalmazhatja.

Ilyen attribútumok például:

- `id`
- `class`
- `style`
- `title`

Valamint léteznek elem specifikus attribútumok, például

- `href`
