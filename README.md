# GitHub-reserved-names

> Get a list, or check if a user or organization name is reserved by GitHub

This is by no means a complete list of reserved GitHub user/organization names.

The list in this repository was gathered from several sources:

* [Octotree](https://github.com/buunguyen/octotree/) ([ref](https://github.com/buunguyen/octotree/blob/master/src/adapters/github.js#L1-L12)).
* [GitHub Hovercard](https://github.com/Justineo/github-hovercard/) ([ref](https://github.com/Justineo/github-hovercard/blob/master/src/hovercard.js#L35-L42)).
* [GitHub Custom Hotkeys Userscript](https://github.com/Mottie/GitHub-userscripts/wiki/GitHub-custom-hotkeys) ([ref](https://github.com/Mottie/GitHub-userscripts/blob/master/github-custom-hotkeys.user.js#L58-L90)).
* And manually entering names into https://github.com/account/organizations/new and seeing it labeled as "Reserved".

See the [history page](./history.md) for more details and how you can help expand this list.

## Install

```
$ npm install --save github-reserved-names
```

## Usage

```js
const isReserved = require('github-reserved-names');

isReserved.check("settings");
//=> true

isReserved.check("google");
//=> false

isReserved.all;
// [ 400, 401, 402, ..., "trending", "watching" ]
```

## CLI

```bash
$ npm install --global github-reserved-names
```

```bash
$ github-reserved --help

  Examples
    $ github-reserved issues
    true

    $ github-reserved --all
    400
    401
    ...

  Options
    --all   Show all reserved names
```

## License

MIT
