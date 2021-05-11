<a id="3rdParties-top"> </a>

<a href="https://nexplayer.github.io/NexPlayer_HTML5_Documentation/#/"><img text src="./_images/logo5.png" alt="Nexplayer"></a>

***

# Third Party

This is a summary of how to use third party tools

***

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

        }
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

## Mux Data

Mux data allows you to monitor your video streaming performance.

<img width="50%" text-align="center" src="./_images/mux-chart.png" alt="nexAgo" >

### Using with the player

To start, you need to have a ENV_KEY from the <a href="https://dashboard.mux.com/environments">Mux environments dashboard</a>. ENV_KEY is a client-side key used for Mux Data monitoring.  These are not to be confused with API tokens which are created in the admin settings dashboard and meant to access the Mux API from a trusted server.

In order to use it, you need to import this three files into the html and set the muxPlayerInitTime.

```html
<head>
  <script type="text/javascript" src="https://src.litix.io/core/4/mux.js"></script>
  <script>window.muxPlayerInitTime = Date.now()</script>
</head>
<body>
	<script type="text/javascript" src="NexMuxHandShake.js"></script>
	<script type="text/javascript" src="config.js"></script>
</body>

 ```

 You can find <a href="https://github.com/NexPlayer/NexPlayer_HTML5_Mux/blob/main/app/config.js">confing.js</a> and <a href="https://github.com/NexPlayer/NexPlayer_HTML5_Mux/blob/main/app/NexMuxHandShake.js">NexMuxHandShake.js</a> in the following <a href="https://github.com/NexPlayer/NexPlayer_HTML5_Mux">repository</a>.

 First you should configure your settings in "config.js".

#### muxConfig : <code>Object</code>
**Properties**:

| Param | Type | Description |
| --- | --- | --- |
| debug | <code>boolean</code> | Enable or disable debug mode |
| disableCookies | <code>boolean</code> | Disable or enable the cookie that Mux use to track playback across subsequent page views if desired. |
| respectDoNotTrack | <code>boolean</code> | By default, mux does not respect Do Not Track when set within browsers. This can be enabled or disabled by this property. |
| automaticErrorTracking | <code>boolean</code> | Enable or disable automatic error tracking completely. |
| data | <code>Object</code> | Site, player and video metadata. |


And your muxConfig should look like this:

```js
var muxConfig = {
  debug: true,
  disableCookies: true,
  respectDoNotTrack: true,
  automaticErrorTracking: true,
  data: {
    env_key: 'ENV_KEY', // required

    // Site Metadata
    viewer_user_id: '', // ex: '12345'
    experiment_name: '', // ex: 'player_test_A'
    sub_property_id: '', // ex: 'cus-1'

    // Player Metadata
    player_name: 'NexPlayer', // ex: 'My Main Player'
    player_version:  '', // ex: '1.0.0'
    player_init_time: window.muxPlayerInitTime, // ex: 1451606400000

    // Video Metadata
    video_id: '', // ex: 'abcd123'
    video_title: '', // ex: 'My Great Video'
    video_series: '', // ex: 'Weekly Great Videos'
    video_duration: '', // in milliseconds, ex: 120000
    video_stream_type: '', // 'live' or 'on-demand'
    video_cdn: '' // ex: 'Fastly', 'Akamai'
  },
};
 ```

 NexMuxHandshake should be created in the callBackWithPlayers after the event "loadeddata" is fired. This object links Nexplayer and Mux events and functions.

 ```js

  let nexMux = null;

    var callBackWithPlayers = function (nexplayerInstance, videoElement) {

      player = nexplayerInstance;
      videoElem = videoElement;

      videoElem.addEventListener("loadeddata", function() {

        nexMux = new NexMuxHandShake();
        // To use ad metrics, set useAdMetrics to true, it is set to false by default.
        nexMux.useAdMetrics = true;
        nexMux.initMuxData();
      });
    }
 ```

If your application plays multiple videos back-to-back in the same video player, you should modify the muxConfig variable created in config.js an then use the following code.

```js
nexMux.videoChange(muxConfig);
 ```

In some cases, you may have the program change within a stream, and you may want to track each program as a view on its own. To do so you should modify the muxConfig variable created in config.js an then use the following code.

```js
nexMux.programChange(muxConfig);
```