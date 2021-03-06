# Modifier key queries

Inspired by [keymaster](https://github.com/madrobby/keymaster).
This is a small subset of the functionality in that library.

Using this library you can query the `modifiers` object at any time to see if a modifier key is held down.

Default supported keys are:
`shift`, `alt`, `option` (same as `alt`), `control`, `command`

```javascript
if (modifiers.command || modifiers.control) {
  // do something special
}

// ..inside your click handler
if (modifiers.shift) {
  ...
}
```

You can also add your own to the defaults:
```javascript
modifiers.add({
  leftArrow: 37,
  upArrow: 38,
  rightArrow: 39,
  downArrow: 40,
  w: 87,
  a: 65,
  s: 83,
  d: 68
});
```

### Building

To create the minified and compressed version with source mapping, run:

`npm run minify`

The code uses addEventListener so if you need to support IE8 you'll want to change the code to use
something like what's described [here](http://msdn.microsoft.com/en-us/magazine/ff728624.aspx).


### License

MIT
