# Color-diff
Implemets the CIEDE2000 color difference algorithm, conversion between RGB and LAB color and mapping all colors in palette X to the closest color in palette Y based on the CIEDE2000 difference.

## Installation

```bash
npm install color-diff --save
```
	
## Usage
	
```js
var diff = require('color-diff');
```

### diff.closest(color, palette)

Returns the closest color.

```js
var color = { R: 255, G: 1, B: 30 };
// red, green, blue
var palette = [ {R: 255, G: 0, B: 0 }, {R: 0, G: 255, B: 0 }, {R: 0, G: 0, B: 255} ];

diff.closest(color, palette); // {R: 255, G: 0, B: 0 }, red
```
	
The result above is obvious, but `diff.closest` could deal with more complicated cases.

#### color
`Object`

`color` is an object containing 3 properties: 'R', 'G', 'B', such as:

```js
{ R: 255, G: 1, B: 0 }
```	

#### palette

`Array.<Object>`

Color palette array which contains many `color`-like objects.


## Author
Markus Näsman

## License
See COPYING
