# repro-svg-to-vue-component

_TDLR: SVG files with `style` tags throw errors on IE._

It seems that the `lib/StyleComponent.js` file is written using recent syntax (object method shorthand), and is not transpiled properly before being used. This causes syntax errors on Internet Explorer 11 (and older). I believe that updating a bit the `lib/StyleComponent.js` file should fix the issue.

## Installation

```sh
yarn
```

## Starting

```sh
yarn dev
```

## Steps to reproduce

0. **Follow the steps below using IE 11.**
1. Open `http://localhost:3000/working`, and play with the counter button. Each click does increment the counter.
2. Open `http://localhost:3000/buggy`, and play with the counter. Nothing happens.
3. Open the browser console. There is a syntax error linked to the `lib/StyleComponent.js` file.
