# simplayer

## About

This is saimple multi platform sound player.
I get ideas from [opener](https://www.npmjs.com/package/opener).

This module should be used when to play simple sound or sound effect.
Not suitable for music players.

## Instalation

```sh
npm install simplayer -g

# if you want to use in node
npm install simplayer --save
```

## Usage

Simplayer function return child process instance.

```js

var simplayer = require('simplayer');

var musicProcess = simplayer('/path/to/sound.mp3');

```

If platform is windows, then support wav file only.

```js

var musicProcess = simplayer('C:\\path\\to\\sound.wav');

```

If handle to close event, Please, in the following manner.

```js

var simplayer = require('simplayer');

var musicProcess = simplayer('/path/to/sound.mp3');

musicProcess.on('close', function(code) {
  console.log('child process exited with code ' + code);
});

```

## Author

- Maxmellon

## LICENSE

MIT
