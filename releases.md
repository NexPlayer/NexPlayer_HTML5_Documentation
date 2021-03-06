<a id="releases-top"> </a>

<a href="https://nexplayer.github.io/NexPlayer_HTML5_Documentation/#/"><img text src="./_images/logo5.png" alt="Nexplayer"></a>

***

# Releases

Each version of the SDK is hosted in a CDN to allow faster and more efficient developments. Optionally, the library can be downloaded and hosted on a custom server.

#### Version 5.5.1
```
https://nexplayer.nexplayersdk.com/5.5.1/nexplayer.js
```
* **[Added]** hideOptionsUi: feature to hide some settings properties from the ui as the quality, speed ...

Date: Mar 8th 2021

#### Version 5.5.0
```
https://nexplayer.nexplayersdk.com/5.5.0/nexplayer.js
```
* **[Added]** MultiView, allows to see more than one stream at the same time
* **[Added]** Function for checking stream compatibility with the current used platform
* **[Added]** YouTube´s streams support
* **[Added]** allowScreenPlayPause: feature to disable the play/pause clicking on the screen
* **[Added]** defaultQuality: feature to start the video using the given default quality
* **[Added]** hideScreenPlay: feature to hide the play button which appears when the video is pausing
* **[Added]** Supporting multiple stream source: Selects a playable stream from an array of objects depending on the device and the browser
* **[Added]** Providing alternate streams as a backup: When a streams fails player is capable of skiping to the next provided stream that works
* **[Added]** disableAbr() method
* **[Added]** getVersion() method
* **[Added]** unMount and detroy for multiView
* **[Improved]** HLS Performance with low network
* **[Improved]** toggleBar() makes that the volume bar disappears too, now it has been solved

Date: Mar 8th 2021

#### Version 5.4.2
```
https://nexplayer.nexplayersdk.com/5.4.2/nexplayer.js
```
* **[Improved]** Volume controller
* **[Improved]** Cuechange events

Date: Jan 12th 2021

#### Version 5.4.1
```
https://nexplayer.nexplayersdk.com/5.4.1/nexplayer.js
```
* **[Added]** Error events
* **[Added]** dashSettings Option
* **[Added]** Callback to blockAt method
* **[Improved]** startFullscreen Option

Date: Dic 21th 2020

#### Version 5.4
```
https://nexplayer.nexplayersdk.com/5.4/nexplayer.js
```
* **[Added]** Picture in Picture Option
* **[Added]** useiOSFullScreen Option to use the native IOS full screen
* **[Improved]** Live button
* **[Improved]** startFullscreen Option

Date: Dic 10th 2020

#### Version 5.3
```
https://nexplayer.nexplayersdk.com/5.3/nexplayer.js
```
* **[Added]** Implement error events
* **[Added]** isFullscreen()

Date: Nov 25th 2020

#### Version 5.2.3
```
https://nexplayer.nexplayersdk.com/5.2.3/nexplayer.js
```
* **[Added]** Include new methods from AdsManager
* **[Improved]** Fix problem in ios when using full screen mode
* **[Improved]** Fix a minor issu when de audio keeps running in background
* **[Improved]** Fix pause doesnt work the first time in iOS
* **[Improved]** Fix controls autohide on first load.

Date: Nov 18th 2020

#### Version 5.2.1
```
https://nexplayer.nexplayersdk.com/5.2.1/nexplayer.js
```
* **[Improved]** possibility of locking the zoom
* **[Improved]** minor issue related with the double touch in ios
* **[Improved]** the placement of the controls has been corrected in some cases where the behavior was not correct

Date: Oct 26th 2020

#### Version 5.2
```
https://nexplayer.nexplayersdk.com/5.2/nexplayer.js
```
* **[Added]** getConfig
* **[Added]** getPlaybackSpeed
* **[Added]** getStreamType -> DASH/ HLS/ mp4 etc
* **[Added]** hasEnded
* **[Added]** isAd
* **[Added]** isPaused
* **[Added]** isPlaying
* **[Added]** isReady
* **[Added]** How to enable autoplay with sound on Chrome
* **[Improved]** Volume slider
* **[Improved]** Improve video 360
* **[Improved]** Full-Screen Mode on iPhone

Date: Oct 22nd 2020

#### Version 5.1.5
```
https://nexplayer.nexplayersdk.com/5.1.5/nexplayer.js
```
* **[Improved]** setCurrentTrack()
* **[Improved]** setThumbnailStep()
* **[Improved]** .addImpressionListener, .addClickListener, .addBlockedListener
* **[Improved]** getSurveyURL() and getMediaURL()
* **[Improved]** Playback bar for live videos
* **[Improved]** JumpForward(value), jumpBackward(value), seeklive(), getDVRWindowSize()
* **[Improved]** Change HTML5 spinner

Date: Sep 25th 2020

#### Version 5.1.4
```
https://nexplayer.nexplayersdk.com/5.1.4/nexplayer.js
```
* **[Improved]** Improve on Safari when playing multiple videos

Date: Sep 21th 2020

#### Version 5.1.2
```
https://nexplayer.nexplayersdk.com/5.1.2/nexplayer.js
```
* **[Improved]** Improve the reproduction in safari
* **[Improved]** Fix the problem with 360 and fairplay

Date: Sep 16th 2020

#### Version 5.1

<!-- <input type="text" value="https://nexplayer.nexplayersdk.com/4.2/nexplayer.js" id="myInput"> -->
```
https://nexplayer.nexplayersdk.com/5.1/nexplayer.js 
```
* **[Added]** setVolume method
* **[Added]** Automatic type360
* **[Added]** support 360 in oculus
* **[Added]** 360 zoom controls
* **[Added]** Certificated base64 in fairplay
* **[Added]** Implement watermark
* **[Improved]** Add event listener for ads start and ads end
* **[Improved]** Create event listeners for quality and playback rate change
* **[Improved]** Fix Dash Live issues
* **[Improved]** Fix DASH low latency for Mozilla
* **[Improved]** Solve bug related to the spinning wheel 
* **[Improved]** Solve bug with iphone ads

Date: Ago 26th 2020

#### Version 4.2

<!-- <input type="text" value="https://nexplayer.nexplayersdk.com/4.2/nexplayer.js" id="myInput"> -->
```
https://nexplayer.nexplayersdk.com/4.2/nexplayer.js 
```

* **[Added]** Multiple players
* **[Added]** New API calls
* **[Improved]** Full Screen iOS
* **[Improved]** Dash Live
* **[Improved]** Performance

#### Version 4.1.1
```
https://nexplayer.nexplayersdk.com/4.1.1/nexplayer.js
```

* **[Added]** Option for adding return button
* **[Added]** Player statistics displayed when writting "nex"
* **[Added]** Main color option
* **[Added]** Spinner when the video is buffering
* **[Added]** New target latency option
* **[Improved]** Fix Safari HLS issues
* **[Improved]** Fix DASH low latency for IE and Edge
* **[Improved]** Fix HLS and DASH for IE and Edge
* **[Improved]** General performance improvement

#### Version 4.0
```
https://nexplayer.nexplayersdk.com/4.0/nexplayer.js
```

* **[Added]** HLS + Widevine support
* **[Added]** Tizen Support
* **[Added]** WebOS Support
* **[Added]** Low Latency mode
* **[Added]** New UI design
* **[Added]** Quality controls
* **[Added]** Speed controls
* **[Added]** 360 support
* **[Added]** VR mode
* **[Added]** Mute option added
* **[Added]** Chromecast support
* **[Added]** VPAID and VAST support
* **[Improved]** API improvements
* **[Improved]** Improvement to Dash and Hls streams playback
* **[Improved]** Fixed minor issues to improve the player playback


#### Version 3.6
```
https://nexplayer.nexplayersdk.com/3.6/nexplayer.js
```

* **[Added]** AirPlay support preintegrated.
* **[Added]** Reactive icons.

#### Version 3.5

```
https://nexplayer.nexplayersdk.com/3.5/nexplayer.js
```

* **[Added]** Online license management (setting the customer key is now necessary).
* **[Added]** SDK hosted in a CDN.
* **[Improved]** Documentation snippets can be easily copied.

#### Version 3.4.2

* **[Added]** [Integrated UI] Documentation section about CORS.

#### Version 3.4.1

* **[Removed]** [Integrated UI] Sample without the integrated UI.

#### Version 3.4

* **[Added]** [Integrated UI] UnMount method to close the container and reuse it for a different video.

#### Version 3.3

* **[Added] [Integrated UI]** Static and dynamic preview thumbnails.
* **[Improved] [Integrated UI]** Volume management on phones and other devices where videos can only autoplay muted.
* **[Improved] [Integrated UI]** Resiliency for decoding errors while using HLS.
* **[Improved] [Integrated UI]** Loading symbol on Edge and IE when using videos with multiple audios.
* **[Improved] [Integrated UI]** Live symbol on some browsers.
* **[Improved] [Integrated UI]** Responsiveness of the sample code and the player UI when the container is resized.

#### Version 3.2

* **[Improved] [Integrated UI]** Extended documentation with examples.

#### Version 3.1

* **[Added] [Integrated UI]** VAST/VPAID support.
* **[Improved] [Integrated UI]** Responsive UI.

#### Version 3.0

* **[Added] [Integrated UI]** Customizable UI integrated inside the SDK.

#### Version 2.14

* **[Added]** Support macOS High Sierra.

#### Version 2.13

* **[Added]** Verimatrix Verspective Analytics.

#### Version 2.12

* **[Improved]** IE reliability.

#### Version 2.11

* **[Improved]** VAST reliability.

#### Version 2.10

* **[Added]** Custom HTTP headers also without DRM.

#### Version 2.9

* **[Improved]** Sample Chromecast receiver.

#### Version 2.8

* **[Improved]** Sample UI.
* **[Improved]** Sample code structure.

#### Version 2.7

* **[Added]** FreeWheel.
* **[Added]** Ad markers.

#### Verison 2.6

* **[Added]** Support attributes on the video tag.

#### Version 2.5

* **[Added]** Dynamic and Static thumbnails.
* **[Added]** CMAF on HLS.
* **[Improved]** HLS with audio only tracks on Safari Mac.

#### Version 2.4.1

* **[Added]** Sample UI for ABR management.
* **[Improved]** HLS resilience for unproperly format content.

#### Version 2.4

* **[Added]** TTML support for HLS.
* **[Added]** Agama integration.

#### Version 2.3.1

* **[Improved]** Incomplete TTML with images support with DASH.

#### Version 2.3

* **[Improved]** TTML with images support with DASH.
* **[Improved]** Preview thumbnails load time and reliability.
* **[Improved]** Sample full-screen with 360 videos on iOS.
* **[Improved]** Sample UI improvements.

#### Version 2.2.1

* **[Improved]** UI sample code

#### Version 2.2

* **[Added]** Preview Thumbnails.
* **[Improved]** WebVTT and CEA subtitle support.

#### Version 2.1

* **[Improved]** DASH live stream on Safari (Mac).
* **[Improved]** HLS WebVTT on Edge and IE.
* **[Improved]** General stability.

#### Version 2.0

* **[Added]** HLS support with TS content and DRMs.

#### Version 1.0

* **[Added]** DASH support including DRMs.
* **[Added]** 360 support.
* **[Added]** Initial release of the player.