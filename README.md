# www.RecordRTC.org

[![npm](https://img.shields.io/npm/v/recordrtc.org.svg)](https://npmjs.org/package/recordrtc.org) [![downloads](https://img.shields.io/npm/dm/recordrtc.org.svg)](https://npmjs.org/package/recordrtc.org)

```
npm install recordrtc.org

# here is how to generate HTML files
cd .\node_modules\recordrtc.org

node_modules\.bin\jsdoc node_modules\recordrtc\RecordRTC.js -d .\..\..\recordrtc.org node_modules\recordrtc\README.md -t template
```

Now you'll see a directory with name `recordrtc.org`.

```
.\..\..\recordrtc.org\index.html
```

Now, you should fork this repository:

* https://github.com/muaz-khan/RecordRTC

And push/pull `recordrtc.org` directory to `gh-pages`.

RecordRTC is using comments format from jsdoc:

* http://usejsdoc.org/

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

## License

[RecordRTC.js](https://github.com/muaz-khan/RecordRTC) is released under [MIT licence](https://www.webrtc-experiment.com/licence/) . Copyright (c) [Muaz Khan](https://plus.google.com/+MuazKhan).
