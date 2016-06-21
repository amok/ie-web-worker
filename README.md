# A bit of retrospective

It is actually WebWorkers stub for IE (or whatever, http://caniuse.com/#feat=webworkers :)

As noticed below, originally hosted on Google Code

Project was moved here, and issue [importScripts not supported](https://code.google.com/archive/p/ie-web-worker/issues/1) was fixed

So it's working stub now

ie-web-worker
=============
A simple script that emulates web worker threads in Internet Explorer.

This project was originally built by Jason Taylor and moved with permission to Github from a Google Code project at http://code.google.com/p/ie-web-worker/.

The code will still be slow (single-threaded) but you can keep you code consistent.

###Usage

```javascript
var worker = new Worker("your_script.js");  
worker.onmessage = function(event) {  
	alert("Got: " + event.data);  
};  
worker.onerror = function(error) {  
	alert("Worker error: " + error.message);  
};  
worker.postMessage("Hello World"); 
```

For more info on worker threads see https://developer.mozilla.org/En/Using_web_workers
