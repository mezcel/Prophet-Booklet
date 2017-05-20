# Prophet Booklet
###### page curl, page turn, text reader

#### About
* I am merely applying turn.js with text content featuring key prophets of the Christian Bible.

* I hope to expand it to include the women prophets. My intentions are purely academic.

#### Status

* Outdated Demo Video: [YouTube Link](https://www.youtube.com/watch?v=LkJA5SSsctA)

##### Dev. Notes

* I am updating the [jsonProphets.json](https://github.com/mezcel/Prophet-Booklet/blob/master/jsonProphets.json) file external from the Flipbook index.html file.

* The JSON file is intended to illustrate/mirror the JSON file used in the existing JavaScript

> Contained within the [Prophet Flipbook - Turnjs 4.zip](https://github.com/mezcel/Prophet-Booklet/blob/master/Prophet%20Flipbook%20-%20Turnjs%204.zip), index.html
```javascript
var jsonProphets = {...};
jsonProphets = jsonProphets.prophets;
```
### MOD Focal Points

* I based my template off of: [Developer of Turn.Js - Emmanuel Garcia ](https://github.com/blasten/turn.js/wiki/Reference)

##### CSS

* adjust the pages dynamically, or otherwise to account for page grow or shrink, at the moment my book has 46 page faces

<em>prophet-flipbook.css</em>

```css
.sj-book .p1,
.sj-book .p2,
.sj-book .p3,
.sj-book .p45,
.sj-book .p46{
	background-color:white;
	background-image:url(../pics/book-covers.jpg) !important;
}

.sj-book .p45{
	background-position:-960px 0 !important;
}

.sj-book .p46{
	background-position:-1440px 0 !important;
}
```

##### JS

* adjust the pages dynamically, or otherwise to account for page grow or shrink, at the moment my book has 46 page faces

<em> prophet-flipbook.js</em>

```javascript
if (newPage<pages-3)
		$('.sj-book .p45 .depth').css({
			width: depthWidth,
			right: 20 - depthWidth
		});
	else
		$('.sj-book .p45 .depth').css({width: 0});
```
