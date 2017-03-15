# [RecordRTC.org](http://RecordRTC.org)

[![npm](https://img.shields.io/npm/v/recordrtc.org.svg)](https://npmjs.org/package/recordrtc.org) [![downloads](https://img.shields.io/npm/dm/recordrtc.org.svg)](https://npmjs.org/package/recordrtc.org)

http://recordrtc.org/ is a documentation webpage for [RecordRTC.js](https://github.com/muaz-khan/RecordRTC). It is [open-sourced in github](https://github.com/muaz-khan/RecordRTC/tree/gh-pages) and everyone can collaborate to improve documentation.

To contribute:

1. You should modify `RecordRTC.js` file (aka [`latest.js`](https://github.com/muaz-khan/RecordRTC/blob/gh-pages/latest.js) file)
2. You'll see that each function/property/method is having comments (format is chosen from http://usejsdoc.org/).
3. Using `jsdoc` tool, you can generate documentation HTML pages from `latest.js` file
4. You should NEVER modify HTML pages. You merely need to modify `latest.js` file for documentation.

Steps to contribute:

1. Modify `latest.js` file
2. Use below NPM-commands to generate HTML pages.
3. Manually copy/paste `latest.js` file in the resulting `recordrtc.org` directory
4. Copy `recordrtc.org` directory and replace in `RecordRTC` github clone's `gh-pages` section
5. Send a pull-request and done!

```
# First step: install recordrtc.org template and javascript file
npm install recordrtc.org

# Second step: generate HTML files from template & latest.js file
cd node_modules
cd recordrtc.org

# This command generates HTML pages from latest.js file

# for Linux/Mac
node_modules/.bin/jsdoc node_modules/recordrtc/RecordRTC.js -d ./../../recordrtc-gh-pages node_modules/recordrtc/README.md -t template

# for Windows
node_modules\.bin\jsdoc node_modules\recordrtc\RecordRTC.js -d .\..\..\recordrtc-gh-pages node_modules\recordrtc\README.md -t template
```

Now you'll see a directory with name `recordrtc.org`.

```
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

## How to modify `latest.js` file?

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

Example - [`stopRecording`](https://github.com/muaz-khan/RecordRTC/blob/gh-pages/latest.js#L206) method:

```javascript
/**
 * This method stops recording. It takes single "callback" argument. It is suggested to get blob or URI in the callback to make sure all encoders finished their jobs.
 * @param {function} callback - This callback function is invoked after completion of all encoding jobs.
 * @method
 * @memberof RecordRTC
 * @instance
 * @example
 * recordRTC.stopRecording(function(videoURL) {
 *     video.src = videoURL;
 * });
 * @todo Implement <code class="str">recordRTC.stopRecording().getDataURL(callback);</code>
 */
stopRecording: stopRecording,
```

## License

[RecordRTC.js](https://github.com/muaz-khan/RecordRTC) is released under [MIT licence](https://www.webrtc-experiment.com/licence/) . Copyright (c) [Muaz Khan](https://plus.google.com/+MuazKhan).
