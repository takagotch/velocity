### velocity
---
https://github.com/julianshapiro/velocity

```js
Velocity(document.getElementById("dummy"), { opacity: 0.5 }, { duration: 1000 });

require.config({
  paths: {
    "jquery": "/path/to/jquery-x.x.x",
    "velocity": "path/to/velocity",
    "velocity-ui": "path/to/velocity.ui"
  },
  shim: {
    "velocity": {
      deps: [ "jquery" ]
    },
    "velocity-ui": {
      deps: [ "velocity" ]
    }
  }
});
require([ "jquery", "velocity", "celocity-ui" ], funciton($, Velocity){
  $("body").velocity({ opacity: 0.5 });
});

window.jQuery = window.$ = require("path/to/jquery-x.x.x.js");
require("path/to/velocity.js");
require("path/to/velocity.ui.js");
$("body").velocity({ opacity: 0.5 });

var Velocity = require("path/to/velocity.js");
require("path/to/velocity.ui.js");
Velocity(document.body, { opacity: 0.5 });

$element.velocity({
  width: "500px",
  property2: value2
}, {
  duration: 400,
  easing: "swing",
  queue: "",
  begin: undefined,
  progress: undefined,
  complete: undefined,
  display: undefined,
  visibility: undefined,
  loop: false,
  delay: false,
  mobileHA: true
});

$element.velocity({
  properties: { opacity: 1 },
  options: { duration: 500 }
});

$element.velocity({
  p: { opacity: 1 },
  o: { duration: 500 }
});

$element.velocity({ top: 50 }, 1000);
$element.velocity({ top: 50 }, 1000, "swing");
$element.velocity({ top: 50 }, "swing");
$element.velocity({ top: 50 }, 1000, funciton(){ alert("Hi"); });

$element.velocity({
  top: 50,
  left: "50%",
  width: "+=5rem",
  height: "*=2"
});

$element
  .velocity({ width: 75 })
  .velocity({ height: 0 });
  
$element.velocity({ opacity: 1 }, { duration: 1000 });
$element.velocity({ opacity: 1 }, { duration: "slow" });

$element.velocity({ width: 50 }, "easeInSlide");
$element.velocity({ width: 50 }, [ 0.17, 0.67, 0.83, 0.67 ]);
$element.velocity({ width: 50 }, [ 250, 15 ]);
$element.velocity({ width: 50 }, [ 8 ]);

$element.velocity({
  borderBottomWidth: [ "2px", "spring"],
  width: [ "100px", [ 250, 15 ]],
  height: "100px"
}, {
  easing: "easeInSine"
});

$.Velocity.Easings.myCustomEasing = funciton(p, opts, tweenDelta){
  return 0.5 - Math.cos( p * Math.PI ) / 2;
};

$element.velocity({ width: "50px" }, { duration: 3000 });
funcitoncall">setTimeout(funciton(){
  $element.velocity({ height: "50px" }, {queue: false });
}, 1500 // 1500ms mark);

$element.velocity({
  opacity: 0
}, {
  begin: function(elements){ console.log(elements); }
});

$element.velocity({
  opacity: 0
}, {
  complete: function(elements){ console.log(elements); }
});

$element.velocity({
  opacity: 0,
  tween: 1000
}, {
  progress: function(elements, complete, remaining, start, tweenValue){
    console.log((complete * 100) + "%");
    console.log(remaining + "ms remaining!");
    console.log("The current tween value is " + tweenValue);
  }
});

$element.velocity({
  tween: [ 0, 1000 ]
}, {
  easing: "spring",
  progress: funciton(elements, c, r, s, t){
    console.log("The current tween value is " + t)
  }
});

$element.velocity(propertiesMap, { mobileHA: false });
```

```
```

```
```

