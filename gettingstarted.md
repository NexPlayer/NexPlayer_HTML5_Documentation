# Getting Started

## Sample Integration

Playing a video with the integrated UI can be done in an HTML5 page:

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no" />

    <title>NexPlayer</title>
    <style type="text/css">
        #player_container {
            width: 90%;
            margin: auto;
            padding-top: 50.625%; /* 16:9 Aspect Ratio 56.25 * 0.9 */
            position: relative;
        }
        @media (min-width: 75rem) {
            #player_container {
                width: 50%;
                padding-top: 28.125%; /* 16:9 Aspect Ratio 56.25 * 0.5 */
            }            
        }
        h1 {
            text-align: center;
        }
        #player {
            background-color: black;
            position: absolute;
            top: 0px;
            width: 100%;
            height: 100%;
        }
        #warning {
            background-color: red;
            text-align: center;
            display: none;
        }
    </style>
</head>

<body>
    <h1>NexPlayer HTML5</h1>
    <div id="warning">
        <h1>Unsupported protocol</h1>
        <h3>Loading HTML using the file protocol can't be supported. Please use a <a href="https://nexplayer.github.io/getting_started.html#explanation">server</a> (HTTP/HTTPS protocol).</h3>
    </div>
    <div id="player_container">
        <div id="player"></div>
    </div>

    <script src="Latest SDK version. Check 'Releases' section"></script>
    <script type="text/javascript">
        nexplayer.Setup({
            key: "ENTER YOUR LICENSE KEY HERE",
            div: document.getElementById('player'),
            src: "http://commondatastorage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4",

        });

    </script>
</body>
</html>
```


<div class="alert alert-success hints-alert"><div class="hints-icon"><i class="fa fa-mortar-board"></i></div><div class="hints-container"><p>Please note that replacing the license key is mandatory. License key should have been already sent to your inbox or you can request one from support.madrid@nexplayer.com.</p>
</div></div>

<div class="alert alert-info hints-alert"><div class="hints-icon"><i class="fa fa-info-circle"></i></div><div class="hints-container"><p>Please note that we have built a specific library for Samsung Smart TVs. To enable Tizen support, please change the current library to our Tizen library: </p>
</div></div>

## Step-by-Step Integration Guide

To integrate NexPlayer into your project you must complete the following steps:

- The NexPlayer™ JavaScript library should be included in the HTML file:

```html
<script src="Latest SDK version. Check 'Releases' section"></script>
```

<div class="alert alert-success hints-alert"><div class="hints-icon"><i class="fa fa-mortar-board"></i></div><div class="hints-container"><p>Please note that the use of https to call our library is mandatory. </p>
</div></div>

- A div that will contain the video and the UI has to be declared:
```html
<body>
...
    <div id="player"></div>
...
</body>
```
- The player should be initialized by entering the previous div to the Setup method:
```js
nexplayer.Setup({
    key: 'ENTER YOUR LICENSE KEY HERE',
    div: document.getElementById('player'),
    src: 'http://commondatastorage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4'
});
```

## Sample Integration with React

Integrating NexPlayer into a React Component can also be posible with the next sample:

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no" />
    <link rel="icon" type="image/png" href="/src/img/NexPlayer-favicon.png" />

    <title>NexPlayer React Sample</title>
    <style type="text/css">
        #player {
            background-color: #191828;
            position: absolute;
            top: 0%;
            width: 50%;
            height: 50%;
        }
        #warning {
            background-color: red;
            text-align: center;
            display: none;
        }
    </style>
</head>

<body>
    <h1>NexPlayer HTML5</h1>
    <div id="warning">
        <h1>Unsupported protocol</h1>
        <h3>Loading HTML using the file protocol can't be supported. Please use a <a href="https://nexplayer.github.io/getting_started.html#explanation">server</a> (HTTP/HTTPS protocol).</h3>
    </div>
    <div id="root"></div>
        <script src="Latest SDK version. Check 'Releases' section"></script>
        <script type="module" src="/src/main.jsx"></script>
</body>
</html>
```
<div class="alert alert-success hints-alert"><div class="hints-icon"><i class="fa fa-mortar-board"></i></div><div class="hints-container"><p>Please note that the use of https to call our library is mandatory. </p>
</div></div>

Nexplayer.jsx Component
```jsx
import React, { useEffect } from "react";

            function App() {
            useEffect(() => {
                nexplayer.Setup({
                key: "ENTER YOUR LICENSE KEY HERE",
                div: document.getElementById("player"),
                src: "https://dash.akamaized.net/akamai/bbb_30fps/bbb_30fps.mpd",
                });
            }, []);

            return (
                <>
                <div id="player"></div>
                </>
            );
            }

            export default App;
```
<div class="alert alert-info hints-alert"><div class="hints-icon"><i class="fa fa-info-circle"></i></div><div class="hints-container">
<p>You can use the React Hook 'useEffect' to load the JavaScript code which loads the player on the component.
On the return we must add the div that will contain the video. </p>
</div></div>
    <div class="alert alert-success hints-alert"><div class="hints-icon"><i class="fa fa-mortar-board"></i></div><div class="hints-container"><p>Please note that replacing the license key is mandatory. License key should have been already sent to your inbox or you can request one from support.madrid@nexplayer.com.</p>
    </div></div>

main.jsx file
```jsx
import React from "react";
import ReactDOM from "react-dom/client";
import NexPlayer from "./NexPlayer";
import "./index.css";

ReactDOM.createRoot(document.getElementById("root")).render(
  <React.StrictMode>
    <NexPlayer />
  </React.StrictMode>
);
```
## React Sample Deployment

For deploying this project first install Node.js
```bash
npm install
```

Compiling all the assets
```bash
npm run dev
```

Building the project
```bash
npm run build
```

Finally host the /dist folder on a WebServer


## NexPlayer Configuration Parameters

There is a substantial number of customizable options for NexPlayer™ including: the name and subtitle format of the video, a logo for the company, the DRM information, a VAST link, and the thumbnail preview...

```js
    key: 'Player key to validate the playback', // Mandatory
    div: document.getElementById('player'), // Mandatory
    src: 'URL video', // Mandatory
    allowScreenPlayPause: true, // Optional: Allow to play and pause the video when clicking over it.
    autohide: true, // Optional, sets if the UI must hide when the user doesn't interact with the video.
    autoplay: true, // Optional
    blockZoom:true, // Optional: Only available when 360 is enabled.
    callbacksForLogger: callback, // Optional: Callback called along the logger instances.
    callbacksForReturn: callback, // Optional: Callback called along the return button.
    callbacksForPlayer: callback, // Optional: Callback called along the player instances.
    cast: {}, // Optional
    chromecastEndImg: 'URL image', // Optional
    chromecastLaunchImg: 'URL image', // Optional
    debug: true, // Optional
    defaultQuality: -1, // Optional: Set the starting track by indicating its id. Default is -1, which will enable the ABR.
    disableFullscreen: true, // Optional
    disableKeyEvents: false, // Optional
    drm: [{
        NexDRMType:'DRM Type (eg. com.widevine.alpha)', NexDRMKey: 'URI for the DRM Key', 
        NexHeaders:[{FieldName: 'Header Field Name', FieldValue: 'Header Field Value'}],
        NexCallback: // Optional DRM callback for FairPlay
    }], // Optional: DRM information
    externSubtitles: [{"src": "VTT", "language": "eng" }, ...] // Optional
    hideOptionsUi:{  // Optional: Hide the desired setting from the UI.
        quality: false,
        speed:false,
        audio:false,
        subtitles:false
	},
    hideScreenPlay: false, // Optional: Hide the play button in the middle of the video, which appears when the video is paused.
    hideVolumeIcon: true, // Optional: Hide the volume icon for mobile devices. The volume is controlled by the device buttons.
    lowLatency: true, // // Toggle on/off low latency.
    liveSettings: { //Optional, requires low latency.
        liveDelay: 5, // Optional, seconds of delay.
        maxDrift: 10, // Optional, the maximum delay before to make a seek live.
        playbackRate: 0.5,   // Optional, the speed that the player gets in order to keep the live delay.
    }, // Optional, settings for live playback.
    logosrc: 'URL logo of the company', // Optional
    mutedAtStart: true, // Optional
    maxFrameDrop:
    pip: true, // Optional: Enables picture-in-picture mode.
    poster: 'URL poster', // Optional
    seekUI: 10, // Optional, sets the number of seconds the UI buttons will seek forwards or backwards.
    showingFullUI: true, // Optional
    showUI360: boolean, // Oprional
    srcSets: [
        {
            src: 'video URL',
            drm: {
                NexDRMType:'DRM Type (eg. com.widevine.alpha)', NexDRMKey: 'URI for the DRM Key', 
                NexHeaders:[{FieldName: 'Header Field Name', FieldValue: 'Header Field Value'}],
                NexCallback: // Optional DRM callback for FairPlay
            } // Optional: DRM information or undefined
            valid: false // Set always false
        },
        {
            src: 'other video URL',
            drm: 'undefined',
            valid: false // Set always false
        },
        ...
    ] // Optional: Objects array containing a stream and an optional DRM.
    staticThumbnailsImage: 'URL of the image containing the preview thumbnails', // Optional
    staticThumbnailsVTT: string, // URI of the VTT file containing thumbnails timing and location info (Optional when using static thumbs).
    startingBufferLength: number, // Optional, determines the buffer that the video should have before start.
    startFullscreen: true, // Optional
    subtitle: 'Subtitle of the video', // Optional
    timeUI: boolean, // Optional, determines if the time will be hidden in the UI.
    title: 'Name of the video', // Optional
    type_360: '360 visualisation type' // Optional, 'equirectangular', 'cubemap' or 'topdown'.
    useDynamicThumbnails: true, // Optional
    useiOSFullScreen: boolean, // Optional
    vast: 'URL with a VAST/VPAID advertisement', // Optional
    watermark: { 
        url: 'URL of the image of the watermark', // Optional
        position: { top: 'size px', left: 'size px'},
        size: { height:'size px', width: 'size px'}
    },
    withCredentials: boolean, // Optional, indicates whether or not cross-site Access-Control requests should be made using credentials such as cookies, authorization headers or TLS client certificates.
    forceOffset: number, // Optional, allows to select an offset when looking for the segments on HLS live videos. Player will take EXT-X-MEDIA-SEQUENCE plus the given offset as the starting segment number of the playlist.
```