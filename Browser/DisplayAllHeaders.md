```
javascript:(function(){function read(url){var r=new XMLHttpRequest();r.open('HEAD',url,false);r.send(null);return r.getAllResponseHeaders();}alert(read(window.location))})();
```
or
```
javascript:(function(){function read(url){var r=new XMLHttpRequest();r.open('HEAD',url,false);r.send(null);return r.getAllResponseHeaders();}console.log(read(window.location))})();
```
