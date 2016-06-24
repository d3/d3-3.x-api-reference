> [API Reference](API-Reference.md) ▸ **Behaviors**

**The [D3 4.0 API Reference](https://github.com/d3/d3/blob/master/API.md) has moved. This page describes the D3 3.x API.**

Behaviors encapsulate a complex set of low-level DOM interactions (i.e. user gestures that vary between input methods) into a higher-level set of custom events (see [d3.dispatch](Internals.md#d3_dispatch)). Behaviors often allow some additional configuration by the user. D3 includes two built-in behaviors:

* [Drag](Drag-Behavior.md) — tracks mouse or multitouch movement(s) relative to an origin
* [Zoom](Zoom-Behavior.md) — emits zoom and pan events in response to common input idioms

Behaviors are typically functions which you can apply to a selection using its [call operator](Selections.md#call). For example, you can create and apply a behavior to a selection like this:

```
selection.call(d3.behavior.drag().on('dragstart', function (d) {
  console.log("Started moving item with data:", d);
}));
```

Note carefully the nesting: the `'dragstart'` event is registered on the `d3.behavior.drag()` instance, not on the selection! It is this same instance — which is itself also a function — that gets called on the selection. This call allows the behavior to do its own internal setup on the selection.
