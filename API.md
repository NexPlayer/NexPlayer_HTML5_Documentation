<a id="api-top"> </a>

# NexPlayer API 

## Player

**Type**: global class
- Player
 - instance
   - [.Setup(info)](#nexplayersetupinfo)
   - [.getTracks()](#gettracks) ⇒ [Array.< Track >](#track-object)
   - [.getCurrentTrack()](#getcurrenttrack) ⇒ [Track](#track-object)
   - [.setCurrentTrack(trackID)](#playersetcurrenttracktrackid)
   - [.enableABR()](#playerenableabr)
   - [.getAudioStreams()](#getaudiostreams) ⇒ [Array.< AudioStream >](#audiostream-object)
   - [.getCurrentAudioStream()](#getcurrentaudiostream) ⇒ [AudioStream](#audiostream-object)
   - [.setAudioStream(streamID)](#playersetaudiostream)
   - [.getCurrentSubtitle()](#getcurrentsubtitle)
   - [.getSubtitles()](#getsubtitles)
   - [.setSubtitle(subID)](#playersetsubtitlesubid)
   - [.isLive()](#islive) ⇒ boolean
   - [.on(callbackType, functionToBeCalled)](#playeroncallbacktype-functiontobecalled)
   - [.attachSubtitleRendererDiv(subtitleRendererDiv)](#playerattachsubtitlerendererdivsubtitlerendererdiv)
   - [.create360View()](#playercreate360view)
   - [.FairPlayNexLicenseRequestLoaded(event)](#playerfairplaynexlicenserequestloadedevent)
   - [.FairPlayNexLicenseRequestFailed(event)](#playerfairplaynexlicenserequestfailedevent)
   - [.setThumbnailResources(callback, vttURl, imageURL)](#playersetthumbnailresourcescallback-vtturl-imageurl)
   - [.isUTC()](#isutc) ⇒ boolean
   - [.getCurrentTime()](#getcurrenttime) ⇒ number
   - [.getDuration()](#getduration) ⇒ number
   - [.getDVRWindowSize()](#getDVRWindowSize) ⇒ number
   - [.getURL()](#playergeturl)
   - [.checkFrameDrop()](#playercheckframedrop) ⇒ number
   - [.seek(value)](#playerseekvalue)
   - [.sendImpression()](#playersendimpression)
   - [.getProtocol()](#getprotocol) ⇒ number
   - [.getThumbnailController()](#getthumbnailcontroller) ⇒ ThumbController
   - [.setThumbnailStep(step)](#playersetthumbnailstepstep)
   - [.enablePreviewThumbnails(option)](#playerenablepreviewthumbnailsoption)
   - [.setSpeed(speed)](#playersetspeedspeed)
   - [.getQualityLevels()](#getqualitylevels) ⇒ array
   - [.setTrack(qualityLevel)](#playersettrackqualitylevel)
   - [.togglePlayPause()](#playertoggleplaypause)
   - [.toggleFullScreen()](#playertogglefullscreen)
   - [.showStats()](#playershowstats)
   - [.jumpForward(value)](#playerjumpforward)
   - [.jumpBackward(value)](#playerjumpbackward)
   - [.setThumbnailStep(step)](#playersetthumbnailstepstep)
   - [.getCurrentLiveLatency()](#playergetcurrentlivelatency)
   - [.getCurrentBuffer()](#playergetcurrentbuffer)
   - [.toggleControlBar()](#playertogglecontrolbar)
   - [.isControlBarOpen()](#playeriscontrolbaropen)
   - [.toggleLanguagesMenu()](#playertogglelanguagesmenu)
   - [.nextFocus()](#playernextfocus)
   - [.previousFocus()](#playerpreviousfocus)
   - [.clickFocus()](#playerclickFocus)
   - [.adManager()](#playeradmanager)
   - [.getAdObject()](#playergetadobject)
   - [.getId()](#playergetid)
   - [.getTitle()](#playergettitle)
   - [.getDescription()](#playergetdescription)
   - [.getMediaURL()](#playergetmediaurl)
   - [.getSurveyURL()](#playergetsurveyurl)
   - [.getDuration()](#playergetduration)
   - [.getSkipTime()](#playergetskiptime)
   - [.getCurrentTime()](#playergetcurrenttime)
   - [.getContentType()](#playergetcontenttype)
   - [.isSkippable()](#playerisskippable)
   - [.isLinear()](#playerislinear)
   - [.isVpaid()](#playerisvpaid)
   - [.pause()](#playerpause)
   - [.play()](#playerplay)
   - [.skip()](#playerskip)
   - [.abort()](#playerabort)
   - [.addClickListener(func)](#playeraddclicklistenerfunc)
   - [.addVolumeMutedListener(func)](#playeraddvolume)
   - [.addVolumeChangedListener(func)](#playeraddvolumechangedlistenerfunc)
   - [.addSkippedListener(func)](#playeraddskippedlistenerfunc)
   - [.addPausedListener(func)](#playeraddpausedlistenerfunc)
   - [.addResumedListener(func)](#playeraddresumedlistenerfunc)
   - [.addStartedListener(func)](#playeraddstartedlistenerfunc)
   - [.addFirstQuartileListener(func)](#playeraddfirstquartilelistenerfunc)
   - [.addMidpointListener(func)](#playeraddmidpointlistenerfunc)
   - [.addThirdQuartileListener(func)](#playeraddthirdquartilelistenerfunc)
   - [.addCompleteListener(func)](#playeraddcomlpetelistenerfunc)
   - [.addImpressionListener(func)](#playeraddimpressionlistenerfunc)
   - [.addErrorListener(func)](#playeradderrorlistenerfunc)
   - [.addBlockedListener(func)](#playeraddblockedlistenerfunc)
 - static
   - [.NexProtocol](#nexprotocol): enum
   - [.NexEvent](#nexevent): enum
   - [.THUMB_TYPE](#thumbtype): enum


#### nexplayer.Setup(info)

Creates and initializes the player.

**Type**: instance method of [<code>Player</code>](#Player)   
**Param**: **info** is and object which its values could be:

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | that validates the playback. |
| div | <code>HTMLDivElement</code> | the div container of the player. |
| src | <code>string</code> | of the video to be played. |
| autoplay | <code>boolean</code> | determine if the video must start playing or paused. By default it's set to true. |
| drm | <code>Array.<NexDRMInformation></code> | contains an array of DRM information. By default it's set to null. |
| seekUI | <code>number</code> | establish the number of seconds the UI buttons will seek forwards or backwards. By default is set to 10s. |
| mutedAtStart | <code>boolean</code> | determine if the video will start playing muted or not. By default this value is set to false. |
| debug	 | <code>boolean</code> | determine if log information is showed. By default is set to true. |
| type_360 | <code>string</code> | select the 360 video format to play. Possible values are 'equirectangular', 'cubemap' and 'topdown'. |
| autohide | <code>boolean</code> | establish if the UI must hide when the user does not interact with the video. By default is set to true.. |
| callbacksForPlayer | <code>function</code> | used for retrieving the nexplayer instance and video element. This is necessary for getting the instance and use the NexPlayer API. |
| callbackForReturn | <code>function</code> | establish a callback to be executed when the corresponding button is clicked. |
| callbackForLogger | <code>function</code> | function to be called when the logger show a message. |
| vast | <code>string</code> | advertisement url that is going to be played. VAST, VPAID, VMAP are supported. |
| useDynamicThumbnails | <code>boolean</code> | determine if dynamic thumbnails are used. By default this values is set to false. |
| showingFullUI | <code>boolean</code> | determine if the UI is hidden or not. |
| disableKeyEvents | <code>boolean</code> | determine if the keyboard keys can be used to control the video (play/pause, forward/backward and volume up/down). |

<a id="gettracks"> </a>
   #### player.getTracks() ⇒ Array.< Track >

Get all the video avaliable tracks (different qualities).

**Type**: instance method of [<code>Player</code>](#Player)     
**Returns**:: Array.< Track > - all the tracks available.
   
<a id="getcurrenttrack"> </a>
   #### player.getCurrentTrack() ⇒ Track

Get the current track information.

**Type**: instance method of [<code>Player</code>](#Player)   
**Returns**: Track - the current track.

#### player.setCurrentTrack(trackID)

Set the current track.

**Type**: instance method of [<code>Player</code>](#Player)   
**Export**:

| Param | Type | Description |
| --- | --- | --- |
| trackID | <code>number</code> | ID of the track to be used. |

#### player.enableABR()

Enable the ABR to change automatically between tracks.

**Type**: instance method of [<code>Player</code>](#Player)    

<a id="getaudiostreams"> </a>
   #### player.getAudioStreams() ⇒ Array.< AudioStream >

Get the available audio streams.

**Type**: instance method of [<code>Player</code>](#Player)   
**Returns**: Array.<AudioStream> - the list of the available audio streams.

<a id="getcurrentaudiostream"> </a>
   #### player.getCurrentAudioStream() ⇒ AudioStream

Get the audio stream currently in use.

**Type**: instance method of [<code>Player</code>](#Player)   
**Returns**: AudioStream - the current audio track.

#### player.setAudioStream(streamID)

Set the current audio stream.

**Type**: instance method of [<code>Player</code>](#Player)   
**Export**:

| Param | Type | Description |
| --- | --- | --- |
| streamID | <code>number</code> | ID of the audio stream to be used. |


<a id="getcurrentsubtitle"> </a>  
   #### player.getCurrentSubtitle() 

Get the current subtitle info.

**Type**: instance method of [<code>Player</code>](#Player)     
**Returns**: Current Subtitle - the current subtitle track (undefined if no subs are activated).

<a id="getsubtitles"> </a>  
   #### player.getSubtitles()
   
Get all the avaliable subtitle tracks info.

**Type**: instance method of [<code>Player</code>](#Player)   
**Returns**: Array of subtitles - the subtitle tracks of the video.

#### player.setSubtitle(subID)

Set the current subtitle track.

**Type**: instance method of [<code>Player</code>](#Player)   
**Export**:

| Param | Type | Description |
| --- | --- | --- |
| subID | <code>number</code> | ID of the subtitle track to be used |


<a id="islive"> </a>  
   #### player.isLive() ⇒ boolean

Informs whether the video is live or on demand (VOD). Needs to be called when the manifest is finally loaded. 
It is recommended to use within the video "loadeddata" event.

**Type**: instance method of [<code>Player</code>](#Player)   
**Returns**: boolean - true if the video is live, false otherwise.


#### player.on(callbackType, functionToBeCalled)

Adds a listener for Events.

**Type**: instance method of [<code>Player</code>](#Player)      
**Export**:

| Param | Type | Description |
| --- | --- | --- |
| callbackType | <code>NexEvent</code> | Event to listen for |
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

   
   Set the currentTime property of the attached video element in seconds. If it is a live stream is necessary to combine it with [.getDVRWindowSize()](#getcurrenttime). 
   (if isUTC is true, the seek value will be in a different format than the currentTime of the video element).

   **Type**: instance method of [<code>Player</code>](#Player) 

  | Param | Type |Description |
  | --- | --- | --- |
  | event | Event | value in seconds that the player will seek to. |

  ```js
   player.seek(120) // It jumps into minute 2:00 in the video (120 secs)
   player.seek(player.getDVRWindowSize() - 120)) // In jumps back 2 minutes (120 secs) from current live time.
   ```


#### player.sendImpression()

Send the impression details to the server (only for internal management).

**Type**: instance method of [<code>Player</code>](#Player) 

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

Set the time interval between frames for dynamic thumbnails.

**Type**: instance method of [<code>Player</code>](#Player) 

  | Param | Type |Description |
  | --- | --- | --- |
  | step | number | the seconds between two different thumbnails. |

#### player.enablePreviewThumbnails(option) 

Enable thumbnails preview. This method must be called before Init().

**Type**: instance method of [<code>Player</code>](#Player) 

 | Param | Type |Description |
 | --- | --- | --- |
 | option | boolean | the value that enable or not the thumbnails. |

#### player.setSpeed(speed)

Set the video playback speed.

**Type**: instance method of [<code>Player</code>](#Player) 

 | Param | Type |Description |
 | --- | --- | --- |
 | speed | number | the speed value. |

<a id="getqualitylevels"> </a>  
#### player.getQualityLevels() ⇒ array

Get the video quality levels array.

**Type**: instance method of [<code>Player</code>](#Player)   
**Returns**: array - quality levels array info

#### player.setTrack(qualityLevel)

Set the video quality level.

**Type**: instance method of [<code>Player</code>](#Player) 

#### player.togglePlayPause()

Toggle between play and pause.

**Type**: instance method of [<code>Player</code>](#Player) 


#### player.toggleFullScreen()

Toggle between full screen and windowed.

**Type**: instance method of [<code>Player</code>](#Player) 

<a id="playershowstats"></a>

#### player.showStats()

Display basic stream information when typing "nex" on the keyboard.

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

Set the step for dynamic thumbnails.

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

Toogle the subtitles menu options.

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

#### player.adManager().getMediaURL()

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

<a id="thumbtype"></a>

#### Player.THUMB_TYPE : <code>enum</code>
**Type**: static enum of [<code>Player</code>](#Player)  
**Read only**: true  
**Properties**:

| Name | Type | Default |
| --- | --- | --- |
| STATIC_THUMBNAILS | <code>number</code> | <code>0</code> | 
| DYNAMIC_THUMBNAILS | <code>number</code> | <code>1</code> |

<a id="NexCallbackEvent"></a>

#### NexCallbackEvent : <code>function</code>
Called when a NexEvent happens.

**Type**: global typedef  

<a id="NexCallback"></a>

#### NexCallback : <code>function</code>
Called when a FairPlay content needs to request the license.

**Type**: global typedef  

| Param | Description |
| --- | --- |
| event | when the webkitkeymessage event from FairPlay is called. |

<a id="NexHeaders"></a>

#### NexHeaders : <code>Object</code>
**Type**: global typedef  
**Properties**:

| Name | Type | Description |
| --- | --- | --- |
| FieldName | <code>string</code> | of the HTTPHeaders. |
| FiledValue | <code>string</code> | of the HTTPHeaders. |

<a id="NexDRMInformation"></a>

#### NexDRMInformation : <code>Object</code>
**Type**: global typedef  
**Properties**:

| Name | Type | Description |
| --- | --- | --- |
| NexDRMType | <code>string</code> | NexDRMType of the video. |
| NexDRMKey | <code>string</code> | NexDRMKey of the video. |
| NexHeaders | [<code>Array.&lt;NexHeaders&gt;</code>](#NexHeaders) | NexHeaders of the video. |
| NexCallback | [<code>NexCallback</code>](#NexCallback) | NexCallback for FairPlay content. |

<a id="Track"></a>

#### Track : <code>Object</code>
**Type**: global typedef     
**Properties**:  

| Name | Type | Description |
| --- | --- | --- |
| width | <code>number</code> | width of the video. |
| height | <code>number</code> | height of the video. |
| bitrate | <code>number</code> | bitrate of the video. |
| id | <code>number</code> | id of the video. |

<a id="AudioStream"></a>

#### AudioStream : <code>Object</code>
**Type**: global typedef  
**Properties**:  

| Name | Type | Description |
| --- | --- | --- |
| id | <code>number</code> | id of the stream. |
| language | <code>number</code> | language of the stream. |
| name | <code>number</code> | name of the stream. |
