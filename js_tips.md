
``` javascript
var data = obj && obj.data || {};

// shortcut for
var data = {};
if(obj && obj.data) {
  data = obj.data;
}
```
