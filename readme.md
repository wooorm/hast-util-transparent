# hast-util-transparent [![Build][build-badge]][build] [![Coverage][coverage-badge]][coverage] [![Downloads][downloads-badge]][downloads] [![Chat][chat-badge]][chat]

Check if a [node][] is a [**transparent**][spec] [element][].

## Installation

[npm][]:

```bash
npm install hast-util-transparent
```

## Usage

```javascript
var transparent = require('hast-util-transparent')

transparent({
  type: 'element',
  tagName: 'div',
  children: [{type: 'text', value: 'Alpha'}]
}) // => false

transparent({
  type: 'element',
  tagName: 'a',
  properties: {href: '#bravo', title: 'Charlie'},
  children: [{type: 'text', value: 'Delta'}]
}) // => true
```

## API

### `transparent(node)`

Check if the given value is a [**transparent**][spec] [element][].

###### Parameters

`node` (`*`) — Value to check.

###### Returns

`boolean` — whether `node` passes the test.

## Contribute

See [`contributing.md` in `syntax-tree/hast`][contributing] for ways to get
started.

This organisation has a [Code of Conduct][coc].  By interacting with this
repository, organisation, or community you agree to abide by its terms.

## License

[MIT][license] © [Titus Wormer][author]

<!-- Definition -->

[build-badge]: https://img.shields.io/travis/syntax-tree/hast-util-transparent.svg

[build]: https://travis-ci.org/syntax-tree/hast-util-transparent

[coverage-badge]: https://img.shields.io/codecov/c/github/syntax-tree/hast-util-transparent.svg

[coverage]: https://codecov.io/github/syntax-tree/hast-util-transparent

[downloads-badge]: https://img.shields.io/npm/dm/hast-util-transparent.svg

[downloads]: https://www.npmjs.com/package/hast-util-transparent

[chat-badge]: https://img.shields.io/badge/join%20the%20community-on%20spectrum-7b16ff.svg

[chat]: https://spectrum.chat/unified/rehype

[npm]: https://docs.npmjs.com/cli/install

[license]: license

[author]: https://wooorm.com

[node]: https://github.com/syntax-tree/hast#node

[element]: https://github.com/syntax-tree/hast#element

[spec]: https://html.spec.whatwg.org/#transparent-content-models

[contributing]: https://github.com/syntax-tree/hast/blob/master/contributing.md

[coc]: https://github.com/syntax-tree/hast/blob/master/code-of-conduct.md
