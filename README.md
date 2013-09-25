# GH Gif [![Build Status](https://secure.travis-ci.org/node-gh/gh-flow.png?branch=master)](https://travis-ci.org/node-gh/gh-flow) [![NPM version](https://badge.fury.io/js/gh-flow.png)](http://badge.fury.io/js/gh-flow) [![Dependency Status](https://david-dm.org/node-gh/gh-flow.png)](https://david-dm.org/node-gh/gh-flow)

![DaftPunktocat](http://zno.io/RMu9/daftpunktocat.gif)

NodeGH plugin for commenting on pull requests/issues using GIF reactions.

> Maintained by [Zeno Rocha](https://github.com/zenorocha) and [Eduardo Lundgren](https://github.com/eduardolundgren).

## Install

```
[sudo] npm install -g gh-gif
```

## Usage

```
gh gif
```

Option             | Usage        | Type
---                | ---          | ---
`-n`, `--number`   | **Required** | `Number`
`-R`, `--reaction` | **Required** | `String`
`-i`, `--image`    | *Optional*   | `String`
`-r`, `--repo`     | *Optional*   | `String`
`-u`, `--user`     | *Optional*   | `String`

#### Examples

* Comment on pull request/issue #75 with a happy reaction.

    ```
gh gif 75 --reaction happy
    ```

* Comment on pull request/issue #75 of a certain repo with a surprised reaction.

    ```
gh gif 75 --reaction surprised --user node-gh --repo gh-gif
    ```

* Comment on pull request/issue #75 using a certain image.

    ```
gh gif 75 --image http://media1.giphy.com/media/5DQdk5oZzNgGc/original.gif
    ```

* Comment on multiple pull requests/issues at the same time.

	```
gh gif --reaction happy --number 1 --number 2
	```

## Testing

Check [Travis](https://travis-ci.org/node-gh/gh-gif) for continous integration results.

* Run [JSHint](http://www.jshint.com/), a tool to detect errors and potential problems.

    ```
npm run-script lint
    ```

* Run [Mocha](http://visionmedia.github.io/mocha/), a unit test framework.

    ```
npm run-script test
    ```

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## History

* v0.1.3 September 22, 2013
    * Do not post gif on giphy error
* v0.1.2 September 16, 2013
    * Use public beta key instead of the private one
* v0.1.1 September 15, 2013
    * Fix `gh gif 1 --image url`
    * Fix `--reaction` to use `--image` command implementation
* v0.1.0 September 15, 2013
    * First public release
* v0.0.1 September 12, 2013
    * Start plugin using [gh-boilerplate](https://github.com/node-gh/gh-boilerplate)

## License

[BSD License](https://github.com/node-gh/gh/blob/master/LICENSE.md)