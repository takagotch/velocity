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

$element.velocity({
  translateX: [ 500, 0 ],
  opacity: [ 0, "easeInSine", 1 ]
});

$element
  .velocity("slideDown", { duration: 1500 })
  .velocity("slideUp", { delay: 500, duration: 1500 });

$element
  .velocity("scroll", { duration: 1500, easing: "spring" })
  .velocity({ opacity: 1 });
  
$element.velocity("scroll", { container: $("#container") });

$element.velocity("scroll", { axis: "x" });

$element
  .velocity("scroll", { duration: 750, offset: 250 })
  .velocity("scroll", { duration: 750, offset: -50 });

$("html").velocity("scroll", { offset: "750px", mobileHA: false });

$element.velocity("stop");
$element.velocity("stop", "myQueue");

$element.velocity({ opacity: 0 });
$element
  .velocity("stop")
  .velocity("reverse");
  
$element
  .velocity({ width: 100 }, 1000)
  .velocity({ height: 200 }, 1000);
$element.velocity("stop", true);  
  
$allElements.velocity({ opacity: 0 });
$allElements.velocity("stop");
$firstElement.velocity("stop");

$elemnt.velocity("finish");

$element.velocity("reverse");
$element.velocity("reverse", { duration: 2000 });

$element.velocity({
  translateX: "200px",
  rotateZ: "45deg"
});

$element.velocity({
  translateZ: 0,
  translateX: "200px",
  rotateZ: "45deg"
});

$element.velocity({
  backgroundColor: "#ff0000",
  backgroundColorAlpha: 0.5,
  colorRed: "50%",
  colorBlue: "+=50",
  colorAlpha: 0.85
});

$svgRectangle.velocity({
  x: 200,
  r: 25,
  translateX: "200px",
  translateZ: "200px",
  fill: "#ff0000",
  strokeRed: 255,
  strokeGreen: 0,
  strokeBlue: 0,
  opacity: 1,
  width: "50%"
});

$element.velocity({ textShadowBlur: "10px" });

$.Velocity.hook($element, "translateX", "500px");
$.Velocity.hook(elementNode, "textShadowBlur", "10px");
$.Velocity.hook($element, "translateX");
$.Velocity.hook(elementNode, "textShadowBlur");

$.Velocity.animate(element, { opacity: 0.5 })
  .then(funciton(elements){ console.log("Resolved."); })
  .catch(funciton(error){ console.log("Rejected."); });
  
$.Velocity.mock = 10;

var divs = document.getElementByTagName("div");
$.Velocity(divs, { opacity: 0 }, { duration: 1500 });

var divs = document.getElementByTagName("div");
$.Velocity({ opacity: 0 }, o: { duration: 1500 });

$element.velocity({
  opacity: function(){ return Math.random() }
});

$element.velocity({
  translateX: funciton(i, total){
    return i * 10;
  }
});

$element
  .velocity({ translateX: [ 500, 0 ] })
  .velocity({ translateX: 1000 })

$element1.velocity({ translateX: 100 }, 1000, function(){
  $element2.velocity({ translateX: 200 }, 1000, function(){
    $element3.velocity({ translateX: 300 }, 1000);
  });
});

var mySequence = [
  { e: $element1, p: { translateX: 100 }, o: { duration: 1000 },
  { e: $element2, p: { translateX: 200 }, o: { duration: 1000, sequenceQueue: false },
  { e: $element3, p: { translateX: 300 }, o: { duration: 1000 }
];
$.Velocity.RunSequence(mySequence);

$.Velocity.RegisterEffect(name, {
  defaultDuration: duration,
  calls: [
    [ { property: value }, durationPercentage, { options } ],
    [ { property: value }, durationPercentage, { options } ]
  ],
  reset: { property: value, property: value }
});

$Velocity.RegisterEffect("callout.pulse", {
  defaultDuration: 900,
  calls: [
    [ { scaleX: 1.1 }, 0.50 ],
    [ { scaleX: 1 }, 0.50 ]
  ]
});
$element.velocity("callout.pulse");

$.Velocity
  .RegisterEffect("transition.flipXIn", {
    defaultDuration: 700,
    calls: [
      [ { opacity: 1, rotateY: [ 0, -55 ] } ]
    ]
  });
  .RegisterEffect("transition.flipXOut". {
    defaultDuration: 700,
    calls: [
      [ { opacity: 0, rotateY: 55 } ]
    ],
    reset: { rotateY: 0 }
  });

$element
  .velocity("transition.flipXIn")
  .velocity("transition.flipXOut", { delay: 1000 });

$element.velocity("transition.flipXIn", { display: null });

(function(d) { var vmd=d.createElement("script"); vmd.src="https://julian.com/velocity/vmd.min.js"; d.body.appendChild(vmd); })(document);
```

```
```

```
```

