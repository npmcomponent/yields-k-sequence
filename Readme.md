*This repository is a mirror of the [component](http://component.io) module [yields/k-sequence](http://github.com/yields/k-sequence). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/yields-k-sequence`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*

# k-sequence

  keyboard sequences.

## Installation

  Install with [component(1)](http://component.io):

    $ component install yields/k-sequence

## API

### seq(keys[, ms], fn)

Create a function that will be invoked only if
the given `keys` sequence is matched, `ms` can be omitted
and defaulted to `500ms`.

if `ms` is `500ms` the keys must be pressed within `500ms` for
the callback to be called.

```js
var a = seq('a b c', function(e){});
var b = seq('a * b * c', function(e){});
el.addEventListener('keydown', a);
el.addEventListener('keydown', b);

press('a b c'); // => a is called
press('a a b b c'); // => b is called
```

## Tests

```bash
$ make test
```

## License

  MIT
