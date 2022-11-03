# Releases

#### Version 8.1.0.1

* **[Improved]** Fixed problem with Fairplay DRM with ExpressPlay licence.

Date: November 3rd 2022

#### Version 8.1.0

* **[Improved]** Solved an issue with embedded subtitles.
* **[Improved]** Fixed the playback with some Fairplay streams work.
* **[Improved]** Solved an issue with DRM headers.
* **[Improved]** Fixed autoplay issue when it was deactivated and live streams were used. Now live stream won't start automatically if autoplay is set to false.
* **[Improved]** Solved issue with Dash streams.
* **[Improved]** Fixed buffer spinner shown when showingFullUI property is true.
* **[Added]** Add new method to change the current stream <a href="#/API?id=playerloadsource">loadSource(url)</a>
* **[Added]** Add new property in the Setup <a href="#/API?id=nexplayer-methods">maxFrameDrop</a> and new event <a href="#/API?id=nexevent">Frames_Drop_Capping.</a>
* **[Added]** Add new property in the Setup <a href="#/API?id=nexplayer-methods">licenseWithCredentials.</a>
* **[Added]** Add new property in the Setup <a href="#/API?id=nexplayer-methods">xhrSetHeader.</a>


Date: October 3rd 2022
#### Version 8.0.0

* **[Improved]** Solved an issue with the fake full screen on iOS.
* **[Improved]** Optimize memory usage on Dash.
* **[Added]** Support for CMCD as custom HTTP request header and as HTTP query argument.
* **[Added]** Support for Verimatrix watermark.
* **[Added]** Add a new event <a href="#/API?id=nexevent">Invalid_License</a> in the method <a href="#/API?id=playeroncallbacktype-functiontobecalled">on()</a>.

Date: May 25th 2022

#### Version 7.1.2

* **[Improved]** Fixed issue causing buffering with different audio/video segment durations.
* **[Improved]** Fixed content's requests that requires cookies to be played.

Date: January 17th 2022

#### Version 7.1.1

* **[Improved]** Fixed problem triggering "cuechange" event for EMSG metadata boxes.

Date: October 20th 2021

#### Version 7.1.0

* **[Improved]** Fixed ABR issues on HLS.
* **[Improved]** Fixed video playback after an ad starts.
* **[Improved]** Video plays when autoplay is set to false.
* **[Added]** Live thumbnail support on HLS streams.
* **[Added]** Live thumbnail support on DASH streams.
* **[Added]** <a href="#/API?id=getthumbnailat">getThumbnailAt()</a> method.

Date: October 11th 2021

#### Version 7.0.1

* **[Improved]** General improvements.

Date: September 9th 2021

#### Version 7.0.0

* **[Improved]** Fixed continuous buffering with DASH live streams.
* **[Improved]** Improved start time with HLS live streams that use PDT property.
* **[Improved]** Fixed bug regarding HLS streams quality change.
* **[Improved]** Fixed bug when reloading the player using HLS-LL streams.
* **[Improved]** Fixed error that made the main content play during an advertisement.

Date: August 13th 2021

#### Version 6.0.2

* **[Added]** Events to get info about loaded/buffered fragments on HLS. More info <a href="#/API?id=nexevent">here</a>.
* **[Added]** Unified DASH and HLS live settings into one setup parameter liveSettings (properties: liveDelay, maxDrift, playbackRate).
* **[Improved]** Changed misspelling of the property *FiledValue* to *FieldValue* in the <a href="#/API?id=NexHeaders">NexHeaders</a> object.
* **[Improved]** Fixed error with icons preventing from use 360 when video is stopped.
* **[Improved]** Fixed errors with some methods for live on VOD.

Date: July 30th 2021

#### Version 6.0.1

* **[Added]** forceOffset: Allows to select an offset for live HLS videos. The offset is a number which indicates how much segments the player should slide ahead the given segment number (EXT-X-MEDIA-SEQUENCE). This prevents player from stall if the presentation times between audio and video playlists are not perfectly synchronized.
* **[Improved]** Fixed buffering issues with some HLS videos.

Date: July 12nd 2021

#### Version 6.0.0

* **[Added]** HLS low latency.
* **[Added]** Reload method which allows the player to reload.
* **[Added]** Support for metadata over EMSG boxes for fMP4 segments in HLS.
* **[Improved]** Fixed issue regarding the duration when using MultiView.
* **[Improved]** Fixed ABR issue.
* **[Improved]** Fixed issue when using ad events listener.

Date: June 22nd 2021

#### Version 5.5.3.1

* **[Improved]** Solved setMediaKeys error while using ads.

Date: May 6th 2021

#### Version 5.5.3

* **[Added]** Support for multiple external subtitles.
* **[Added]** A custom-sized initial buffer can now be set by passing the desired number of seconds to achieve. It can be used through a new property, “startingBufferLength”, in the nexplayer Setup method.
* **[Improved]** UnMount performance when failed download data.
* **[Improved]** Bugs when ads are empty.

Date: Apr 30th 2021

#### Version 5.5.2

* **[Added]** hideVolumeIcon: Hide the volume icon for mobile devices. The volume is controlled by the device buttons.
* **[Added]** hiddenVolumeIcon(): Hides the volume icon.
* **[Added]** showVolumeIcon(): Shows the volume icon.
* **[Added]** Supporting drm with chromecast: dash and hls with Widevine and PlayReady.
* **[Improved]** Black screen when type_360 is false.

Date: March 18th 2021

#### Version 5.5.1

* **[Added]** hideOptionsUi: feature to hide some settings properties from the ui as the quality, speed ...

Date: March 8th 2021

#### Version 5.5.0

* **[Added]** MultiView, allows to see more than one stream at the same time
* **[Added]** Function for checking stream compatibility with the current used platform
* **[Added]** YouTube´s streams support
* **[Added]** allowScreenPlayPause: feature to disable the play/pause clicking on the screen
* **[Added]** defaultQuality: feature to start the video using the given default quality
* **[Added]** hideScreenPlay: feature to hide the play button which appears when the video is pausing
* **[Added]** Supporting multiple stream source: Selects a playable stream from an array of objects depending on the device and the browser
* **[Added]** Providing alternate streams as a backup: When a streams fails player is capable of skipping to the next provided stream that works
* **[Added]** disableAbr() method
* **[Added]** getVersion() method
* **[Added]** unMount and destroy for multiView
* **[Improved]** HLS Performance with low network
* **[Improved]** toggleBar() makes that the volume bar disappears too, now it has been solved

Date: March 8th 2021

#### Version 5.4.2

* **[Improved]** Volume controller
* **[Improved]** Cuechange events

Date: January 12th 2021

#### Version 5.4.1

* **[Added]** Error events
* **[Added]** dashSettings Option
* **[Added]** Callback to blockAt method
* **[Improved]** startFullscreen Option

Date: December 21st 2020

#### Version 5.4

* **[Added]** Picture in Picture Option
* **[Added]** useiOSFullScreen Option to use the native IOS full screen
* **[Improved]** Live button
* **[Improved]** startFullscreen Option

Date: December 10th 2020

#### Version 5.3

* **[Added]** Implement error events
* **[Added]** isFullscreen()

Date: November 25th 2020

#### Version 5.2.3

* **[Added]** Include new methods from AdsManager
* **[Improved]** Fix problem in ios when using full screen mode
* **[Improved]** Fix a minor issue when de audio keeps running in background
* **[Improved]** Fix pause doesn't work the first time in iOS
* **[Improved]** Fix controls autohide on first load.

Date: November 18th 2020

#### Version 5.2.1

* **[Improved]** possibility of locking the zoom
* **[Improved]** minor issue related with the double touch in ios
* **[Improved]** the placement of the controls has been corrected in some cases where the behavior was not correct

Date: October 26th 2020

#### Version 5.2

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

Date: October 22nd 2020

#### Version 5.1.5

* **[Improved]** setCurrentTrack()
* **[Improved]** setThumbnailStep()
* **[Improved]** .addImpressionListener, .addClickListener, .addBlockedListener
* **[Improved]** getSurveyURL() and getMediaURL()
* **[Improved]** Playback bar for live videos
* **[Improved]** JumpForward(value), jumpBackward(value), seeklive(), getDVRWindowSize()
* **[Improved]** Change HTML5 spinner

Date: September 25th 2020

#### Version 5.1.4

* **[Improved]** Improve on Safari when playing multiple videos

Date: September 21th 2020

#### Version 5.1.2

* **[Improved]** Improve the reproduction in safari
* **[Improved]** Fix the problem with 360 and fairplay

Date: September 16th 2020

#### Version 5.1

* **[Added]** setVolume method
* **[Added]** Automatic type360
* **[Added]** support 360 in oculus
* **[Added]** 360 zoom controls
* **[Added]** Certificated base64 in Fairplay
* **[Added]** Implement watermark
* **[Improved]** Add event listener for ads start and ads end
* **[Improved]** Create event listeners for quality and playback rate change
* **[Improved]** Fix Dash Live issues
* **[Improved]** Fix DASH low latency for Mozilla
* **[Improved]** Solve bug related to the spinning wheel
* **[Improved]** Solve bug with iphone ads

Date: August 26th 2020

#### Version 4.2

* **[Added]** Multiple players
* **[Added]** New API calls
* **[Improved]** Full Screen iOS
* **[Improved]** Dash Live
* **[Improved]** Performance

#### Version 4.1.1

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

* **[Added]** AirPlay support pre-integrated.
* **[Added]** Reactive icons.

#### Version 3.5

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
