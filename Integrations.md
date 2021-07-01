<a id="integrations-top"> </a>

<a href="https://nexplayer.github.io/NexPlayer_HTML5_Documentation/#/"><img text src="./_images/logo5.png" alt="Nexplayer"></a>

***

# Integrations<!-- {docsify-ignore-all} -->

This is a summary of how to use third party tools

***
<a id="agora-top"> </a>

## Agora

Agora allows us to give you the chance to see a video with your friends

<img width="50%" text-align="center" src="./_images/agoraimg.png" alt="nexAgo" >

### Using with the player

To start, you need to have a channel set up in Agora. You can do that by creating an account in the following link: https://www.agora.io/en.

In order to use it, you need to create a div with the “agoraContainer” id, inside of the player container.

```html
	<div id="player_container">
		<div id="player"></div>
		<div id="agoraContainer"></div>
	</div>

```

After, all you need to do is add the agoraOptions object to your setup.

<a id="agoraOptions"></a>

#### agoraOptions : <code>Object</code>
**Type**: global typedef  
**Properties**:

| Param | Type | Description |
| --- | --- | --- |
| channel | <code>String</code> | The name of your channel. |
| token | <code>string</code> | The Token of you channel. |
| appid | <code>string</code> | Your AppId. |

And your setup should look like this:

```js

	nexplayer.Setup({
		key: "REPLACE THIS WITH YOUR CUSTOMER KEY",
		div: document.getElementById('player'),
		autoplay: true,
		mutedAtStart: true,
		showingFullUI: true,
		debug: false,
		callbacksForPlayer: callBackWithPlayers,
		src: "VIDEO URL",
		agoraOptions: {
			token: "YOUR CHANNEL TOKEN",
			channel: "YOUR CHANNEL NAME",
			appid: "YOUR APPID"
		},
	});

```

### Agora API

<a id="joinAgora"> </a>  

#### player.joinAgora()

You need to have a previous config given to agora before naming this function. If all is correct, you will be able to join the given Agora channel.

**Type**: instance method of [<code>Player</code>](#Player)

<a id="leaveAgora"> </a>  

#### player.leaveAgora()

Left the Agora channel.

**Type**: instance method of [<code>Player</code>](#Player)

***
<a id="conviva-top"> </a>

## Conviva Analytics

<a href="https://www.nexplayersdk.com/nexplayer-html5/" target = "_blank" >NexPlayer™ HTML5</a> is a multi-screen streaming player that enables HLS and DASH live streaming across all browsers and platforms with the highest video quality. NexPlayer™ HTML5 supports an advanced feature set that includes DRM, Closed Captioning, Time Shifting and 360 video playback among many others.

This repository contains the sample demo code of NexPlayer™ HTML5 with the integration of  <a href="https://www.conviva.com/" target = "_blank" >Conviva</a>.A fully working demo can be downloaded on this github <a href="https://github.com/NexPlayer/NexPlayer_HTML5_Conviva" target = "_blank" >repository</a>.

### Quick Start

- The folders "app" and "conviva" include the scripts that should be included in the HTML file:

```js

	<script type="text/javascript" src="conviva/conviva-core-sdk.min.js"></script>
	<script type="text/javascript" src="conviva/conviva-html5native-impl.js"></script>
	<script type="text/javascript" src="app/configs.js"></script>
	<script type="text/javascript" src="app/NexHandshake.js"></script>

```

- Configure your settings in "app/configs.js".
- NexHandshake should be created after the event "loadeddata" is fired. This object preintegrates the Conviva client and will handle the analytic sessions.

```js

	var NexConviva = null;

	...
	videoElement.addEventListener('loadeddata', loadModules, false);
	...

	function loadModules() {
		NexConviva = new NexHandshake(videoElem, url, player.isLive(), true);
		NexConviva.initConvivaClient();
		NexConviva.createContentSession();
		NexConviva.updateBitrateData(player.getCurrentTrack().bitrate / 1000);
		// Use this in order to update the bitrate data every time a track changes
		player.on(nexplayer.Player.NexEvent.Track_Change, function() {
			NexConviva.updateBitrateData(player.getCurrentTrack().bitrate / 1000);
		});
		// Example of creating a custom tag
		NexConviva.createCustomTag("a", "20", false);
		// It is necessary to call this method to update the metadata on Conviva side
		NexConviva.updateContentMetadata();
	}

```

- To destroy and reset the current Conviva session the following code should be used:

```js
	NexConviva.cleanupContentSession();
```

This is already called in NexHandshake.js file, but it can be modified and be called whenever it is wanted to clean up the session.

***
<a id="ioswebview-top"> </a>

###  iOS WebView

Here is the example code to create a simple application

```swift

  import UIKit
  import WebKit
  class ViewController: UIViewController, WKUIDelegate {
    
	var webView: WKWebView!

	override func loadView() {
		let webConfiguration = WKWebViewConfiguration()
		webView = WKWebView(frame: .zero, configuration: webConfiguration)
		webView.uiDelegate = self
		view = webView
	}
	override func viewDidLoad() {
		super.viewDidLoad()
		
		let myURL = URL(string:"Your url")
		let myRequest = URLRequest(url: myURL!)
		webView.load(myRequest)
	}}

```

For the video to start playing, you will need to configure the following parameters

```swift

    override func loadView() {
		let webConfiguration = WKWebViewConfiguration()
		webConfiguration.preferences.javaScriptEnabled = true
		webConfiguration.mediaPlaybackRequiresUserAction = false
		webConfiguration.allowsInlineMediaPlayback = true
		webView = WKWebView(frame: .zero, configuration: webConfiguration)
		webView.uiDelegate = self
		view = webView
    }

```

***
<a id="multiplesources-top"> </a>

### Multiple Sources

This feature, as long as src is undefined, allows the player to choose a playable src from one of the objects contained in the srcSets array depending on the browser and device support. Furthermore, this enhancement will automatically skip those streams that may fail during playback and try to restart it taking any of the following videos provided in the property previously mentioned.

```js

	nexplayer.Setup({
		key: 'REPLACE THIS WITH YOUR CUSTOMER KEY',
		div: document.getElementById('player'),
		src: 'video URL',
		drm: [{
			NexDRMType:'DRM Type (eg. com.widevine.alpha)', NexDRMKey: 'URI for the DRM Key', 
			NexHeaders:[{FieldName: 'Header Field Name', FiledValue: 'Header Field Value'}],
			NexCallback: // Optional DRM callback for FairPlay
		}], // Optional: DRM information
		srcSets:[
			{
				src: 'video URL',
				drm: {
					NexDRMType:'DRM Type (eg. com.widevine.alpha)', NexDRMKey: 'URI for the DRM Key', 
					NexHeaders:[{FieldName: 'Header Field Name', FiledValue: 'Header Field Value'}],
					NexCallback: // Optional DRM callback for FairPlay
				} // Optional: DRM information or undefined
			},
			{
				src: 'other video URL',
				drm: 'undefined'
			},
			...
		] // Optional: Objects array containing a stream and an optional DRM.
	});

```

***
<a id="verimatrix-top"> </a>

## Verimatrix Watermarking

Verimatrix Watermarking allows the customers, the chance to use their own Watermark in order to get more secure in their content, during the playback.

### Using with the player

To start, you need to import the watermark.min.js file, to get it you should request it here https://www.verimatrix.com/products/watermarking/.


```html

<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no" />
		<title>NexPlayer</title>
		<style type="text/css">
				/* "YOUR STYLE" */
		</style>
	</head>
	<body>
		<div id="player_container">
			<div id="player" width="560" height="315"></div>
		</div>
		<script src="YOUR watermark.min.js FILE URL"></script>
		<script src="YOUR nexplayer.js FILE"></script>
		<script>

			var player = null;
			var videoElem = null;
			var callBackWithPlayers = function (nexplayerInstance, videoElement) {
				player = nexplayerInstance;
				videoElem = videoElement;
				let FLogoImage = new Image();
				FLogoImage.src = "YOUR WATERMARK IMG URL";
				let wmInfo = {
					"strength" : 255, // WATERMARK STRENGTH (1-255)
					"transactionId": 12424, // REQUIRED FOR WmSdInitWatermark(). TRANSACTION OR USER IDENTIFIER.
					"videoParentElement": videoElem.parentElement, // YOUR VIDEO ELEMENT PARENT 
					"videoElement": videoElem, // YOUR VIDEO ELEMENT ID 
					"apiToken": 't1EKhe8A', // OPTIONAL. OPAQUE STRING FOR ACTIVATING SUBSEQUENT API ACTIONS
					"logoImage": FLogoImage, // OPTIONAL. SET A VISIBLE IMAGE TO DRAW IN ADDITION TO THE IMPERCEPTIBLE WATERMARK
					"logoPos": [ 15, 20, 269, 100 ], // SET COORDINATES FOR THE LOGO IMAGE. FORMAT: [x, y, WIDTH, HEIGHT]
					"player" : player, // THE OBJECT REPRESENTING VIDEO PLAYER.
				}
				let watermarkContext = WmSdkInitWatermark(wmInfo); // STARTS TO INITIALIZE THE WATERMARK AND SET ITS ESSENTIAL PARAMETERS, WHEN VIDEO PLAYBACK STARTS. THIS IS THE ONLY FUNCTION YOU MUST CALL TO START WATERMARKING.
			}
		
			nexplayer.Setup({
				key: "YOUR LICENSE KEY",
				div: document.getElementById('player'),
				autoplay: true,
				mutedAtStart: true,
				debug: true,
				callbacksForPlayer: callBackWithPlayers,
				src: 'YOUR STREAM SRC',
			});

		</script>
	</body>
</html>

```

### wmInfo Object

| Param | Type | Description |
| --- | --- | --- |
| strength | Integer | Watermark strength. <br/> Valid values: <br/> • 255: Visible watermark for debugging <br/> • 1 - 100: Production watermark strength <br/> (1 = weakest, 100 = strongest/possibly visible) <br/> A stronger watermark is faster to extract. Values of 50 or <br/> less require very long videos to extract.<br/> Default: 80- |
| transactionId | Unsigned <br/> integer | Required for WmSdInitWatermark(). Transaction or user identifier. <br/> Size: 36 bits <br/> Valid values: 0 - 687194767365 | 
| operatorId | Unsigned <br/> integer | Operator identifier. You do not need to provide operatorId as it is hard-coded to an operator-specific value in the software. <br/> Size: 12 bits <br/> Valid values: 0 - 4095| 
| videoParentElement | HTML DOM Element object | Parent node of the HTML element where playback is occuring, typically div. canvasElement (see below) is placed within videoParentElement. If you use custom controls for controlling the video, these are also attached to videoParentElement. <br/> You must provide videoParentElement or videoElement (see below) in order to associate the watermark with correct element. | 
| videoElement | HTML DOM Element object | Video element where playback is occurring.<br/> If videoElement is not provided, the first video element found on the page is used.| 
| canvasElement | HTML DOM Element object | Canvas element (OSD) where the watermark is drawn. This element is drawn on top of the video. <br/> If canvasElement is not provided ,Verimatrix Watermarking creates a canvas element and places it into videoParentElement| 
| player | object | The object representing video player | 
| allowFullscreen | Boolean | Flag to permit fullscreen video playback. In order for Verimatrix Watermarking to work correctly in fullscreen mode, other properties such as videoParentElement have to be set correctly. <br/> Values:<br/> • true = Allow transition to fullscreen mode <br/> • false = Disallow fullscreen mode <br/> Default: false <br/> Keep reading the guide to see more needed info about it| 
| afterDraw | function(successflag) | Verimatrix Watermarking executes this function after drawing the watermark. You can use this callback to get feedback on the watermarking process| 
| strengthMultiplier | Float | Applying the strength multiplier enhances the watermark strength. This capability is intended for debugging purposes: the normal strength scale 1-100 is sufficient for imperceptible watermarks. <br/> Default: undefined (equal to 1)| 
| debugBorder | Boolean | Draws debug borders around canvasElement and watermark. Used to debug placement of elements in relation to video playback. <br/> Values: <br/> • true = Draw debug borders <br/> • false = Do not draw debug borders <br/> Default: false | 
| logoImage | Image | Optional. Set a visible image to draw in addition to the imperceptible watermark. The demonstration of Verimatrix Watermarking uses this field to draw Verimatrix logo. <br/> Default: None | 
| logoPos | Array | Set coordinates for the logo image. <br/> Format: [x, y, width, height]<br/> Default: Upper left corner of the video | 
| apiToken | String | Optional. Opaque string for activating subsequent API actions. <br/> If you provide apiToken in the arguments for WmSdkInitWatermark(), you must provide the same apiToken in subsequent update() and finish() calls |

### Watermarking Update

Is needed to update the watermarking to be sure that is in the correct position always, for this we can use the update() method which receive the wmInfo Object, You can also use update() to change the watermark parameters.

If you provided apiToken in the argument for WmSdkInitWatermark(), you must 
provide the same apiToken in update() in order to change any parameters.

You must call update() when the layout of the elements on the browser window may 
have changed. You must call update() on entering or leaving fullscreen mode. It is best practice to call update() on each known event that may affect layout, and also periodically to handle any other layout 
changing events.

```js

	var callBackWithPlayers = function (nexplayerInstance, videoElement) {
		...

		wmInfo.strength = 250;
		function onFullScreen() {
			watermarkContext.update(wmInfo);
		}
		document.addEventListener('fullscreenchange', onFullScreen);

		...
	}

```

### Watermarking Finish

After the video playback is finished, we can remove the watermark using the method finish(), to call the only parameter needed is the apiToken.

```js
	var callBackWithPlayers = function (nexplayerInstance, videoElement) {
		...

		videoElement.addEventListener('ended', function (event) {
			console.log("ended");
			watermarkContext.finish(wmInfo);
		},true);

		...
	}

```

***
<a id="youtube-top"> </a>

##  YouTube

### Sample
    
  YouTube API integrated in html5

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
				padding-top: 50.625%;
				/* 16:9 Aspect Ratio 56.25 * 0.9 */
				position: relative;
				background-color: rgba !important;
			}

			#player {
				background-color: black;
				position: absolute;
				top: 0px;
				width: 100%;
				height: 100%;
			}
		</style>
	</head>
	<body>
		<div id="player_container">
			<div id="player" width="530" height="315"></div>
		</div>
		<script src="NexPlayer Library"></script>
		<script>

			var YouTubePlayer = new nexplayer.YouTubePlayer();
			var player;

			YouTubePlayer.init("REPLACE THIS WITH YOUR CUSTOMER KEY");

				function onYouTubeIframeAPIReady() {
				player = new YT.Player("player", {
					height: '360',
					width: '640',
					startSeconds: 0,
					videoId: YouTubePlayer.URL('https://www.youtube.com/watch?v=Yelb7w9cjVg'),
					events: {
						'onReady': onPlayerReady,
					}
				});
			}

			function onPlayerReady(event) {
				event.target.playVideo();
			}
		</script>
	</body>
</html>

```

### Step-by-Step

To integrate NexPlayer™ YouTube into your project you must complete the following steps:

- The NexPlayer™ JavaScript library should be included in the HTML file:

```html
	<script src="NexPlayer Library"></script>

```

<div class="alert alert-success hints-alert"><div class="hints-icon"><i class="fa fa-mortar-board"></i></div><div class="hints-container"><p>Please note that the use of https to call our library is mandatory. </p>
</div></div>

A div that will contain the videos and the UI has to be declared:

```html
	<div id="player_container">
		<div id="player" width="530" height="315"></div>
	</div>

```

To create the youtube player we first need to declare the youtube class. Once created, we declare a <a href="https://developers.google.com/youtube/iframe_api_reference" target="_blank">variable</a>, which is the one that will host all the YouTube methods.

```js

	var YouTubePlayer = new nexplayer.YouTubePlayer();
	var player;

```

Once the player is initialized we create a function that will load the content of the video. Using the previous variable, we are going to set the YouTube instance.

```js

	YouTubePlayer.init("REPLACE THIS WITH YOUR CUSTOMER KEY");

	function onYouTubeIframeAPIReady() {
		player = new YT.Player("player", {
			height: '360',
			width: '640',
			startSeconds: 0,
			videoId: YouTubePlayer.URL('https://www.youtube.com/watch?v=Yelb7w9cjVg'),
		});
	}

```
