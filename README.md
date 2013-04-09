# Backbone.Events => Events

This is the Backbone Events system without any other Backbone extras. It is taken from version 1.0 of Backbone, and it is currently dependent on the underscore (or lodash) library. Extra support has been added for AMD compatibility.

Use with [RequireJS](http://requirejs.org/):

```javascript
define(['events'], function (Events) {
	Events.on('user:update', function () {
        //updated
    });
});

...

define(['events'], function (Events) {
    Events.trigger('user:update');
});
```

When using with RequireJS, make sure to define underscore in your config:

```javascript
require.config({
    ...
    paths: {
        underscore: 'lib/lodash'
    }
    ...
})
```

Or just use it in the global context:

```javascript
$(function (){
    Events.trigger('ready');
})
```

All credit goes to the original Backbone developers.
