### Hexidecimal to RGB

Convert a hexidecimal color value to an array of [R, G, B].  Accepts 6- or 3-digit color values.

```js
var hexToRGB = _ => {
  _ = _.replace(/^(#|0x)/, '');
  var rgb = parseInt(_, 16);
  return _.length === 6 ? 
    [ rgb >> 16, (rgb >> 8) & 0xFF, rgb & 0xFF ] 
  : _.length === 3 ? 
    [ 17*(rgb >> 8), 17*((rgb >> 4) & 0xF), 17 * (rgb & 0xF) ] 
  : 
    [NaN, NaN, NaN];
};
```

