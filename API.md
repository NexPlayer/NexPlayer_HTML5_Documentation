# NexPlayer API

## Nexplayer

**Type**: namespace
- Functions:
   - [.Setup(configuration)](#nexplayersetupconfiguration)
   - [.checkSupportedConfigurations(URL, DRMType)](#nexplayerchecksupportedconfigurations)
   - [.decodeData(data)](#nexplayerdecodedatadata)
   - [.Reload(configuration)](#nexplayerreloadconfiguration)

## Player

**Type**: global class
- Player
 - Instance
   - [.attachSubtitleRendererDiv(subtitleRendererDiv)](#playerattachsubtitlerendererdivsubtitlerendererdiv)
   - [.checkFrameDrop()](#playercheckframedrop) ⇒ number
   - [.clickFocus()](#playerclickFocus)
   - [.create360View()](#playercreate360view)
   - [.disableABR()](#playerdisableabr)
   - [.enableABR()](#playerenableabr)
   - [.enablePreviewThumbnails(option)](#playerenablepreviewthumbnailsoption)
   - [.enterPictureInPicture()](#enterpictureinpicture)
   - [.exitPictureInPicture()](#exitpictureinpicture)
   - [.FairPlayNexLicenseRequestFailed(event)](#playerfairplaynexlicenserequestfailedevent)
   - [.FairPlayNexLicenseRequestLoaded(event)](#playerfairplaynexlicenserequestloadedevent)
   - [.getAudioStreams()](#getaudiostreams) ⇒ [Array.< AudioStream >](#audiostream-object)
   - [.getConfig()](#getconfig)
   - [.getBufferLength()](#getbufferlength) ⇒ number
   - [.getCurrentAudioStream()](#getcurrentaudiostream) ⇒ [AudioStream](#audiostream-object)
   - [.getCurrentBuffer()](#playergetcurrentbuffer)
   - [.getCurrentLiveLatency()](#playergetcurrentlivelatency)
   - [.getCurrentLiveTime()](#getcurrentlivetime) ⇒ number
   - [.getCurrentSubtitle()](#getcurrentsubtitle)
   - [.getCurrentTime()](#getcurrenttime) ⇒ number
   - [.getCurrentTrack()](#getcurrenttrack) ⇒ [Track](#track-object)
   - [.getDuration()](#getduration) ⇒ number
   - [.getDVRWindowSize()](#getDVRWindowSize) ⇒ number
   - [.getManifestInfo()](#getmanifestinfo)
   - [.getPlaybackSpeed()](#getplaybackspeed)
   - [.getProtocol()](#getprotocol) ⇒ number
   - [.getQualityLevels()](#getqualitylevels) ⇒ array
   - [.getStreamType()](#getstreamtype)
   - [.getSubtitles()](#getsubtitles)
   - [.getThumbnailAt(number)](#getthumbnailat)
   - [.getThumbnailController()](#getthumbnailcontroller) ⇒ ThumbController
   - [.getTimeShiftBufferDepth()](#gettimeshiftbufferdepth) ⇒ number
   - [.getTimeUntilLive()](#gettimeuntillive) ⇒ number
   - [.getTracks()](#gettracks) ⇒ [Array.< Track >](#track-object)
   - [.getURL()](#playergeturl)
   - [.getVersion()](#getversion)
   - [.hasEnded()](#hasended)
   - [.hiddenVolumeIcon()](#hiddenvolumeicon)
   - [.isAd()](#isad)
   - [.isControlBarOpen()](#playeriscontrolbaropen)
   - [.isFullScreen()](#isfullscreen)
   - [.isLive()](#islive) ⇒ boolean
   - [.isPaused()](#ispaused)
   - [.isPictureInPicture()](#ispictureinpicture)
   - [.isPictureInPictureAvailable()](#ispictureinpictureavailable)
   - [.isPlaying()](#isplaying)
   - [.isReady()](#isready)
   - [.isUTC()](#isutc) ⇒ boolean
   - [.jumpBackward(value)](#playerjumpbackward)
   - [.jumpForward(value)](#playerjumpforward)
   - [.loadSource(url)](#playerloadsource)
   - [.nextFocus()](#playernextfocus)
   - [.on(callbackType, functionToBeCalled)](#playeroncallbacktype-functiontobecalled)
   - [.previousFocus()](#playerpreviousfocus)
   - [.seek(value)](#playerseekvalue)
   - [.seekLive()](#playerseekLive)
   - [.setAudioStream(streamID)](#playersetaudiostream)
   - [.setCurrentTrack(trackID)](#playersetcurrenttracktrackid)
   - [.setSpeed(speed)](#playersetspeedspeed)
   - [.setSubtitle(subID)](#playersetsubtitlesubid)
   - [.setThumbnailResources(callback, vttURl, imageURL)](#playersetthumbnailresourcescallback-vtturl-imageurl)
   - [.setThumbnailStep(step)](#playersetthumbnailstepstep)
   - [.showStats()](#playershowstats)
   - [.showVolumeIcon()](#showvolumeicon)
   - [.toggleBar()](#playertoggleBar)
   - [.toggleControlBar()](#playertogglecontrolbar)
   - [.toggleFullScreen()](#playertogglefullscreen)
   - [.toggleLanguagesMenu()](#playertogglelanguagesmenu)
   - [.togglePlayPause()](#playertoggleplaypause)
 - Ads
   - [.adManager()](#playeradmanager)
   - [.abort()](#playerabort)
   - [.addBlockedListener(func)](#playeraddblockedlistenerfunc)
   - [.addClickListener(func)](#playeraddclicklistenerfunc)
   - [.addCompleteListener(func)](#playeraddcomlpetelistenerfunc)
   - [.addErrorListener(func)](#playeradderrorlistenerfunc)
   - [.addFirstQuartileListener(func)](#playeraddfirstquartilelistenerfunc)
   - [.addImpressionListener(func)](#playeraddimpressionlistenerfunc)
   - [.addMidpointListener(func)](#playeraddmidpointlistenerfunc)
   - [.addPausedListener(func)](#playeraddpausedlistenerfunc)
   - [.addResumedListener(func)](#playeraddresumedlistenerfunc)
   - [.addSkippedListener(func)](#playeraddskippedlistenerfunc)
   - [.addStartedListener(func)](#playeraddstartedlistenerfunc)
   - [.addThirdQuartileListener(func)](#playeraddthirdquartilelistenerfunc)
   - [.addVolumeChangedListener(func)](#playeraddvolumechangedlistenerfunc)
   - [.addVolumeMutedListener(func)](#playeraddvolume)
   - [.destroy()](#playerdestroy)
   - [.discardAdBreak()](#playerdiscardadbreak)
   - [.focus()](#playerfocus)
   - [.getAdObject()](#playergetadobject)
   - [.getAdSkippableState()](#playergetadskippablestate)
   - [.getAdSystem()](#playergetadsystem)
   - [.getAdvertiserName()](#playergetadvertisername)
   - [.getApiFramework()](#playergetapiframework)
   - [.getContentType()](#playergetcontenttype)
   - [.getCreativeAdId()](#playergetcreativeadId)
   - [.getCreativeId()](#playergetcreativeid)
   - [.getCuePoints()](#playergetcuepoints)
   - [.getCurrentTime()](#playergetcurrenttime)
   - [.getDealId()](#playergetdealid)
   - [.getDescription()](#playergetdescription)
   - [.getDuration()](#playergetduration)
   - [.getHeight](#playergetheight)
   - [.getId()](#playergetid)
   - [.getMediaUrl()](#playergetmediaurl)
   - [.getMinSuggestedDuration()](#playergetminduggestedduration)
   - [.getRemainingTime()](#playergetremainingtime)
   - [.getSkipTime()](#playergetskiptime)
   - [.getSurveyURL()](#playergetsurveyurl)
   - [.getTitle()](#playergettitle)
   - [.getTraffickingParameters()](#gettraffickingparameters)
   - [.getTraffickingParametersString()](#gettraffickingparametersstring)
   - [.getUiElements()](#getuielements)
   - [.getUniversalAdIdRegistry()](#getuniversaladidregistry)
   - [.getUniversalAdIds()](#getuniversaladids)
   - [.getUniversalAdIdValue()](#getuniversaladidvalue)
   - [.getVastMediaBitrate()](#getvastmediabitrate)
   - [.getVastMediaHeight()](#getvastmediaheight)
   - [.getVastMediaWidth()](#getvastmediawidth)
   - [.getVolume()](#playergetvolume)
   - [.getWidth()](#getwidth)
   - [.getWrapperAdIds()](#getwrapperadids)
   - [.getWrapperAdSystems()](#getwrapperadsystems)
   - [.getWrapperCreativeIds()](#getwrappercreativeids)
   - [.init(width, height, viewMode, videoElement)](#playerinit)
   - [.isCustomPlaybackUsed()](#playeriscustomplaybackused)
   - [.isLinear()](#playerislinear)
   - [.isSkippable()](#playerisskippable)
   - [.isVpaid()](#playerisvpaid)
   - [.pause()](#playerpause)
   - [.play()](#playerplay)
   - [.resize](#playerresize)
   - [.setVolume()](#playersetvolume)
   - [.skip()](#playerskip)
 - Static
   - [NexEvent](#nexevent): enum
   - [NexProtocol](#nexprotocol): enum
   - [THUMB_TYPE](#thumbtype): enum
 - Global Typedefs
   - [AudioStream](#audiostream) : object
   - [Frame](#frame) : object
   - [NexCallback](#nexcallback) : object
   - [NexCallbackEvent](#nexcallbackevent) : object
   - [NexDRMInformation](#nexdrminformation) : object
   - [NexHeaders](#nexheaders) : object
   - [Track](#track) : object
 - VR Player
   - [.getFieldView()](#playergetFieldView)
   - [.setFieldView()](#playersetFieldView)
- Multiview
   - [.additionalVideo(info)](#multiviewAdditionalVideo)
   - [.addPlayer(player)](#multiviewAddPlayer)
   - [.Initialize()](#)
   - [.seek()](#multiviewSeek)
   - [.seekLive()](#multiviewSeekLive)
   - [.togglePlayPause()](#multiviewTogglePlayPause)
- YouTubePlayer
   - [.init()](#init)
   - [.URL()](#URL)

## Nexplayer methods

#### nexplayer.Setup(configuration)

Creates and initializes the player.

**Type**: function of [<code>nexplayer</code>](#Player)
**Param**:
   - **configuration** is an object which its properties values could be:

**Mandatory Parameters:**

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | NexPlayer key to validate the playback. |
| div | <code>HTMLDivElement</code> | Div container of the player. |
| src | <code>string</code> | Relevant src of the video to be played. |

**Optional Parameters:**

| Param | Type | Description |
| --- | --- | --- |
| allowScreenPlayPause | <code>boolean</code> | Allows to play and pause the video clicking on it. |
| autohide | <code>boolean</code> | Sets if the UI must hide when the user does not interact with the video. True by default. |
| autoplay | <code>boolean</code> | Determines if the video must start playing or paused. True by default. |
| blockZoom | <code>boolean</code> | Determines if the zoom in 360 videos is available or not. |
| callbackForLogger | <code>Function</code> | Function to be called when the logger shows a message. |
| callbackForReturn | <code>Function</code> | Sets a callback checkSupportedConfigurations(URL, DRMType) to be executed when the corresponding button is clicked. |
| callbacksForPlayer | <code>Function</code> | Used for retrieving the nexplayer instance and video element. This is necessary for getting the instance and use the NexPlayer API. |
| cast | <code>boolean</code> | Determines if the cast will be enabled or not. |
| chromecastEndImg | <code>string</code> | URL of an image to be used as ending. |
| chromecastLaunchImg | <code>string</code> | URL of an image to be used at launch. |
| debug | <code>boolean</code> | Determines if log information is showed. By default is set to true. |
| defaultQuality | <code>number</code> | Sets the starting track through its id. By default is -1, this enables the ABR. |
| disableFullscreen | <code>boolean</code> | Determines if the full screen will be enabled. |
| disableKeyEvents | <code>boolean</code> | Determines if the keyboard keys can be used to control the video (play/pause, forward/backward and volume up/down). |
| drm | <a href="#/API?id=NexDRMInformation"><code>Array\<NexDRMInformation></code></a> | Contains an array of DRM information. By default it's set to null. |
| externSubtitles | <code>Array</code> | Used to provide subtitle files as external subtitles. |
| hideOptionsUi | <code>Object</code> | Hides the setting that you choose from the UI. |
| hideScreenPlay | <code>boolean</code> | Hides the play button in the middle of the video, which appears when the video is paused. |
| hideVolumeIcon | <code>boolean</code> |  Determines if the volume icon will be hidden for mobile devices. The volume is controlled by the device buttons. |
| lowLatency | <code>boolean</code> |  Determines if the low latency will be enabled. |
| liveSettings | <code>Object</code> | Settings to control live playback. Requires low latency. |
| logosrc | <code>string</code> | Company URL logo. |
| mutedAtStart | <code>boolean</code> | Determines if the video will start playing muted or not. By default this value is set to false. |
| pip | <code>boolean</code> | Determines if picture-in-picture will be enabled. |
| poster | <code>string</code> | Video poster URL.  |
| seekUI | <code>number</code> | Sets the number of seconds the UI buttons will seek forwards or backwards. Set to 10s by default. |
| showingFullUI | <code>boolean</code> | Determines if the UI is hidden or not. |
| showUI360 | <code>boolean</code> | Determines if the 360UI will be enabled. |
| srcSets | <code>Array</code> | Array of objects that contains a stream and an optional DRM.
| staticThumbnailsImage | <code>string</code> | Image to extract thumbnails from. |
| staticThumbnailsVTT | <code>string</code> | Used to provide the player an external thumbnails VTT file. |
| startingBufferLength | <code>number</code> | Determines the buffer that the video should have before start. |
| startFullscreen | <code>boolean</code> | Determines if the video will start on full screen. |
| subtitle | <code>string</code> | Video subtitle name. |
| timeUI | <code>boolean</code> | Determines if the video time will be hidden on the UI. |
| title | <code>string</code> | Video name. |
| type_360 | <code>string</code> | Selects the 360 video format to play. Possible values are 'equirectangular', 'cubemap' and 'topdown'. |
| useDynamicThumbnails | <code>boolean</code> | Determines if dynamic thumbnails are used. By default this value is set to false. |
| useiOSFullScreen | <code>boolean</code> | Determines if the iOS native full screen will be used. |
| vast | <code>string</code> | Advertisement URL that is going to be played. VAST, VPAID and VMAP are supported. |
| watermark | <code>Object</code> | Watermark image URL. |
| withCredentials | <code>boolean</code> | Indicates whether or not cross-site Access-Control requests should be made using credentials such as cookies, authorization headers or TLS client certificates. |
| cmcd | <code>Object</code> |  Enables the Common Media Client Data. Only needs to create an empty object to enable it. |
|licenseWithCredentials| <code>boolean</code> | Indicates whether or not cross-site Access-Control requests should be made using credentials such as cookies, authorization headers or TLS client certificates with DRM.|
| maxFrameDrop | <code>number</code> | The value of this property should be within the range 0 - 1. A <a href="#/API?id=nexevent">Frames_Drop_Capping</a> event will be triggered whenever the percentage of frames dropped is higher than this threshold.|
| xhrSetHeader | <code>Array</code> | You can configure the headers that are necessary for the URL request.|

<a id="nexplayerchecksupportedconfigurations"></a>

#### nexplayer.checkSupportedConfigurations(URL, DRMType)

Check if the audio and video codecs and DRMType, if it is provided, are supported by the device.

**Type**: function of [<code>nexplayer</code>](#Player)
**Params**:
   - **URL**: manifest URL of the video.
   - **DRMType**: optional type of DRM (e.g., "com.microsoft.playready" )
**Returns**: A Promise. If it is resolved returns a MediaKeySystemAccess object with the supported codecs, and if it is rejected returns a string with the error.

#### nexplayer.Reload(configuration)

Reloads the player with the given configuration. If the configuration object is not provided the previous one will be used. If it is provided the properties passed will override the values of the previous configuration object.

**Type**: function of [<code>nexplayer</code>](#Player)
**Param**:
   - **configuration** is an object which its properties values could be:

**Mandatory Parameters:**

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | NexPlayer key to validate the playback. |
| div | <code>HTMLDivElement</code> | Div container of the player. |
| src | <code>string</code> | Relevant src of the video to be played. |

**Optional Parameters:**

| Param | Type | Description |
| --- | --- | --- |
| allowScreenPlayPause | <code>boolean</code> | Allows to play and pause the video clicking on it. |
| autohide | <code>boolean</code> | Sets if the UI must hide when the user does not interact with the video. True by default. |
| autoplay | <code>boolean</code> | Determines if the video must start playing or paused. True by default. |
| blockZoom | <code>boolean</code> | Determines if the zoom in 360 videos is available or not. |
| callbackForLogger | <code>Function</code> | Function to be called when the logger shows a message. |
| callbackForReturn | <code>Function</code> | Sets a callback checkSupportedConfigurations(URL, DRMType) to be executed when the corresponding button is clicked. |
| callbacksForPlayer | <code>Function</code> | Used for retrieving the nexplayer instance and video element. This is necessary for getting the instance and use the NexPlayer API. |
| cast | <code>boolean</code> | Determines if the cast will be enabled or not. |
| chromecastEndImg | <code>string</code> | URL of an image to be used as ending. |
| chromecastLaunchImg | <code>string</code> | URL of an image to be used at launch. |
| debug | <code>boolean</code> | Determines if log information is showed. By default is set to true. |
| defaultQuality | <code>number</code> | Sets the starting track through its id. By default is -1, this enables the ABR. |
| disableFullscreen | <code>boolean</code> | Determines if the full screen will be enabled. |
| disableKeyEvents | <code>boolean</code> | Determines if the keyboard keys can be used to control the video (play/pause, forward/backward and volume up/down). |
| drm | <a href="#/API?id=NexDRMInformation"><code>Array\<NexDRMInformation></code></a> | Contains an array of DRM information. By default it's set to null. |
| externSubtitles | <code>Array</code> | Used to provide subtitle files as external subtitles. |
| hideOptionsUi | <code>Object</code> | Hides the setting that you choose from the UI. |
| hideScreenPlay | <code>boolean</code> | Hides the play button in the middle of the video, which appears when the video is paused. |
| hideVolumeIcon | <code>boolean</code> |  Determines if the volume icon will be hidden for mobile devices. The volume is controlled by the device buttons. |
| lowLatency | <code>boolean</code> |  Determines if the low latency will be enabled. |
| liveSettings | <code>Object</code> | Settings to control live playback. Requires low latency. |
| logosrc | <code>string</code> | Company URL logo. |
| mutedAtStart | <code>boolean</code> | Determines if the video will start playing muted or not. By default this value is set to false. |
| pip | <code>boolean</code> | Determines if picture-in-picture will be enabled. |
| poster | <code>string</code> | Video poster URL.  |
| seekUI | <code>number</code> | Sets the number of seconds the UI buttons will seek forwards or backwards. Set to 10s by default. |
| showingFullUI | <code>boolean</code> | Determines if the UI is hidden or not. |
| showUI360 | <code>boolean</code> | Determines if the 360UI will be enabled. |
| srcSets | <code>Array</code> | Array of objects that contains a stream and an optional DRM.
| staticThumbnailsImage | <code>string</code> | Image to extract thumbnails from. |
| staticThumbnailsVTT | <code>string</code> | Used to provide the player an external thumbnails VTT file. |
| startingBufferLength | <code>number</code> | Determines the buffer that the video should have before start. |
| startFullscreen | <code>boolean</code> | Determines if the video will start on full screen. |
| subtitle | <code>string</code> | Video subtitle name. |
| timeUI | <code>boolean</code> | Determines if the video time will be hidden on the UI. |
| title | <code>string</code> | Video name. |
| type_360 | <code>string</code> | Selects the 360 video format to play. Possible values are 'equirectangular', 'cubemap' and 'topdown'. |
| useDynamicThumbnails | <code>boolean</code> | Determines if dynamic thumbnails are used. By default this value is set to false. |
| useiOSFullScreen | <code>boolean</code> | Determines if the iOS native full screen will be used. |
| vast | <code>string</code> | Advertisement URL that is going to be played. VAST, VPAID and VMAP are supported. |
| watermark | <code>object</code> | Watermark image URL. |
| withCredentials | <code>boolean</code> | Indicates whether or not cross-site Access-Control requests should be made using credentials such as cookies, authorization headers or TLS client certificates. |
| cmcd | <code>Object</code> |  Enables the Common Media Client Data. Only needs to create an empty object to enable it. |
|licenseWithCredentials| <code>boolean</code> | Indicates whether or not cross-site Access-Control requests should be made using credentials such as cookies, authorization headers or TLS client certificates with DRM.|
| maxFrameDrop | <code>number</code> | The value of this property should be within the range 0 - 1. A <a href="#/API?id=nexevent">Frames_Drop_Capping</a> event will be triggered whenever the percentage of frames dropped is higher than this threshold.|
| xhrSetHeader | <code>Array</code> | You can configure the headers that are necessary for the URL request.|

#### nexplayer.decodeData(data)

Decodes an ArrayBuffer and converts it into a string. END OF TEXT (\u0003) and NULL (\u0000) unicode characters are cleaned.

**Type**: function of [<code>nexplayer</code>](#Player)

**Param**:
   - **data** is the ArrayBuffer to decode.

**Returns**: decoded and cleaned string or null if the parameter provided is not an ArrayBuffer.

## Player methods and objects

<a id="gettracks"> </a>
   #### player.getTracks() ⇒ Array.< Track >

Gets all of the videoes avaliable tracks (different qualities).

**Type**: instance method of [<code>Player</code>](#Player)
**Returns**: Array.< Track > - all the tracks available.

<a id="getcurrenttrack"> </a>
   #### player.getCurrentTrack() ⇒ Track

Get the current track information.

**Type**: instance method of [<code>Player</code>](#Player)
**Returns**: Track - the current track.

#### player.setCurrentTrack(trackID)

Sets the current track.

**Type**: instance method of [<code>Player</code>](#Player)
**Export**:

| Param | Type | Description |
| --- | --- | --- |
| trackID | <code>number</code> | ID of the track to be used. |

#### player.enableABR()

Enables the ABR to change automatically between tracks.

**Type**: instance method of [<code>Player</code>](#Player)

#### player.disableABR()

Disables the ABR to prevent the player from changing tracks regardless of bandwidth.

**Type**: instance method of [<code>Player</code>](#Player)

<a id="getaudiostreams"> </a>
   #### player.getAudioStreams() ⇒ Array.< AudioStream >

Get the available audio streams.

**Type**: instance method of [<code>Player</code>](#Player)
**Returns**: An array<AudioStream> - which contains the available audio streams.

<a id="getcurrentaudiostream"> </a>
   #### player.getCurrentAudioStream() ⇒ AudioStream

Get the audio stream currently in use.

**Type**: instance method of [<code>Player</code>](#Player)
**Returns**: AudioStream - the current audio track.

#### player.setAudioStream(streamID)

Sets the current audio stream.

**Type**: instance method of [<code>Player</code>](#Player)
**Export**:

| Param | Type | Description |
| --- | --- | --- |
| streamID | <code>number</code> | ID of the audio stream to be used. |


<a id="getcurrentsubtitle"> </a>
   #### player.getCurrentSubtitle()

Gets the current subtitle info.

**Type**: instance method of [<code>Player</code>](#Player)
**Returns**: Current Subtitle - the current subtitle track (undefined if no subtitles are activated).

<a id="getsubtitles"> </a>
   #### player.getSubtitles()

Gets all the avaliable subtitle tracks info.

**Type**: instance method of [<code>Player</code>](#Player)
**Returns**: Array of subtitles - the subtitle tracks of the video.

#### player.setSubtitle(subID)

Sets the current subtitle track.

**Type**: instance method of [<code>Player</code>](#Player)
**Export**:

| Param | Type | Description |
| --- | --- | --- |
| subID | <code>number</code> | ID of the subtitle track to be used |


<a id="islive"> </a>
   #### player.isLive() ⇒ boolean

Informs whether the video is live or on demand (VOD). This needs to be called when the manifest is finally loaded.
It is recommended to use within the video "loadeddata" event.

**Type**: instance method of [<code>Player</code>](#Player)
**Returns**: boolean - true if the video is live, otherwise it returns false.


#### player.on(callbackType, functionToBeCalled)

Adds a listener for Events.

**Type**: instance method of [<code>Player</code>](#Player)
**Export**:

| Param | Type | Description |
| --- | --- | --- |
| callbackType | <a href="#/API?id=nexevent"><code>NexEvent</code></a> | Event to listen for |
| functionToBeCalled	 | <code>NexCallbackEvent</code> | 	Function called on each event |

#### player.attachSubtitleRendererDiv(subtitleRendererDiv)

Adds a DIV to render certain subtitles in a more precise way. This is optional and the native subtitles of the video element will be used if this is not set.

**Type**: instance method of [<code>Player</code>](#Player)
**Export**:

| Param | Type | Description |
| --- | --- | --- |
| subtilteRendererDiv | <code>SubtitleRendererDiv</code> | DIV to render some advanced subtitles |

#### player.create360View()

Creates the 360 view.

**Type**: instance method of [<code>Player</code>](#Player)


#### player.FairPlayNexLicenseRequestLoaded(event)

Called when the FairPlay request is done.

**Type**: instance method of [<code>Player</code>](#Player)
**Export**:

| Param | Description |
| --- | --- |
| event | Event |

#### player.FairPlayNexLicenseRequestFailed(event)

Called if the FairPlay request fails.

**Type**: instance method of [<code>Player</code>](#Player)
**Export**:

| Param | Description |
| --- | --- |
| event | Event |


#### player.setThumbnailResources(callback, vttURl, imageURL)

Sets thumbnail resources. This method should be called before Init().


**Type**: instance method of [<code>Player</code>](#Player)
**Export**:

| Param | Type | Description |
| --- | --- | --- |
| callback | <code>NexCallbackEvent</code> | function called when the thumbnails are loaded |
| vttURl	 | <code>String</code> | 	path to the .vtt thumbnails file |
| imageURL	 | <code>String</code> | 	path to the thumbnails image file |



<a id="isutc"> </a>
   #### player.isUTC() ⇒ boolean

   Indicates whether the video information (currentTime, duration, seekable range, etc.) of the video element is based on the present or on an absolute value that starts at midnight UTC, Jan 1, 1970. If this is true, you will need to take this into account when seeking through the currentTime of the video element. Some useful methods (like getCurrentTime, getDuration, and seek) are available to reduce the complexity in these cases. Note that this property only applies to live streams.

   **Type**: instance method of [<code>Player</code>](#Player)
   **Returns**: boolean - true if the video information is using UTC, false otherwise.


<a id="getcurrenttime"> </a>
   #### player.getCurrentTime() ⇒ number

   Returns the currentTime taking into account isUTC (if isUTC is true, getCurrentTime's returned value will be different from the time of the video element).

   **Type**: instance method of [<code>Player</code>](#Player)
   **Returns**: number - the current time of the video.

<a id="getduration"> </a>
   #### player.getDuration() ⇒ number

   Returns the duration taking into account isUTC (if isUTC is true, getDuration's returned value will be different from the duration of the video element).

   **Type**: instance method of [<code>Player</code>](#Player)
   **Returns**: number - the duration of the video.

<a id="getDVRWindowSize"> </a>
   #### player.getDVRWindowSize() ⇒ number

   Returns the window of allowable play time behind the live point of a live stream, this value will increase until the buffer is full, with the full content, at that point of time, the value will be constant.

   **Type**: instance method of [<code>Player</code>](#Player)
   **Returns**: number - the window of allowable play time behind the live point of a live stream.

#### player.getURL()

  Returns the current video URL.

  **Type**: instance method of [<code>Player</code>](#Player)
  **Returns**: String

<a id="playercheckframedrop"> </a>
   #### player.checkFrameDrop() ⇒ number

   Returns the number of dropped frames as proxy for CPU load

   **Type**: instance method of [<code>Player</code>](#Player)
   **Returns**: number - number of dropped frames.



#### player.seek(value)


   Sets the currentTime property of the attached video element. (if isUTC is true, the seek value will be in a different format than the currentTime of the video element).

   **Type**: instance method of [<code>Player</code>](#Player)

  | Param | Type |Description |
  | --- | --- | --- |
  | event | Event | value in seconds that the player will seek to. |

  ```js
   //Non-live video
   player.seek(120) // This will seek forward 120 seconds (2:00 minutes), must be a positive number ranging from 0 to the full duration of the video in seconds
   //Live video
   player.seek(-120) // It jumps back 120 seconds (2:00 minutes) from the current live time, must be a negative number ranging from minus {the DVR window size} to 0
   ```

#### player.seekLive()

   Jump to the livestream current time from the current position (if isUTC is true, the seek value will be in a different format than the currentTime of the video element). Only works on livestreams.

   **Type**: instance method of [<code>Player</code>](#Player)

<a id="getbufferlength"> </a>
#### player.getBufferLength() ⇒ number

Returns the seconds of buffer loaded that the player has available to play.

**Type**: instance method of [<code>Player</code>](#Player)
**Returns**: number - time of buffer length

<a id="getcurrentlivetime"> </a>
#### player.getCurrentLiveTime() ⇒ number

Returns the time in which the livestream is at.

**Type**: instance method of [<code>Player</code>](#Player)
**Returns**: number - time in which the livestream is at.

<a id="gettimeuntillive"> </a>
#### player.getTimeUntilLive() ⇒ number

Returns the time difference between the current video time and the livestream time.

**Type**: instance method of [<code>Player</code>](#Player)
**Returns**: number - time difference between the time it's currently found in and the time the livestream is at.

<a id="getmanifestinfo"> </a>
#### player.getManifestInfo()

Returns some information about the manifest.

**Type**: instance method of [<code>Player</code>](#Player)
**Returns**: number - some information about the manifest.

<a id="gettimeshiftbufferdepth"> </a>
#### player.getTimeShiftBufferDepth ⇒ number

Returns the time shift buffer depth in seconds, this function only works in live streams.

**Type**: instance method of [<code>Player</code>](#Player)
**Returns**: number - time shift buffer depth

<a id="getprotocol"> </a>
#### player.getProtocol() ⇒ number

Returns the protocol type.

**Type**: instance method of [<code>Player</code>](#Player)
**Returns**: number - the protocol type.

<a id="getthumbnailcontroller"> </a>
#### player.getThumbnailController() ⇒ ThumbController

Returns the preview thumbnail controller.

**Type**: instance method of [<code>Player</code>](#Player)
**Returns**: ThumbController - Thumbnail controller

#### player.setThumbnailStep(step)

Sets the time interval between frames for dynamic thumbnails.

**Type**: instance method of [<code>Player</code>](#Player)

  | Param | Type |Description |
  | --- | --- | --- |
  | step | number | The seconds between two different thumbnails. |

#### player.enablePreviewThumbnails(option)

Enable thumbnails preview. This method must be called before Init().

**Type**: instance method of [<code>Player</code>](#Player)

 | Param | Type |Description |
 | --- | --- | --- |
 | option | boolean | The value that enable or not the thumbnails. |

#### player.setSpeed(speed)

Set the video playback speed.

**Type**: instance method of [<code>Player</code>](#Player)

 | Param | Type |Description |
 | --- | --- | --- |
 | speed | number | The speed value. |

<a id="getqualitylevels"> </a>
#### player.getQualityLevels() ⇒ array

Get the video quality levels array.

**Type**: instance method of [<code>Player</code>](#Player)
**Returns**: array - quality levels array info

#### player.togglePlayPause()

Plays or pauses the playback.

**Type**: instance method of [<code>Player</code>](#Player)

#### player.toggleFullScreen()

Toggles between full screen or window mode.

**Type**: instance method of [<code>Player</code>](#Player)

<a id="playershowstats"></a>

#### player.showStats()

Displays basic stream information when typing "nex" on the keyboard.

**Type**: instance method of  [<code>Player</code>](#Player)

<a id="playerjumpforwardvalue"></a>

#### player.jumpForward(value)

Jumps forward to the current playback position of the player.

**Type**: instance method of  [<code>Player</code>](#Player)
**Param**: {number} **value** is the number of seconds to jump forward

<a id="playerjumpbackwardvalue"></a>

#### player.jumpBackward(value)

Jumps backward to the current playback position of the player.

**Type**: instance method of  [<code>Player</code>](#Player)
**Param**: {number} **value** is the number of seconds to jump backward

<a id="playersetthumbnailstepstep"></a>

#### player.setThumbnailStep(step)

Sets the step for dynamic thumbnails.

**Type**: instance method of  [<code>Player</code>](#Player)
**Param**: {number} **step** is the seconds between two different thumbnails

<a id="playergetcurrentlivelatency"></a>

#### player.getCurrentLiveLatency()

Returns the live latency value.

**Type**: instance method of  [<code>Player</code>](#Player)
**Returns**: latency number of seconds

<a id="playergetcurrentbuffer"></a>

#### player.getCurrentBuffer()

Returns the current buffer level.

**Type**: instance method of  [<code>Player</code>](#Player)

<a id="playeriscontrolbaropen"></a>

#### player.isControlBarOpen()

Returns if the control bar is opened.

**Type**: instance method of  [<code>Player</code>](#Player)
**Returns**: boolean

<a id="playertogglelanguagesmenu"></a>

#### player.toggleLanguagesMenu()

Toggles the subtitle menu options.

**Type**: instance method of  [<code>Player</code>](#Player)

<a id="playerloadsource"></a>

#### player.loadSource(url)

Change the URL of the content without changing the instance.

**Type**: instance method of  [<code>Player</code>](#Player)

<a id="playernextfocus"></a>

#### player.nextFocus()

Moves along to the next element that can be focused. The possible elements to be focused are:
'nexplayer_play_pause', 'nexplayer_full_volume_div', 'nexplayer_language', 'nexplayer_full_screen', 'nexplayer_return_container'

**Type**: instance method of  [<code>Player</code>](#Player)

<a id="playerpreviousfocus"></a>

#### player.previousFocus()

Moves along to the previous element that can be focused. The possible elements to be focused are:
'nexplayer_play_pause', 'nexplayer_full_volume_div', 'nexplayer_language', 'nexplayer_full_screen', 'nexplayer_return_container'.

**Type**: instance method of  [<code>Player</code>](#Player)

<a id="playerclickfocus"></a>

#### player.clickFocus()

Click the current focused element.

**Type**: instance method of  [<code>Player</code>](#Player)

<a id="playertogglebar"></a>

#### player.toggleBar()

Hides or shows the playback bar.

**Type**: instance method of [<code>Player</code>](#Player)

<a id="isfullscreen"></a>

#### player.isFullScreen()

Informs if the video is full screen or not

**Type**: instance method of Player.[<code>Player</code>](#Player)

**Returns**: boolean - true if the video is fullscreen, otherwise it returns false.

<a id="getconfig"></a>

#### player.getConfig()

Returns the parameters defined in the set up, for that video

**Type**: instance method of Player.[<code>Player</code>](#Player)

<a id="getplaybackspeed"></a>

#### player.getPlaybackSpeed()

Returns the play back speed.

**Type**: instance method of  [<code>Player</code>](#Player)
**Returns**: Number

<a id="getstreamtype"></a>

#### player.getStreamType()

Returns the type of video (DASH/ HLS/ mp4 ...)

**Type**: instance method of  [<code>Player</code>](#Player)
**Returns**: String

<a id="hasended"></a>

#### player.hasEnded()

Returns true if the video has ended.

**Type**: instance method of  [<code>Player</code>](#Player)
**Returns**: boolean

<a id="isad"></a>

#### player.isAd()

Returns true while an ad is played back or content playback has been paused for ad playback, false otherwise.

**Type**: instance method of  [<code>Player</code>](#Player)
**Returns**: boolean

<a id="ispaused"></a>

#### player.isPaused()

Returns true if the video state is paused, otherwise false

**Type**: instance method of  [<code>Player</code>](#Player)
**Returns**: boolean

<a id="isplaying"></a>

#### player.isPlaying()

Returns true if the video state is playing, otherwise false

**Type**: instance method of  [<code>Player</code>](#Player)
**Returns**: boolean

<a id="isready"></a>

#### player.isReady()

Returns true if the player has finished initialization and is ready to use and to handle other API calls.

**Type**: instance method of  [<code>Player</code>](#Player)
**Returns**: boolean

<a id="enterpictureinpicture"></a>

#### player.enterPictureInPicture()

To enter picture in picture mode

**Type**: instance method of  [<code>Player</code>](#Player)

<a id="exitpictureinpicture"></a>

#### player.exitPictureInPicture()

To exit picture in picture mode

**Type**: instance method of  [<code>Player</code>](#Player)

<a id="ispictureinpicture"></a>

#### player.isPictureInPicture()

Returns true if the video is in picture in picture, otherwise false.

**Type**: instance method of  [<code>Player</code>](#Player)
**Returns**: boolean

<a id="ispictureinpictureavailable"></a>

#### player.isPictureInPictureAvailable()

Return true if pictur in pictur mode is supported for the browser, otherwise false.

**Type**: instance method of  [<code>Player</code>](#Player)
**Returns**: boolean

<a id="getversion"></a>

#### player.getVersion()

Returns the version of the SDK.

**Type**: instance method of  [<code>Player</code>](#Player)
**Returns**: String

<a id="hiddenvolumeicon"></a>

#### player.hiddenVolumeIcon()

Hides the volume icon.

**Type**: instance method of  [<code>Player</code>](#Player)

<a id="showvolumeicon"></a>

#### player.showVolumeIcon()

Shows the volume icon.

**Type**: instance method of  [<code>Player</code>](#Player)

#### <a id="getthumbnailat"></a> player.getThumbnailAt(number)

Get the thumbnail at a specific video time.

| Param | Type | Description |
| --- | --- | --- |
| Time | <code>number</code> | Get thumbnails at the given time. |

**Type**: instance method of [<code>Player</code>](#Player)

**Returns**: Promise <Frame, object> - <a href="#/API?id=frame">Frame</a> as resolve, and object which contains details as a reject.

## Ad methods

<a id="playeradmanager"></a>

#### player.adManager()

Returns the AdManager instance in order to perform actions on ads through the IMA SDK.

**Type**: instance method of  [<code>Player</code>](#Player)
**Returns**: AdManager object

<a id="playergetadobject"></a>

#### player.adManager().getAdObject()

Returns the IMA SDK manager object.

**Type**: instance method of  [<code>Player</code>](#Player)
**Returns**: IMAs AdManager object

<a id="playergetid"></a>

#### player.adManager().getId()

Returns the ID of the current ad.

**Type**: instance method of  [<code>Player</code>](#Player)
**Returns**: String

<a id="playergettitle"></a>

#### player.adManager().getTitle()

Returns the title of the current ad.

**Type**: instance method of  [<code>Player</code>](#Player)
**Returns**: String

<a id="playergetdescription"></a>

#### player.adManager().getDescription()

Returns the description of the current ad.

**Type**: instance method of  [<code>Player</code>](#Player)
**Returns**: String

<a id="playergetmediaurl"></a>

#### player.adManager().getMediaUrl()

Returns the video ad URL.

**Type**: instance method of  [<code>Player</code>](#Player)
**Returns**: String

<a id="playergetsurveyurl"></a>

#### player.adManager().getSurveyURL()

Returns the ad survey URL.

**Type**: instance method of  [<code>Player</code>](#Player)
**Returns**: String

<a id="playergetduration"></a>

#### player.adManager().getDuration()

Returns the total duration of the current ad.

**Type**: instance method of  [<code>Player</code>](#Player)
**Returns**: number

<a id="playergetskiptime"></a>

#### player.adManager().getSkipTime()

Returns how much time is left until the user can skip the ad (only if it is skippable).

**Type**: instance method of  [<code>Player</code>](#Player)
**Returns**: number

<a id="playergetcurrenttime"></a>

#### player.adManager().getCurrentTime()

Returns the current time position of the ad.

**Type**: instance method of  [<code>Player</code>](#Player)
**Returns**: number

<a id="playergetcontenttype"></a>

#### player.adManager().getContentType()

Returns the ad video type (e.g. "video/mp4").

**Type**: instance method of  [<code>Player</code>](#Player)
**Returns**: String

<a id="playerisskippable"></a>

#### player.adManager().isSkippable()

Returns whether the ad is skippable or not.

**Type**: instance method of  [<code>Player</code>](#Player)
**Returns**: boolean

<a id="playerislinear"></a>

#### player.adManager().isLinear()

Returns whether the ad is linear or not.

**Type**: instance method of  [<code>Player</code>](#Player)
**Returns**: boolean

<a id="playerisvpaid"></a>

#### player.adManager().isVpaid()

Returns whether the ad is in the VPAID format or not.

**Type**: instance method of  [<code>Player</code>](#Player)
**Returns**: boolean

<a id="playerpause"></a>

#### player.adManager().pause()

Pauses the ad.

**Type**: instance method of  [<code>Player</code>](#Player)

<a id="playerplay"></a>

#### player.adManager().play()

Plays the ad when it is paused.

**Type**: instance method of  [<code>Player</code>](#Player)

<a id="playerskip"></a>

#### player.adManager().skip()

Skips the ad (if possible).

**Type**: instance method of  [<code>Player</code>](#Player)

<a id="playerabort"></a>

#### player.adManager().abort()

Closes the ad and starts the video.

**Type**: instance method of  [<code>Player</code>](#Player)

<a id="playersetvolume"></a>

#### player.adManager().setVolume(value)

Set the volume for the current ad.

**Type**: instance method of  [<code>Player</code>](#Player)


| Param | Type | Description |
| --- | --- | --- |
| value | <code>number</code> | The volume to set, from 0 (muted) to 1 (loudest). |

<a id="playerdestroy"></a>

#### player.adManager().destroy()

Removes ad assets loaded at runtime that need to be properly removed at the time of ad completion and stops the ad and all tracking.

**Type**: instance method of  [<code>Player</code>](#Player)
<a id="playerdiscardadbreak"></a>

#### player.adManager().discardAdBreak()

If an ad break is currently playing, discard it and resume content. Otherwise, ignore the next scheduled ad break. For example, this can be called immediately after the ads manager loads to ignore a preroll without losing future midrolls or postrolls. This is a no-op unless the ad request returned a playlist or VMAP response.

**Type**: instance method of  [<code>Player</code>](#Player)
<a id="playerfocus"></a>

#### player.adManager().focus()

Puts the focus on the skip button, if exists. Otherwise, the focus is put on interactive elements, including icons or interactive creatives.

**Type**: instance method of  [<code>Player</code>](#Player)
<a id="playergetadskippablestate"></a>

#### player.adManager().getAdSkippableState()

Returns true if the current ad can be skipped.

**Return**: <code>boolean</code> True if the current ad can be skipped, false otherwise.

**Type**: instance method of  [<code>Player</code>](#Player)
<a id="playergetcuepoints"></a>

#### player.adManager().getCuePoints()

Returns an array of offsets in seconds indicating when a scheduled ad break will play. A preroll is represented by 0, and a postroll is represented by -1. An empty array indicates the ad or ad pod has no schedule and can be played at any time.

**Return** <code>non-null Array of number</code> List of time offsets in seconds.

**Type**: instance method of  [<code>Player</code>](#Player)
<a id="playergetremainingtime"></a>

#### player.adManager().getRemainingTime()

Get the remaining time of the current ad that is playing. If the ad is not loaded yet or has finished playing, the API would return -1.

**Return** <code>number</code> Returns the time remaining for current ad. If the remaining time is undefined for the current ad (for example custom ads), the value returns -1.

**Type**: instance method of  [<code>Player</code>](#Player)
<a id="playergetvolume"></a>

#### player.adManager().getVolume()

Get the volume for the current ad.

**Return** <code>number</code> The volume of the current ad, from 0 (muted) to 1 (loudest).

**Type**: instance method of  [<code>Player</code>](#Player)
<a id="playerinit"></a>

#### player.adManager().init(width, height, viewMode, videoElement)

Call init to initialize the ad experience on the ads manager.

Get the volume for the current ad.

| Param | Type | Description |
| --- | --- | --- |
| width | <code>number</code> | The desired width of the ad. |
| height | <code>number</code> | The desired height of the ad. |
| viewMode | <code>viewMode</code> | The desired view mode. Value must not be null. |
| videoElement | <code>Optional</code> | HTMLVideoElement The video element for custom playback. This video element overrides the one provided in the AdDisplayContainer constructor. Only use this property if absolutely necessary - otherwise we recommend specifying this video element while creating the AdDisplayContainer. Value may be null. |

**Type**: instance method of  [<code>Player</code>](#Player)
<a id="playeriscustomplaybackused"></a>

#### player.adManager().isCustomPlaybackUsed()

Returns true if a custom video element is being used to play the current ad.

**Return** <code>boolean </code> Whether custom playback is used.

**Type**: instance method of  [<code>Player</code>](#Player)
<a id="playeresize"></a>

#### player.adManager().resize(width, height, viewMode)

Resizes the current ad.

| Param | Type | Description |
| --- | --- | --- |
| width | <code>number</code> | New ad slot width. |
| height | <code>number</code> | New ad slot height. |
| viewMode | <code>viewMode</code> | The new view mode. Value must not be null. |

**Type**: instance method of  [<code>Player</code>](#Player)
<a id="playergetadsystem"></a>

#### player.adManager().getAdSystem()

The source ad server information included in the ad response.

**Return**: <code>string</code> The source ad server of the ad, or the empty string if this information is unavailable.

**Type**: instance method of  [<code>Player</code>](#Player)
<a id="playergetadvertisername"></a>

#### player.adManager().getAdvertiserName()

The advertiser name as defined by the serving party.

**Return**: <code>string</code> The advertiser name, or the empty string if this information is unavailable.

**Type**: instance method of  [<code>Player</code>](#Player)
<a id="playergetapiframework"></a>

#### player.adManager().getApiFramework()

Identifies the API needed to execute the ad. This corresponds with the apiFramework specified in vast.

**Return**: <code>nullable string</code> The API framework need to execute the ad, or null if this information is unavailable.

**Type**: instance method of  [<code>Player</code>](#Player)
<a id="playergetcreativeadid"></a>

#### player.adManager().getCreativeAdId()

Returns the ISCI (Industry Standard Commercial Identifier) code for an ad, or empty string if the code is unavailable. This is the Ad-ID of the creative in the VAST response.

**Return**: <code>string</code>

**Type**: instance method of  [<code>Player</code>](#Player)
<a id="playergetcreativeid"></a>

#### player.adManager().getCreativeId()

Retrieves the ID of the selected creative for the ad.

**Return**: <code>string</code>The ID of the selected creative for the ad, or the empty string if this information is unavailable.

**Type**: instance method of  [<code>Player</code>](#Player)
<a id="playergetdealid"></a>

#### player.adManager().getDealId()

Returns the first deal ID present in the wrapper chain for the current ad, starting from the top. Returns the empty string if unavailable.

**Return**: <code>string</code>

**Type**: instance method of  [<code>Player</code>](#Player)
<a id="playergetheight"></a>

#### player.adManager().getHeight()

Returns the height of the selected non-linear creative.

**Return**: <code>number</code>  The height of the selected non-linear creative or 0 for a linear creative.

**Type**: instance method of  [<code>Player</code>](#Player)
<a id="playergetminsuggestedduration"></a>

#### player.adManager().getMinSuggestedDuration()

Returns the minimum suggested duration in seconds that the nonlinear creative should be displayed. Returns -2 if the minimum suggested duration is unknown. For linear creative it returns the entire duration of the ad.

**Return**: <code>number</code>  The minimum suggested duration in seconds that a creative should be displayed.

**Type**: instance method of  [<code>Player</code>](#Player)
<a id="playergettraffickingparameters"></a>

#### player.adManager().getTraffickingParameters()

Gets custom parameters associated with the ad at the time of ad trafficking.

**Return**: <code>non-null Object with string properties</code>  A mapping of trafficking keys to their values, or the empty Object if this information is not available.

**Type**: instance method of  [<code>Player</code>](#Player)
<a id="gettraffickingparametersstring"></a>

#### player.adManager().getTraffickingParametersString()

Gets custom parameters associated with the ad at the time of ad trafficking. Returns a raw string version of the parsed parameters from getTraffickingParameters.

**Return**: <code>string</code>  Trafficking parameters, or the empty string if this information is not available.

**Type**: instance method of  [<code>Player</code>](#Player)
<a id="getuielements"></a>

#### player.adManager().getUiElements()

Returns the UI elements that are being displayed when this ad is played. Refer to UiElements for possible elements of the array returned.

**Return**: <code>non-null Array of string</code> The UI elements being displayed.

**Type**: instance method of  [<code>Player</code>](#Player)
<a id="getuniversaladidregistry"></a>

#### player.adManager().getUniversalAdIdRegistry()

The registry associated with cataloging the UniversalAdId of the selected creative for the ad.

**Deprecated**: Use ad.getUniversalAdIds() instead.

**Return**: <code>string</code> Returns the registry value, or "unknown" if unavailable.

**Type**: instance method of  [<code>Player</code>](#Player)
<a id="getuniversaladids"></a>

#### player.adManager().getUniversalAdIds()

The list of UniversalAdIds of the selected creative for the ad.

**Return**: <code>non-null Array of non-null UniversalAdIdInfo</code> Returns the list of universal ad ID information that applies for this ad.

**Type**: instance method of  [<code>Player</code>](#Player)
<a id="getuniversaladidvalue"></a>

#### player.adManager().getUniversalAdIdValue()

The UniversalAdId of the selected creative for the ad.

**Deprecated**: Use ad.getUniversalAdIds() instead.

**Return**: <code>string</code> Returns the id value or "unknown" if unavailable.

**Type**: instance method of  [<code>Player</code>](#Player)
<a id="getvastmediabitrate"></a>

#### player.adManager().getVastMediaBitrate()

When both the creative and the media file have been selected by the SDK, this will return the bitrate for the media file as listed in the vast response.

**Return**: <code>number</code> The bitrate for the selected media file or 0.

**Type**: instance method of  [<code>Player</code>](#Player)
<a id="getvastmediaheight"></a>

#### player.adManager().getVastMediaHeight()

Returns the VAST media height of the selected creative.

**Return**: <code>number</code> The VAST media height of the selected creative or 0 if none is selected.

**Type**: instance method of  [<code>Player</code>](#Player)
<a id="getvastmediawidth"></a>

#### player.adManager().getVastMediaWidth()

Returns the VAST media width of the selected creative.

**Return**: <code>number</code> The VAST media width of the selected creative or 0 if none is selected.

**Type**: instance method of  [<code>Player</code>](#Player)
<a id="getwidth"></a>

#### player.adManager().getWidth()

Returns the width of the selected creative.

**Return**: <code>number</code> The width of the selected non-linear creative or 0 for a linear creative.

**Type**: instance method of  [<code>Player</code>](#Player)
<a id="getwrapperadids"></a>

#### player.adManager().getWrapperAdIds()

Ad IDs used for wrapper ads. The IDs returned starts at the inline ad (innermost) and traverses to the outermost wrapper ad. An empty array is returned if there are no wrapper ads.

**Return**: <code>non-null Array of string</code> The IDs of the ads, starting at the inline ad, or an empty array if there are no wrapper ads.

**Type**: instance method of  [<code>Player</code>](#Player)
<a id="getwrapperadsystems"></a>

#### player.adManager().getWrapperAdSystems()

Ad systems used for wrapper ads. The ad systems returned starts at the inline ad and traverses to the outermost wrapper ad. An empty array is returned if there are no wrapper ads.

**Return**: <code>non-null Array of string</code> The ad systems of the ads, starting at the inline ad, or an empty array if there are no wrapper ads.

**Type**: instance method of  [<code>Player</code>](#Player)
<a id="getwrappercreativeids"></a>

#### player.adManager().getWrapperCreativeIds()

Selected creative IDs used for wrapper ads. The creative IDs returned starts at the inline ad and traverses to the outermost wrapper ad. An empty array is returned if there are no wrapper ads.

**Return**: <code>non-null Array of string</code> The IDs of the ads' creatives, starting at the inline ad, or an empty array if there are no wrapper ads.

**Type**: instance method of  [<code>Player</code>](#Player)
<a id="isLinear"></a>

#### player.adManager().islinear()

Indicates whether the ad’s current mode of operation is linear or non-linear. If the value is true, it indicates that the ad is in linear playback mode; if false, it indicates non-linear mode. The player checks the linear property and updates its state according to the details of the ad placement. While the ad is in linear mode, the player pauses the content video. If linear is true initially, and the ad is a pre-roll (defined externally), the player may choose to delay loading the content video until near the end of the ad playback.

**Return**: <code>boolean</code> True if the ad is linear, false otherwise.

**Type**: instance method of  [<code>Player</code>](#Player)

<a id="playeraddclicklistenerfunc"></a>

#### player.adManager().addClickListener(func)

Sets a listener function called each time the user clicks on the ad.

**Type**: instance method of  [<code>Player</code>](#Player)

| Param | Type | Description |
| --- | --- | --- |
| func | <code>function</code> | the function called when the user clicks on the ad |

<a id="playeraddvolume"></a>

#### player.adManager().addVolumeMutedListener(func)

Sets a listener function called each time the user mutes the ad's volume.

**Type**: instance method of  [<code>Player</code>](#Player)

| Param | Type | Description |
| --- | --- | --- |
| func | <code>function</code> | the function called when the user mutes the ad |

<a id="playeraddvolumechangedlistenerfunc"></a>

#### player.adManager().addVolumeChangedListener(func)

Sets a listener function called each time the user changes the ad's volume.

**Type**: instance method of  [<code>Player</code>](#Player)

| Param | Type | Description |
| --- | --- | --- |
| func | <code>function</code> | the function called when the user changes the ad's volume |

<a id="playeraddskippedlistenerfunc"></a>

#### player.adManager().addSkippedListener(func)

Sets a listener function called each time the user skips the ad.

**Type**: instance method of  [<code>Player</code>](#Player)

| Param | Type | Description |
| --- | --- | --- |
| func | <code>function</code> | the function called when the user skips the ad |

<a id="playeraddpausedlistenerfunc"></a>

#### player.adManager().addPausedListener(func)

Sets a listener function called each time the user pauses the ad.

**Type**: instance method of  [<code>Player</code>](#Player)

| Param | Type | Description |
| --- | --- | --- |
| func | <code>function</code> | the function called when the user pauses the ad |

<a id="playeraddresumedlistenerfunc"></a>

#### player.adManager().addResumedListener(func)

Sets a listener function called each time the user resumes the ad.

**Type**: instance method of  [<code>Player</code>](#Player)

| Param | Type | Description |
| --- | --- | --- |
| func | <code>function</code> | the function called when the user resumes the ad |

<a id="playeraddstartedlistenerfunc"></a>

#### player.adManager().addStartedListener(func)

Sets a listener function called when the ad starts.

**Type**: instance method of  [<code>Player</code>](#Player)


| Param | Type | Description |
| --- | --- | --- |
| func | <code>function</code> | the function called when the ad starts |

<a id="playeraddfirstquartilelistenerfunc"></a>

#### player.adManager().addFirstQuartileListener(func)

Sets a listener function called when the ad reaches the first quartile of the video duration.

**Type**: instance method of  [<code>Player</code>](#Player)


| Param | Type | Description |
| --- | --- | --- |
| func | <code>function</code> | the function called when the ad reaches the first quartile of the video duration |

<a id="playeraddmidpointlistenerfunc"></a>

#### player.adManager().addMidpointListener(func)

Sets a listener function called when the ad reaches the middle of the video duration.

**Type**: instance method of  [<code>Player</code>](#Player)


| Param | Type | Description |
| --- | --- | --- |
| func | <code>function</code> | the function called when the ad reaches the middle of the video duration |


<a id="playeraddthirdquartilelistenerfunc"></a>

#### player.adManager().addThirdQuartileListener(func)

Sets a listener function called when the ad reaches the third quartile of the video duration.

**Type**: instance method of  [<code>Player</code>](#Player)


| Param | Type | Description |
| --- | --- | --- |
| func | <code>function</code> | the function called when the ad reaches the third quartile of the video duration |

<a id="playeraddcomlpetelistenerfunc"></a>

#### player.adManager().addCompleteListener(func)

Sets a listener function called when the ad finishes.

**Type**: instance method of  [<code>Player</code>](#Player)


| Param | Type | Description |
| --- | --- | --- |
| func | <code>function</code> | the function called when the ad finishes |

<a id="playeraddimpressionlistenerfunc"></a>

#### player.adManager().addImpressionListener(func)

Sets a listener function called when the impression URL has been pinged.

**Type**: instance method of  [<code>Player</code>](#Player)


| Param | Type | Description |
| --- | --- | --- |
| func | <code>function</code> | the function called when the impression URL has been pinged |

<a id="playeradderrorlistenerfunc"></a>

#### player.adManager().addErrorListener(func)

Sets a listener function called when the ad fails during loading or playing.

**Type**: instance method of  [<code>Player</code>](#Player)


| Param | Type | Description |
| --- | --- | --- |
| func | <code>function</code> | the function called when the ad fails during loading or playing |

<a id="playeraddblockedlistenerfunc"></a>

#### player.adManager().addBlockedListener(func)

Sets a listener function called when the ad is blocked by an external app.

**Type**: instance method of  [<code>Player</code>](#Player)


| Param | Type | Description |
| --- | --- | --- |
| func | <code>function</code> | the function called when the ad is blocked by an external app |

## Static

<a id="nexprotocol"></a>

#### Player.NexProtocol : <code>enum</code>
**Type**: static enum of [<code>Player</code>](#Player)
**Read only**: true
**Properties**:

| Name | Type | Default |
| --- | --- | --- |
| HLS | <code>number</code> | <code>0</code> |
| DASH | <code>number</code> | <code>1</code> |
| PROGRESSIVE_DOWNLOAD | <code>number</code> | <code>2</code> |
| UNKNOWN | <code>number</code> | <code>3</code> |
| OTHER | <code>number</code> | <code>4</code> |

<a id="nexevent"></a>

#### Player.NexEvent : <code>enum</code>
**Type**: static enum of [<code>Player</code>](#Player)
**Read only**: true
**Properties**:

| Name | Type | Default |
| --- | --- | --- |
| Track_Change | <code>number</code> | <code>0</code> |
| Fragment_Loading_Completed | <code>number</code> | <code>1</code> |
| Player_Destroyed | <code>number</code> | <code>2</code> |
| Speed_Change | <code>number</code> | <code>3</code> |
| Error | <code>number</code> | <code>4</code> |
| Cue_Change | <code>number</code> | <code>5</code> |
| Fragment_Buffered | <code>number</code> | <code>6</code> |
| Playlist_Loading_Completed | <code>number</code> | <code>7</code> |
| Fragment_Loading | <code>number</code> | <code>8</code> |
| Invalid_License | <code>number</code> | <code>9</code> |
| Frames_Drop_Capping | <code>number</code> | <code>10</code> |

<a id="thumbtype"></a>

#### Player.THUMB_TYPE : <code>enum</code>
**Type**: static enum of [<code>Player</code>](#Player)
**Read only**: true
**Properties**:

| Name | Type | Default |
| --- | --- | --- |
| STATIC_THUMBNAILS | <code>number</code> | <code>0</code> |
| DYNAMIC_THUMBNAILS | <code>number</code> | <code>1</code> |

## Global Typedef

<a id="nexcallbackevent"></a>

#### NexCallbackEvent : <code>function</code>
Called when a NexEvent happens.

**Type**: global typedef

<a id="nexcallback"></a>

#### NexCallback : <code>function</code>
Called when a FairPlay content needs to request the license.

**Type**: global typedef

| Param | Description |
| --- | --- |
| event | when the webkitkeymessage event from FairPlay is called. |

<a id="nexheaders"></a>

#### NexHeaders : <code>Object</code>
**Type**: global typedef
**Properties**:

| Name | Type | Description |
| --- | --- | --- |
| FieldName | <code>string</code> | of the HTTPHeaders. |
| FieldValue | <code>string</code> | of the HTTPHeaders. |

<a id="nexdrminformation"></a>

#### NexDRMInformation : <code>Object</code>
**Type**: global typedef
**Properties**:

| Name | Type | Description |
| --- | --- | --- |
| NexDRMType | <code>string</code> | NexDRMType of the video. |
| NexDRMKey | <code>string</code> | NexDRMKey of the video. |
| NexHeaders | [<code>Array.&lt;NexHeaders&gt;</code>](#NexHeaders) | NexHeaders of the video. |
| NexCallback | [<code>NexCallback</code>](#NexCallback) | NexCallback for FairPlay content. |

<a id="track"></a>

#### Track : <code>Object</code>
**Type**: global typedef
**Properties**:

| Name | Type | Description |
| --- | --- | --- |
| width | <code>number</code> | width of the video. |
| height | <code>number</code> | height of the video. |
| bitrate | <code>number</code> | bitrate of the video. |
| id | <code>number</code> | id of the video. |

* Bitrate property is not available on Safari iOS, Fairplay protected videos on Safari Mac OS or .mp4 videos.

<a id="audiostream"></a>

#### AudioStream : <code>Object</code>
**Type**: global typedef
**Properties**:

| Name | Type | Description |
| --- | --- | --- |
| id | <code>number</code> | id of the stream. |
| language | <code>number</code> | language of the stream. |
| name | <code>number</code> | name of the stream. |

#### <a id="frame"></a> Frame : <code>Object</code>

**Type**: global typedef
**Properties**:

| Name    | Type                | Description                  |
| ------- | ------------------- | ---------------------------- |
| f       | <code>canvas</code> | Thumbnail canvas instance.   |
| w       | <code>number</code> | Width.                       |
| h       | <code>number</code> | Height.                      |
| st      | <code>number</code> | Thumbnail starting time.     |
| ft      | <code>number</code> | Thumbnail ending time.       |


## VR Player

<a id="setFieldView"> </a>
   #### player.setFieldView()

Set the field of view.

**Type**: instance method of [<code>Player</code>](#Player)

 | Param | Type |Description |
 | --- | --- | --- |
 | fov | number | the fov value. |

 <a id="getFieldView"> </a>
   #### player.getFieldView()

   get the field of view.

   **Type**: instance method of  [<code>Player</code>](#Player)
   **Returns**: number

## Multiview

#### multiview.additionalVideo(info)

Creates and initializes the player.

**Type**: function of [<code>nexplayer</code>](#Player)
**Param**:
   - **configuration** is an object which its properties values could be:

**Mandatory Parameters:**

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | NexPlayer key to validate the playback. |
| div | <code>HTMLDivElement</code> | Div container of the player. |
| src | <code>string</code> | Relevant src of the video to be played. |

**Optional Parameters:**

| Param | Type | Description |
| --- | --- | --- |
| allowScreenPlayPause | <code>boolean</code> | Allows to play and pause the video clicking on it. |
| autohide | <code>boolean</code> | Sets if the UI must hide when the user does not interact with the video. True by default. |
| autoplay | <code>boolean</code> | Determines if the video must start playing or paused. True by default. |
| blockZoom | <code>boolean</code> | Determines if the zoom in 360 videos is available or not. |
| callbackForLogger | <code>Function</code> | Function to be called when the logger shows a message. |
| callbackForReturn | <code>Function</code> | Sets a callback checkSupportedConfigurations(URL, DRMType) to be executed when the corresponding button is clicked. |
| callbacksForPlayer | <code>Function</code> | Used for retrieving the nexplayer instance and video element. This is necessary for getting the instance and use the NexPlayer API. |
| cast | <code>boolean</code> | Determines if the cast will be enabled or not. |
| chromecastEndImg | <code>string</code> | URL of an image to be used as ending. |
| chromecastLaunchImg | <code>string</code> | URL of an image to be used at launch. |
| debug | <code>boolean</code> | Determines if log information is showed. By default is set to true. |
| defaultQuality | <code>number</code> | Sets the starting track through its id. By default is -1, this enables the ABR. |
| disableFullscreen | <code>boolean</code> | Determines if the full screen will be enabled. |
| disableKeyEvents | <code>boolean</code> | Determines if the keyboard keys can be used to control the video (play/pause, forward/backward and volume up/down). |
| drm | <a href="#/API?id=NexDRMInformation"><code>Array\<NexDRMInformation></code></a> | Contains an array of DRM information. By default it's set to null. |
| externSubtitles | <code>Array</code> | Used to provide subtitle files as external subtitles. |
| hideOptionsUi | <code>Object</code> | Hides the setting that you choose from the UI. |
| hideScreenPlay | <code>boolean</code> | Hides the play button in the middle of the video, which appears when the video is paused. |
| hideVolumeIcon | <code>boolean</code> |  Determines if the volume icon will be hidden for mobile devices. The volume is controlled by the device buttons. |
| lowLatency | <code>boolean</code> |  Determines if the low latency will be enabled. |
| liveSettings | <code>Object</code> | Settings to control live playback. Requires low latency. |
| logosrc | <code>string</code> | Company URL logo. |
| mutedAtStart | <code>boolean</code> | Determines if the video will start playing muted or not. By default this value is set to false. |
| pip | <code>boolean</code> | Determines if picture-in-picture will be enabled. |
| poster | <code>string</code> | Video poster URL.  |
| seekUI | <code>number</code> | Sets the number of seconds the UI buttons will seek forwards or backwards. Set to 10s by default. |
| showingFullUI | <code>boolean</code> | Determines if the UI is hidden or not. |
| showUI360 | <code>boolean</code> | Determines if the 360UI will be enabled. |
| srcSets | <code>Array</code> | Array of objects that contains a stream and an optional DRM.
| staticThumbnailsImage | <code>string</code> | Image to extract thumbnails from. |
| staticThumbnailsVTT | <code>string</code> | Used to provide the player an external thumbnails VTT file. |
| startingBufferLength | <code>number</code> | Determines the buffer that the video should have before start. |
| startFullscreen | <code>boolean</code> | Determines if the video will start on full screen. |
| subtitle | <code>string</code> | Video subtitle name. |
| timeUI | <code>boolean</code> | Determines if the video time will be hidden on the UI. |
| title | <code>string</code> | Video name. |
| type_360 | <code>string</code> | Selects the 360 video format to play. Possible values are 'equirectangular', 'cubemap' and 'topdown'. |
| useDynamicThumbnails | <code>boolean</code> | Determines if dynamic thumbnails are used. By default this value is set to false. |
| useiOSFullScreen | <code>boolean</code> | Determines if the iOS native full screen will be used. |
| vast | <code>string</code> | Advertisement URL that is going to be played. VAST, VPAID and VMAP are supported. |
| watermark | <code>object</code> | Watermark image URL. |
| withCredentials | <code>boolean</code> | Indicates whether or not cross-site Access-Control requests should be made using credentials such as cookies, authorization headers or TLS client certificates. |
| cmcd | <code>Object</code> |  Enables the Common Media Client Data. Only needs to create an empty object to enable it. |
|licenseWithCredentials| <code>boolean</code> | Indicates whether or not cross-site Access-Control requests should be made using credentials such as cookies, authorization headers or TLS client certificates with DRM.|
| maxFrameDrop | <code>number</code> | The value of this property should be within the range 0 - 1. A <a href="#/API?id=nexevent">Frames_Drop_Capping</a> event will be triggered whenever the percentage of frames dropped is higher than this threshold.|
| xhrSetHeader | <code>Array</code> | You can configure the headers that are necessary for the URL request.|

#### multiview.addPlayer(player)

This method stores each new player which will allow the MultipleView instance to control all the videos.

**Type**: instance method of [<code>Player</code>](#Player)

#### multiview.Initialize()

This method only has to be called once in the index and starts all the videos sequentially. It must be called after all videos are set.

**Type**: instance method of [<code>Player</code>](#Player)

#### multiview.togglePlayPause()

Enables toggle between play and pause.

**Type**: instance method of [<code>Player</code>](#Player)

#### multiview.seek(value)


   Sets the currentTime property of the attached video element. (if isUTC is true, the seek value will be in a different format than the currentTime of the video element).

   **Type**: instance method of [<code>Player</code>](#Player)

  | Param | Type |Description |
  | --- | --- | --- |
  | event | Event | value in seconds that the player will seek to. |

  #### multiview.seekLive()

   Jump to the livestream current time from the current position (if isUTC is true, the seek value will be in a different format than the currentTime of the video element). only works in livestream.

   **Type**: instance method of [<code>Player</code>](#Player)

## Youtube Player


   #### YouTubePlayer.init()
   <a id="init"> </a>
  Initialise the youtube player

  #### YouTubePlayer.URL(url)
   <a id="URL"> </a>
  Parse youtube url to extract the id of the video

   **Type**: instance method of [<code>Player</code>](#Player)
