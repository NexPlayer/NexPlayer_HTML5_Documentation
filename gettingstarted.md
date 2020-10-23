<a id="gettingstarted-top"> </a>

# Getting Started

## NexPlayer™ Integration

### Sample

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

    <script src="https://nexplayer.nexplayersdk.com/latest/nexplayer.js"></script>
    <script type="text/javascript">
        nexplayer.Setup({
            key: "ENTER YOUR LICENSE KEY HERE",
            div: document.getElementById('player'),
            src: 'http://commondatastorage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4',

        });

    </script>
</body>
</html>
```


<div class="alert alert-success hints-alert"><div class="hints-icon"><i class="fa fa-mortar-board"></i></div><div class="hints-container"><p>Please note that replacing the player key is mandatory. You can find the player key in the license section of your dashboard at <a style ="color:#5A5A5A!important" href="https://www.nexplayersdk.com/portal/portal-hub">https://www.nexplayersdk.com/portal/portal-hub</a></p>
</div></div>



<div class="alert alert-info hints-alert"><div class="hints-icon"><i class="fa fa-info-circle"></i></div><div class="hints-container"><p>Please note that we have built a specific library for Samsung Smart TVs. To enable Tizen support, please change the current library to our Tizen library: </p>
</div></div>

### Step-by-Step

To integrate NexPlayer™ into your project you must complete the following steps:

- The NexPlayer™ JavaScript library should be included in the HTML file:

```html
<script src="https://nexplayer.nexplayersdk.com/latest/nexplayer.js"></script>
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
## NexPlayer™ Configuration

There are a substantial number of customizable options for NexPlayer™ including: the name and subtitle format of the video, a logo for the company, the DRM information, a VAST link, and the thumbnail preview...

```js
    key: 'Player key to validate the playback', // Mandatory
    div: document.getElementById('player'), // Mandatory
    src: 'URL video', // Mandatory
    poster: 'URL poster', // Optional
    name: 'Name of the Video', // Optional
    subtitle: 'Subtitle of the video', // Optional
    logosrc: 'URL logo of the company', // Optional
    callbacksForPlayer: callback, // Optional callback called with the player instances
    drm: [{
        NexDRMType:'DRM Type (eg. com.widevine.alpha(', NexDRMKey: 'URI for the DRM Key', 
        NexHeaders:[{FieldName: 'Header Field Name', FiledValue: 'Header Field Value'}],
        NexCallback:OptionalDRMCallbackForFairPlay
    }], // Optional DRM information
    vast: 'URL with a VAST/VPAID advertisement', // Optional
    useDynamicThumbnails: true, // Optional
    staticThumbnailsImage: 'URL of the image containing the preview thumbnails', // Optional
    staticThumbnailsVTT: 'URL of the VTT file', // Optional
    cast: {}, //Optional
    type_360: '360 visualisation type' // Optional
    autoplay: true, // Optional
    mutedAtStart: true, // Optional
    lowLatency: true, // Optional
    lowLatencyLiveDelay: 5, // Seconds of delay, Optional
    debug: true, // Optional
    callbacksForLogger: callback, // Optional callback called with the logger instances
    startFullscreen: true, // Optional
    disableFullscreen: true, // Optional
    showingFullUI: true, // Optional
    seekUI: 10, // Seconds for the seek buttons, Optional
    callbacksForReturn: callback, // Optional callback called with the return button
    disableKeyEvents: false, // Optional
    blockZoom:true, // Optional only available when the 360 is enable
    watermark:{url:'URL of the image of the water mark',//optional
        position:{top: 'size px', left: 'size px'},
        size:{height:'size px', width: 'size px'}
    },
    ...
    
```