```js
var inappUpdate = require("ti.inappupdate");

inappUpdate.addEventListener("update", function(e) {
	console.log("Has update", e.update);
	if (e.update){
		inappUpdate.startUpdate();
	}
});
inappUpdate.checkForUpdate();

$.index.addEventListener("resume", function(){
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
