# Android in-app update for Appcelerator Titanium

<img src="assets/immediate_flow.png"/>

## Example

To test it make sure to read: https://developer.android.com/guide/playcore/in-app-updates/test

```js
var inappUpdate = require("ti.inappupdate");

inappUpdate.addEventListener("update", function(e) {
	console.log("Has update", e.update);
	if (e.update){
		inappUpdate.startUpdate();
	}
});
inappUpdate.checkForUpdate();

Ti.App.addEventListener("resume", function(){
  inappUpdate.resumeUpdate();
})

inappUpdate.addEventListener("resume", function(e) {
  console.log("resuming update");
});
inappUpdate.addEventListener("error", function(e) {
  console.log(e);
});

inappUpdate.addEventListener("done", function(e) {
  console.log("done");
});

```

## Author
Michael Gangolf (<a href="https://github.com/m1ga">@MichaelGangolf</a> / <a href="https://www.migaweb.de">Web</a>)


<span class="badge-buymeacoffee"><a href="https://www.buymeacoffee.com/miga" title="donate"><img src="https://img.shields.io/badge/buy%20me%20a%20coke-donate-orange.svg" alt="Buy Me A Coke donate button" /></a></span>
