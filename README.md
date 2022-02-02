# WebVTT Sample with VTTCue Properties

This is sample code testing different VTTCue properties using WebVTT.

## Running Locally with Node
This demo uses [Node](https://nodejs.org/en/) and the [Node Package Manager](https://www.npmjs.com/). The npm package [https://www.npmjs.com/package/http-server](http-server) is used to statically host video and vtt files.

Requirements:
1. Node + npm and/or npx
2. http-server

[Instructions to install Node and npm](https://docs.npmjs.com/cli/v7/configuring-npm/install)

### Using npx
If you wish to not install any dependencies locally and are using npm version 5.2+, you may simply run the code as follows:
```
npx http-server --cors -c-1
```

### Using npm
Otherwise, be sure to follow the steps below:
1. Run `npm install` to install all `package.json` dependencies
2. Run `npm start`

## Running Locally Using Other Methods
You may use any other static server and/or package manager, if you wish. Note that Without a static server, vtt text tracks will not properly load onto the video file due to [CORS](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS) limitations.

## Properties
The cue properties below determine how text tracks appear on a video:
* `line` - where a cue appears **vertically** (up or down)
* `position` - where a cue appears **horizontally** (left or right)
* `align` - text **alignment** for a cue (left, right, center)
* `size` - **width** of cue text area
* `vertical` - if present, displays text vertically, rather than horizontally

\* `vertical` "inverses" direction for almost all properties. The descriptions above assume the `vertical` property is omitted. Ex. with the property included, `line` is affected *horizontally* instead.

## References and Credits
This demo was inspired by:
* [brenopolanski's webvtt demo](https://github.com/brenopolanski/html5-video-webvtt-example)
* [iandevlin's webvtt demo](https://iandevlin.github.io/mdn/video-player-with-captions/)

The following resources were consulted:
* [MDN Web Docs - WebVTT](https://developer.mozilla.org/en-US/docs/Web/API/VTTCue)
* [MDN Web Docs - VTTCue](https://developer.mozilla.org/en-US/docs/Web/API/VTTCue)
* [W3C - WebVTT](https://w3c.github.io/webvtt/) (candidate recommendation)
