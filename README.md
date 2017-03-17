# [RecordRTC.org](http://RecordRTC.org)

1. [RecordRTC API Reference](http://RecordRTC.org/RecordRTC.html)
2. [MRecordRTC API Reference](http://RecordRTC.org/MRecordRTC.html)
3. [MediaStreamRecorder API Reference](http://RecordRTC.org/MediaStreamRecorder.html)
5. [StereoAudioRecorder API Reference](http://RecordRTC.org/StereoAudioRecorder.html)
6. [WhammyRecorder API Reference](http://RecordRTC.org/WhammyRecorder.html)
7. [Whammy API Reference](http://RecordRTC.org/Whammy.html)
8. [CanvasRecorder API Reference](http://RecordRTC.org/CanvasRecorder.html)
9. [GifRecorder API Reference](http://RecordRTC.org/GifRecorder.html)
10. [Global API Reference](http://RecordRTC.org/global.html)

[![npm](https://img.shields.io/npm/v/recordrtc.org.svg)](https://npmjs.org/package/recordrtc.org) [![downloads](https://img.shields.io/npm/dm/recordrtc.org.svg)](https://npmjs.org/package/recordrtc.org)

http://recordrtc.org/ is a documentation webpage for [RecordRTC.js](https://github.com/muaz-khan/RecordRTC). It is [open-sourced in github](https://github.com/muaz-khan/RecordRTC/tree/gh-pages) and everyone can collaborate to improve documentation.

To contribute:

```sh
mk node_modules
npm install recordrtc.org --production

cd node_modules
cd recordrtc.org # go to this directory

mkdir node_modules
npm intall recordrtc --production # fetch latest RecordRTC from NPM
```

1. You should modify `node_modules/recordrtc/RecordRTC.js` file
2. You'll see that each function/property/method is having comments (format is chosen from http://usejsdoc.org/).
3. Using `jsdoc` tool, you can generate documentation HTML pages from `node_modules/recordrtc/RecordRTC.js` file
4. You should NEVER modify HTML pages. You merely need to modify `node_modules/recordrtc/RecordRTC.js` file for documentation.

Steps to contribute:

1. Modify `node_modules/recordrtc/RecordRTC.js` file
2. Use below NPM-commands to generate HTML pages.
3. Manually copy/paste `node_modules/recordrtc/RecordRTC.js` file in the resulting `recordrtc.org` directory
4. Copy `recordrtc.org` directory and replace in `RecordRTC` github clone's `gh-pages` section
5. Send a pull-request and done!

```sh
# First step: install recordrtc.org template and javascript file
npm install recordrtc.org

# Second step: generate HTML files from template & RecordRTC.js file
cd node_modules
cd recordrtc.org

# This command generates HTML pages from RecordRTC.js file

# for Linux/Mac
node_modules/.bin/jsdoc node_modules/recordrtc/RecordRTC.js -d ./../../recordrtc-gh-pages node_modules/recordrtc/README.md -t template

# for Windows
node_modules\.bin\jsdoc node_modules\recordrtc\RecordRTC.js -d .\..\..\recordrtc-gh-pages node_modules\recordrtc\README.md -t template
```

Now you'll see a directory with name `recordrtc.org`.

```sh
# This command runs index.html file
# You can use it to preview HTML pages (doc files)

# for Linux/mac
./../../recordrtc.org/index.html

# for Windows
.\..\..\recordrtc.org\index.html
```

## Send pull requests

Now, you should fork this repository:

* [https://github.com/muaz-khan/RecordRTC](https://github.com/muaz-khan/RecordRTC)

And push/pull `recordrtc.org` directory to `gh-pages`.

## How to modify `RecordRTC.js` file?

RecordRTC is using comments format from jsdoc:

* [http://usejsdoc.org/](http://usejsdoc.org/)

E.g.

```javascript
/**
* Description
* @summary Summary
* @typedef Hello
* @example
* var some = new Something();
*/
```

Example - `stopRecording` method:

```javascript
/**
* This method stops the recording. It is strongly recommended to get "blob" or "URI" inside the callback to make sure all recorders finished their job.
* @param {function} callback - Callback to get the recorded blob.
* @method
* @memberof RecordRTC
* @instance
* @example
* recorder.stopRecording(function() {
*     // use either "this" or "recorder" object; both are identical
*     video.src = this.toURL();
*     var blob = this.getBlob();
* });
*/
stopRecording: stopRecording,
```

## License

[RecordRTC.js](https://github.com/muaz-khan/RecordRTC) is released under [MIT licence](https://www.webrtc-experiment.com/licence/) . Copyright (c) [Muaz Khan](https://plus.google.com/+MuazKhan).
