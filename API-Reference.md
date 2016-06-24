> **API Reference**

**The [D3 4.0 API Reference](https://github.com/d3/d3/blob/master/API.md) has moved. This page describes the D3 3.x API.**

Everything in D3 is scoped under the `d3` namespace.

D3 uses [semantic versioning](http://semver.org). You can find the current version of D3 as `d3.version`.

See one of:

* [Core](#d3-core) - selections, transitions, data, localization, colors, etc.
* [Scales](#d3scale-scales) - convert between data and visual encodings
* [SVG](#d3svg-svg) - utilities for creating Scalable Vector Graphics
* [Time](#d3time-time) - parse or format times, compute calendar intervals, etc.
* [Layouts](#d3layout-layouts) - derive secondary data for positioning elements
* [Geography](#d3geo-geography) - project spherical coordinates, latitude & longitude math
* [Geometry](#d3geom-geometry) - utilities for 2D geometry, such as Voronoi diagrams and quadtrees
* [Behaviors](#d3behavior-behaviors) - reusable interaction behaviors

## [d3 (core)](Core.md)

### [Selections](Selections.md)

* [d3.select](Selections.md#d3_select) - select an element from the current document.
* [d3.selectAll](Selections.md#d3_selectAll) - select multiple elements from the current document.
* [selection.attr](Selections.md#attr) - get or set attribute values.
* [selection.classed](Selections.md#classed) - add or remove CSS classes.
* [selection.style](Selections.md#style) - get or set style properties.
* [selection.property](Selections.md#property) - get or set raw properties.
* [selection.text](Selections.md#text) - get or set text content.
* [selection.html](Selections.md#html) - get or set inner HTML content.
* [selection.append](Selections.md#append) - create and append new elements.
* [selection.insert](Selections.md#insert) - create and insert new elements before existing elements.
* [selection.remove](Selections.md#remove) - remove elements from the document.
* [selection.data](Selections.md#data) - get or set data for a group of elements, while computing a relational join.
* [selection.enter](Selections.md#enter) - returns placeholders for missing elements.
* [selection.exit](Selections.md#exit) - returns elements that are no longer needed.
* [selection.datum](Selections.md#datum) - get or set data for individual elements, without computing a join.
* [selection.filter](Selections.md#filter) - filter a selection based on data.
* [selection.sort](Selections.md#sort) - sort elements in the document based on data.
* [selection.order](Selections.md#order) - reorders elements in the document to match the selection.
* [selection.on](Selections.md#on) - add or remove event listeners for interaction.
* [selection.transition](Selections.md#transition) - start a transition on the selected elements.
* [selection.interrupt](Selections.md#interrupt) - immediately interrupt the current transition, if any.
* [selection.each](Selections.md#each) - call a function for each selected element.
* [selection.call](Selections.md#call) - call a function passing in the current selection.
* [selection.empty](Selections.md#empty) - returns true if the selection is empty.
* [selection.node](Selections.md#node) - returns the first node in the selection.
* [selection.size](Selections.md#size) - returns the number of elements in the selection.
* [selection.select](Selections.md#select) - subselect a descendant element for each selected element.
* [selection.selectAll](Selections.md#selectAll) - subselect multiple descendants for each selected element.
* [d3.selection](Selections.md#d3_selection) - augment the selection prototype, or test instance types.
* [d3.event](Selections.md#d3_event) - access the current user event for interaction.
* [d3.mouse](Selections.md#d3_mouse) - gets the mouse position relative to a specified container.
* [d3.touch](Selections.md#d3_touch) - gets a touch position relative to a specified container.
* [d3.touches](Selections.md#d3_touches) - gets the touch positions relative to a specified container.

### [Transitions](Transitions.md)

* [d3.transition](Transitions.md#d3_transition) - start an animated transition.
* [transition.delay](Transitions.md#delay) - specify per-element delay in milliseconds.
* [transition.duration](Transitions.md#duration) - specify per-element duration in milliseconds.
* [transition.ease](Transitions.md#ease) - specify transition easing function.
* [transition.attr](Transitions.md#attr) - smoothly transition to the new attribute value.
* [transition.attrTween](Transitions.md#attrTween) - smoothly transition between two attribute values.
* [transition.style](Transitions.md#style) - smoothly transition to the new style property value.
* [transition.styleTween](Transitions.md#styleTween) - smoothly transition between two style property values.
* [transition.text](Transitions.md#text) - set the text content when the transition starts.
* [transition.tween](Transitions.md#tween) - specify a custom tween operator to run as part of the transition.
* [transition.select](Transitions.md#select) - start a transition on a descendant element for each selected element.
* [transition.selectAll](Transitions.md#selectAll) - start a transition on multiple descendants for each selected element.
* [transition.filter](Transitions.md#filter) - filter a transition based on data.
* [transition.transition](Transitions.md#transition) - when this transition ends, start another one on the same elements.
* [transition.remove](Transitions.md#remove) - remove selected elements at the end of a transition.
* [transition.empty](Transitions.md#empty) - returns true if the transition is empty.
* [transition.node](Transitions.md#node) - returns the first node in the transition.
* [transition.size](Transitions.md#size) - returns the number of elements in the selection.
* [transition.each](Transitions.md#each) - add a listener for transition end events.
* [transition.call](Transitions.md#call) - call a function passing in the current transition.
* [d3.ease](Transitions.md#d3_ease) - customize transition timing.
* [ease](Transitions.md#_ease) - a parametric easing function.
* [d3.timer](Transitions.md#d3_timer) - start a custom animation timer.
* [d3.timer.flush](Transitions.md#d3_timer_flush) - immediately execute any zero-delay timers.
* [d3.interpolate](Transitions.md#d3_interpolate) - interpolate two values.
* [interpolate](Transitions.md#_interpolate) - a parametric interpolation function.
* [d3.interpolateNumber](Transitions.md#d3_interpolateNumber) - interpolate two numbers.
* [d3.interpolateRound](Transitions.md#d3_interpolateRound) - interpolate two integers.
* [d3.interpolateString](Transitions.md#d3_interpolateString) - interpolate two strings.
* [d3.interpolateRgb](Transitions.md#d3_interpolateRgb) - interpolate two RGB colors.
* [d3.interpolateHsl](Transitions.md#d3_interpolateHsl) - interpolate two HSL colors.
* [d3.interpolateLab](Transitions.md#d3_interpolateLab) - interpolate two L\*a\*b\* colors.
* [d3.interpolateHcl](Transitions.md#d3_interpolateHcl) - interpolate two HCL colors.
* [d3.interpolateArray](Transitions.md#d3_interpolateArray) - interpolate two arrays of values.
* [d3.interpolateObject](Transitions.md#d3_interpolateObject) - interpolate two arbitrary objects.
* [d3.interpolateTransform](Transitions.md#d3_interpolateTransform) - interpolate two 2D matrix transforms.
* [d3.interpolateZoom](Transitions.md#d3_interpolateZoom) - zoom and pan between two points smoothly.
* [d3.interpolators](Transitions.md#d3_interpolators) - register a custom interpolator.

### [Working with Arrays](Arrays.md)

* [d3.ascending](Arrays.md#d3_ascending) - compare two values for sorting.
* [d3.descending](Arrays.md#d3_descending) - compare two values for sorting.
* [d3.min](Arrays.md#d3_min) - find the minimum value in an array.
* [d3.max](Arrays.md#d3_max) - find the maximum value in an array.
* [d3.extent](Arrays.md#d3_extent) - find the minimum and maximum value in an array.
* [d3.sum](Arrays.md#d3_sum) - compute the sum of an array of numbers.
* [d3.mean](Arrays.md#d3_mean) - compute the arithmetic mean of an array of numbers.
* [d3.median](Arrays.md#d3_median) - compute the median of an array of numbers (the 0.5-quantile).
* [d3.quantile](Arrays.md#d3_quantile) - compute a quantile for a sorted array of numbers.
* [d3.variance](Arrays.md#d3_variance) - compute the variance of an array of numbers.
* [d3.deviation](Arrays.md#d3_deviation) - compute the standard deviation of an array of numbers.
* [d3.bisect](Arrays.md#d3_bisect) - search for a value in a sorted array.
* [d3.bisectRight](Arrays.md#d3_bisectRight) - search for a value in a sorted array.
* [d3.bisectLeft](Arrays.md#d3_bisectLeft) - search for a value in a sorted array.
* [d3.bisector](Arrays.md#d3_bisector) - bisect using an accessor or comparator.
* [d3.shuffle](Arrays.md#d3_shuffle) - randomize the order of an array.
* [d3.permute](Arrays.md#d3_permute) - reorder an array of elements according to an array of indexes.
* [d3.zip](Arrays.md#d3_zip) - transpose a variable number of arrays.
* [d3.transpose](Arrays.md#d3_transpose) - transpose an array of arrays.
* [d3.pairs](Arrays.md#d3_pairs) - returns an array of adjacent pairs of elements.
* [d3.keys](Arrays.md#d3_keys) - list the keys of an associative array.
* [d3.values](Arrays.md#d3_values) - list the values of an associated array.
* [d3.entries](Arrays.md#d3_entries) - list the key-value entries of an associative array.
* [d3.merge](Arrays.md#d3_merge) - merge multiple arrays into one array.
* [d3.range](Arrays.md#d3_range) - generate a range of numeric values.
* [d3.nest](Arrays.md#d3_nest) - group array elements hierarchically.
* [nest.key](Arrays.md#nest_key) - add a level to the nest hierarchy.
* [nest.sortKeys](Arrays.md#nest_sortKeys) - sort the current nest level by key.
* [nest.sortValues](Arrays.md#nest_sortValues) - sort the leaf nest level by value.
* [nest.rollup](Arrays.md#nest_rollup) - specify a rollup function for leaf values.
* [nest.map](Arrays.md#nest_map) - evaluate the nest operator, returning an associative array.
* [nest.entries](Arrays.md#nest_entries) - evaluate the nest operator, returning an array of key-values tuples.
* [d3.map](Arrays.md#d3_map) - a shim for ES6 maps, since objects are not hashes!
* [map.has](Arrays.md#map_has) - returns true if the map contains the specified key.
* [map.get](Arrays.md#map_get) - returns the value for the specified key.
* [map.set](Arrays.md#map_set) - sets the value for the specified key.
* [map.remove](Arrays.md#map_remove) - removes the entry for specified key.
* [map.keys](Arrays.md#map_keys) - returns the map’s array of keys.
* [map.values](Arrays.md#map_values) - returns the map’s array of values.
* [map.entries](Arrays.md#map_entries) - returns the map’s array of entries (key-values objects).
* [map.forEach](Arrays.md#map_forEach) - calls the specified function for each entry in the map.
* [map.empty](Arrays.md#map_empty) - returns false if the map has at least one entry.
* [map.size](Arrays.md#map_size) - returns the number of entries in the map.
* [d3.set](Arrays.md#d3_set) - a shim for ES6 sets, since objects are not hashes!
* [set.has](Arrays.md#set_has) - returns true if the set contains the specified value.
* [set.add](Arrays.md#set_add) - adds the specified value.
* [set.remove](Arrays.md#set_remove) - removes the specified value.
* [set.values](Arrays.md#set_values) - returns the set’s array of values.
* [set.forEach](Arrays.md#set_forEach) - calls the specified function for each value in the set.
* [set.empty](Arrays.md#set_empty) - returns false if the set has at least one value.
* [set.size](Arrays.md#set_size) - returns the number of values in the set.

### [Math](Math.md)

* [d3.random.normal](Math.md#random_normal) - generate a random number with a normal distribution.
* [d3.random.logNormal](Math.md#random_logNormal) - generate a random number with a log-normal distribution.
* [d3.random.bates](Math.md#random_bates) - generate a random number with a Bates distribution.
* [d3.random.irwinHall](Math.md#random_irwinHall) - generate a random number with an Irwin–Hall distribution.
* [d3.transform](Math.md#d3_transform) - compute the standard form of a 2D matrix transform.

### [Loading External Resources](Requests.md)

* [d3.xhr](Requests.md#d3_xhr) - request a resource using XMLHttpRequest.
* [xhr.header](Requests.md#header) - set a request header.
* [xhr.mimeType](Requests.md#mimeType) - set the Accept request header and override the response MIME type.
* [xhr.response](Requests.md#response) - set a response mapping function.
* [xhr.get](Requests.md#get) - issue a GET request.
* [xhr.post](Requests.md#post) - issue a POST request.
* [xhr.send](Requests.md#send) - issue a request with the specified method and data.
* [xhr.abort](Requests.md#abort) - abort an outstanding request.
* [xhr.on](Requests.md#on) - add an event listener for "progress", "load" or "error" events.
* [d3.text](Requests.md#d3_text) - request a text file.
* [d3.json](Requests.md#d3_json) - request a JSON blob.
* [d3.html](Requests.md#d3_html) - request an HTML document fragment.
* [d3.xml](Requests.md#d3_xml) - request an XML document fragment.
* [d3.csv](CSV.md) - request a comma-separated values (CSV) file.
* [d3.tsv](CSV.md#tsv) - request a tab-separated values (TSV) file.

### [String Formatting](Formatting.md)

* [d3.format](Formatting.md#d3_format) - format a number as a string.
* [d3.formatPrefix](Formatting.md#d3_formatPrefix) - returns the [SI prefix](http://en.wikipedia.org/wiki/Metric_prefix) for the specified value and precision.
* [d3.requote](Formatting.md#d3_requote) - quote a string for use in a regular expression.
* [d3.round](Formatting.md#d3_round) - rounds a value to some digits after the decimal point.

### [CSV Formatting (d3.csv)](CSV.md)

* [d3.csv](CSV.md#csv) - request a comma-separated values (CSV) file.
* [d3.csv.parse](CSV.md#parse) - parse a CSV string into objects using the header row.
* [d3.csv.parseRows](CSV.md#parseRows) - parse a CSV string into tuples, ignoring the header row.
* [d3.csv.format](CSV.md#format) - format an array of objects into a CSV string.
* [d3.csv.formatRows](CSV.md#formatRows) - format an array of tuples into a CSV string.
* [d3.tsv](CSV.md#tsv) - request a tab-separated values (TSV) file.
* [d3.tsv.parse](CSV.md#tsv_parse) - parse a TSV string into objects using the header row.
* [d3.tsv.parseRows](CSV.md#tsv_parseRows) - parse a TSV string into tuples, ignoring the header row.
* [d3.tsv.format](CSV.md#tsv_format) - format an array of objects into a TSV string.
* [d3.tsv.formatRows](CSV.md#tsv_formatRows) - format an array of tuples into a TSV string.
* [d3.dsv](CSV.md#dsv) - create a parser/formatter for the specified delimiter and mime type.

### [Localization](Localization.md)

* [d3.locale](Localization.md#d3_locale) - create a new locale using the specified strings.
* [locale.numberFormat](Localization.md#locale_numberFormat) - create a new number formatter.
* [locale.timeFormat](Localization.md#locale_timeFormat) - create a new time formatter / parser.

### [Colors](Colors.md)

* [d3.rgb](Colors.md#d3_rgb) - specify a color in RGB space.
* [rgb.brighter](Colors.md#rgb_brighter) - increase RGB channels by some exponential factor (gamma).
* [rgb.darker](Colors.md#rgb_darker) - decrease RGB channels by some exponential factor (gamma).
* [rgb.hsl](Colors.md#rgb_hsl) - convert from RGB to HSL.
* [rgb.toString](Colors.md#rgb_toString) - convert an RGB color to a string.
* [d3.hsl](Colors.md#d3_hsl) - specify a color in HSL space.
* [hsl.brighter](Colors.md#hsl_brighter) - increase lightness by some exponential factor (gamma).
* [hsl.darker](Colors.md#hsl_darker) - decrease lightness by some exponential factor (gamma).
* [hsl.rgb](Colors.md#hsl_rgb) - convert from HSL to RGB.
* [hsl.toString](Colors.md#hsl_toString) - convert an HSL color to a string.
* [d3.lab](Colors.md#d3_lab) - specify a color in L\*a\*b\* space.
* [lab.brighter](Colors.md#lab_brighter) - increase lightness by some exponential factor (gamma).
* [lab.darker](Colors.md#lab_darker) - decrease lightness by some exponential factor (gamma).
* [lab.rgb](Colors.md#lab_rgb) - convert from L\*a\*b\* to RGB.
* [lab.toString](Colors.md#lab_toString) - convert a L\*a\*b\* color to a string.
* [d3.hcl](Colors.md#d3_hcl) - specify a color in HCL space.
* [hcl.brighter](Colors.md#hcl_brighter) - increase lightness by some exponential factor (gamma).
* [hcl.darker](Colors.md#hcl_darker) - decrease lightness by some exponential factor (gamma).
* [hcl.rgb](Colors.md#hcl_rgb) - convert from HCL to RGB.
* [hcl.toString](Colors.md#hcl_toString) - convert an HCL color to a string.

### [Namespaces](Namespaces.md)

* [d3.ns.prefix](Namespaces.md#prefix) - access or extend known XML namespaces.
* [d3.ns.qualify](Namespaces.md#qualify) - qualify a prefixed name, such as "xlink:href".

### [Internals](Internals.md)

* [d3.functor](Internals.md#functor) - create a function that returns a constant.
* [d3.rebind](Internals.md#rebind) - rebind an inherited getter/setter method to a subclass.
* [d3.dispatch](Internals.md#d3_dispatch) - create a custom event dispatcher.
* [dispatch.on](Internals.md#dispatch_on) - register or unregister an event listener.
* [dispatch.type](Internals.md#_dispatch) - dispatch an event to registered listeners.

## [d3.scale (Scales)](Scales.md)

### [Quantitative](Quantitative-Scales.md#quantitative)

* [d3.scale.linear](Quantitative-Scales.md#linear) - construct a linear quantitative scale.
* [linear](Quantitative-Scales.md#_linear) - get the range value corresponding to a given domain value.
* [linear.invert](Quantitative-Scales.md#linear_invert) - get the domain value corresponding to a given range value.
* [linear.domain](Quantitative-Scales.md#linear_domain) - get or set the scale's input domain.
* [linear.range](Quantitative-Scales.md#linear_range) - get or set the scale's output range.
* [linear.rangeRound](Quantitative-Scales.md#linear_rangeRound) - set the scale's output range, and enable rounding.
* [linear.interpolate](Quantitative-Scales.md#linear_interpolate) - get or set the scale's output interpolator.
* [linear.clamp](Quantitative-Scales.md#linear_clamp) - enable or disable clamping of the output range.
* [linear.nice](Quantitative-Scales.md#linear_nice) - extend the scale domain to nice round numbers.
* [linear.ticks](Quantitative-Scales.md#linear_ticks) - get representative values from the input domain.
* [linear.tickFormat](Quantitative-Scales.md#linear_tickFormat) - get a formatter for displaying tick values.
* [linear.copy](Quantitative-Scales.md#linear_copy) - create a new scale from an existing scale.
* [d3.scale.sqrt](Quantitative-Scales.md#sqrt) - construct a quantitative scale with a square root transform.
* [d3.scale.pow](Quantitative-Scales.md#pow) - construct a quantitative scale with an exponential transform.
* [pow](Quantitative-Scales.md#_pow) - get the range value corresponding to a given domain value.
* [pow.invert](Quantitative-Scales.md#pow_invert) - get the domain value corresponding to a given range value.
* [pow.domain](Quantitative-Scales.md#pow_domain) - get or set the scale's input domain.
* [pow.range](Quantitative-Scales.md#pow_range) - get or set the scale's output range.
* [pow.rangeRound](Quantitative-Scales.md#pow_rangeRound) - set the scale's output range, and enable rounding.
* [pow.interpolate](Quantitative-Scales.md#pow_interpolate) - get or set the scale's output interpolator.
* [pow.clamp](Quantitative-Scales.md#pow_clamp) - enable or disable clamping of the output range.
* [pow.nice](Quantitative-Scales.md#pow_nice) - extend the scale domain to nice round numbers.
* [pow.ticks](Quantitative-Scales.md#pow_ticks) - get representative values from the input domain.
* [pow.tickFormat](Quantitative-Scales.md#pow_tickFormat) - get a formatter for displaying tick values.
* [pow.exponent](Quantitative-Scales.md#pow_exponent) - get or set the exponent power.
* [pow.copy](Quantitative-Scales.md#pow_copy) - create a new scale from an existing scale.
* [d3.scale.log](Quantitative-Scales.md#log) - construct a quantitative scale with a logarithmic transform.
* [log](Quantitative-Scales.md#_log) - get the range value corresponding to a given domain value.
* [log.invert](Quantitative-Scales.md#log_invert) - get the domain value corresponding to a given range value.
* [log.domain](Quantitative-Scales.md#log_domain) - get or set the scale's input domain.
* [log.range](Quantitative-Scales.md#log_range) - get or set the scale's output range.
* [log.rangeRound](Quantitative-Scales.md#log_rangeRound) - set the scale's output range, and enable rounding.
* [log.base](Quantitative-Scales.md#log_base) - get or set the scale's logarithmic base.
* [log.interpolate](Quantitative-Scales.md#log_interpolate) - get or set the scale's output interpolator.
* [log.clamp](Quantitative-Scales.md#log_clamp) - enable or disable clamping of the output range.
* [log.nice](Quantitative-Scales.md#log_nice) - extend the scale domain to nice powers of ten.
* [log.ticks](Quantitative-Scales.md#log_ticks) - get representative values from the input domain.
* [log.tickFormat](Quantitative-Scales.md#log_tickFormat) - get a formatter for displaying tick values.
* [log.copy](Quantitative-Scales.md#log_copy) - create a new scale from an existing scale.
* [d3.scale.quantize](Quantitative-Scales.md#quantize) - construct a linear quantitative scale with a discrete output range.
* [quantize](Quantitative-Scales.md#_quantize) - get the range value corresponding to a given domain value.
* [quantize.invertExtent](Quantitative-Scales.md#quantize_invertExtent) - get the domain values for the specified range value.
* [quantize.domain](Quantitative-Scales.md#quantize_domain) - get or set the scale's input domain.
* [quantize.range](Quantitative-Scales.md#quantize_range) - get or set the scale's output range (as discrete values).
* [quantize.copy](Quantitative-Scales.md#quantize_copy) - create a new scale from an existing scale.
* [d3.scale.threshold](Quantitative-Scales.md#threshold) - construct a threshold scale with a discrete output range.
* [threshold](Quantitative-Scales.md#_threshold) - get the range value corresponding to a given domain value.
* [threshold.invertExtent](Quantitative-Scales.md#threshold_invertExtent) - get the domain values for the specified range value.
* [threshold.domain](Quantitative-Scales.md#threshold_domain) - get or set the scale's input domain.
* [threshold.range](Quantitative-Scales.md#threshold_range) - get or set the scale's output range (as discrete values).
* [threshold.copy](Quantitative-Scales.md#threshold_copy) - create a new scale from an existing scale.
* [d3.scale.quantile](Quantitative-Scales.md#quantile) - construct a quantitative scale mapping to quantiles.
* [quantile](Quantitative-Scales.md#_quantile) - get the range value corresponding to a given domain value.
* [quantile.invertExtent](Quantitative-Scales.md#quantile_invertExtent) - get the domain values for the specified range value.
* [quantile.domain](Quantitative-Scales.md#quantile_domain) - get or set the scale's input domain (as discrete values).
* [quantile.range](Quantitative-Scales.md#quantile_range) - get or set the scale's output range (as discrete values).
* [quantile.quantiles](Quantitative-Scales.md#quantile_quantiles) - get the scale's quantile bin thresholds.
* [quantile.copy](Quantitative-Scales.md#quantile_copy) - create a new scale from an existing scale.
* [d3.scale.identity](Quantitative-Scales.md#identity) - construct a linear identity scale.
* [identity](Quantitative-Scales.md#_identity) - the identity function.
* [identity.invert](Quantitative-Scales.md#_identity) - equivalent to identity; the identity function.
* [identity.domain](Quantitative-Scales.md#identity_domain) - get or set the scale's domain and range.
* [identity.range](Quantitative-Scales.md#identity_domain) - equivalent to identity.domain.
* [identity.ticks](Quantitative-Scales.md#identity_ticks) - get representative values from the domain.
* [identity.tickFormat](Quantitative-Scales.md#identity_tickFormat) - get a formatter for displaying tick values.
* [identity.copy](Quantitative-Scales.md#identity_copy) - create a new scale from an existing scale.

### [Ordinal](Ordinal-Scales.md#ordinal)

* [d3.scale.ordinal](Ordinal-Scales.md#ordinal) - construct an ordinal scale.
* [ordinal](Ordinal-Scales.md#_ordinal) - get the range value corresponding to a given domain value.
* [ordinal.domain](Ordinal-Scales.md#ordinal_domain) - get or set the scale's input domain.
* [ordinal.range](Ordinal-Scales.md#ordinal_range) - get or set the scale's output range.
* [ordinal.rangePoints](Ordinal-Scales.md#ordinal_rangePoints) - divide a continuous output range for discrete points.
* [ordinal.rangeRoundPoints](Ordinal-Scales.md#ordinal_rangeRoundPoints) - divide a continuous output range for discrete points.
* [ordinal.rangeBands](Ordinal-Scales.md#ordinal_rangeBands) - divide a continuous output range for discrete bands.
* [ordinal.rangeRoundBands](Ordinal-Scales.md#ordinal_rangeRoundBands) - divide a continuous output range for discrete bands.
* [ordinal.rangeBand](Ordinal-Scales.md#ordinal_rangeBand) - get the discrete range band width.
* [ordinal.rangeExtent](Ordinal-Scales.md#ordinal_rangeExtent) - get the minimum and maximum values of the output range.
* [ordinal.copy](Ordinal-Scales.md#ordinal_copy) - create a new scale from an existing scale.
* [d3.scale.category10](Ordinal-Scales.md#category10) - construct an ordinal scale with ten categorical colors.
* [d3.scale.category20](Ordinal-Scales.md#category20) - construct an ordinal scale with twenty categorical colors.
* [d3.scale.category20b](Ordinal-Scales.md#category20b) - construct an ordinal scale with twenty categorical colors.
* [d3.scale.category20c](Ordinal-Scales.md#category20c) - construct an ordinal scale with twenty categorical colors.

## [d3.svg (SVG)](SVG.md)

### [Shapes](SVG-Shapes.md)

* [d3.svg.line](SVG-Shapes.md#line) - create a new line generator.
* [line](SVG-Shapes.md#_line) - generate a piecewise linear curve, as in a line chart.
* [line.x](SVG-Shapes.md#line_x) - get or set the *x*-coordinate accessor.
* [line.y](SVG-Shapes.md#line_y) - get or set the *y*-coordinate accessor.
* [line.interpolate](SVG-Shapes.md#line_interpolate) - get or set the interpolation mode.
* [line.tension](SVG-Shapes.md#line_tension) - get or set the cardinal spline tension.
* [line.defined](SVG-Shapes.md#line_defined) - control whether the line is defined at a given point.
* [d3.svg.line.radial](SVG-Shapes.md#line_radial) - create a new radial line generator.
* [line](SVG-Shapes.md#_line_radial) - generate a piecewise linear curve, as in a polar line chart.
* [line.radius](SVG-Shapes.md#line_radial_radius) - get or set the *radius* accessor.
* [line.angle](SVG-Shapes.md#line_radial_angle) - get or set the *angle* accessor.
* [line.interpolate](SVG-Shapes.md#line_radial_interpolate) - get or set the interpolation mode.
* [line.tension](SVG-Shapes.md#line_radial_tension) - get or set the cardinal spline tension.
* [line.defined](SVG-Shapes.md#line_radial_defined) - control whether the line is defined at a given point.
* [d3.svg.area](SVG-Shapes.md#area) - create a new area generator.
* [area](SVG-Shapes.md#_area) - generate a piecewise linear area, as in an area chart.
* [area.x](SVG-Shapes.md#area_x) - get or set the *x*-coordinate accessors.
* [area.x0](SVG-Shapes.md#area_x0) - get or set the *x0*-coordinate (baseline) accessor.
* [area.x1](SVG-Shapes.md#area_x1) - get or set the *x1*-coordinate (topline) accessor.
* [area.y](SVG-Shapes.md#area_y) - get or set the *y*-coordinate accessors.
* [area.y0](SVG-Shapes.md#area_y0) - get or set the *y0*-coordinate (baseline) accessor.
* [area.y1](SVG-Shapes.md#area_y1) - get or set the *y1*-coordinate (topline) accessor.
* [area.interpolate](SVG-Shapes.md#area_interpolate) - get or set the interpolation mode.
* [area.tension](SVG-Shapes.md#area_tension) - get or set the cardinal spline tension.
* [area.defined](SVG-Shapes.md#area_defined) - control whether the area is defined at a given point.
* [d3.svg.area.radial](SVG-Shapes.md#area_radial) - create a new area generator.
* [area](SVG-Shapes.md#_area_radial) - generate a piecewise linear area, as in a polar area chart.
* [area.radius](SVG-Shapes.md#area_radial_radius) - get or set the *radius* accessors.
* [area.innerRadius](SVG-Shapes.md#area_radial_innerRadius) - get or set the inner *radius* (baseline) accessor.
* [area.outerRadius](SVG-Shapes.md#area_radial_outerRadius) - get or set the outer *radius* (topline) accessor.
* [area.angle](SVG-Shapes.md#area_radial_angle) - get or set the *angle* accessors.
* [area.startAngle](SVG-Shapes.md#area_radial_startAngle) - get or set the *angle* (baseline) accessor.
* [area.endAngle](SVG-Shapes.md#area_radial_endAngle) - get or set the *angle* (topline) accessor.
* [area.defined](SVG-Shapes.md#area_radial_defined) - control whether the area is defined at a given point.
* [d3.svg.arc](SVG-Shapes.md#arc) - create a new arc generator.
* [arc](SVG-Shapes.md#_arc) - generate a solid arc, as in a pie or donut chart.
* [arc.innerRadius](SVG-Shapes.md#arc_innerRadius) - get or set the inner radius accessor.
* [arc.outerRadius](SVG-Shapes.md#arc_outerRadius) - get or set the outer radius accessor.
* [arc.cornerRadius](SVG-Shapes.md#arc_cornerRadius) - get or set the corner radius accessor.
* [arc.padRadius](SVG-Shapes.md#arc_padRadius) - get or set the pad radius accessor.
* [arc.startAngle](SVG-Shapes.md#arc_startAngle) - get or set the start angle accessor.
* [arc.endAngle](SVG-Shapes.md#arc_endAngle) - get or set the end angle accessor.
* [arc.padAngle](SVG-Shapes.md#arc_padAngle) - get or set the pad angle accessor.
* [arc.centroid](SVG-Shapes.md#arc_centroid) - compute the arc centroid.
* [d3.svg.symbol](SVG-Shapes.md#symbol) - create a new symbol generator.
* [symbol](SVG-Shapes.md#_symbol) - generate categorical symbols, as in a scatterplot.
* [symbol.type](SVG-Shapes.md#symbol_type) - get or set the symbol type accessor.
* [symbol.size](SVG-Shapes.md#symbol_size) - get or set the symbol size (in square pixels) accessor.
* [d3.svg.symbolTypes](SVG-Shapes.md#symbolTypes) - the array of supported symbol types.
* [d3.svg.chord](SVG-Shapes.md#chord) - create a new chord generator.
* [chord](SVG-Shapes.md#_chord) - generate a quadratic Bézier connecting two arcs, as in a chord diagram.
* [chord.radius](SVG-Shapes.md#chord_radius) - get or set the arc radius accessor.
* [chord.startAngle](SVG-Shapes.md#chord_startAngle) - get or set the arc start angle accessor.
* [chord.endAngle](SVG-Shapes.md#chord_endAngle) - get or set the arc end angle accessor.
* [chord.source](SVG-Shapes.md#chord_source) - get or set the source arc accessor.
* [chord.target](SVG-Shapes.md#chord_target) - get or set the target arc accessor.
* [d3.svg.diagonal](SVG-Shapes.md#diagonal) - create a new diagonal generator.
* [diagonal](SVG-Shapes.md#_diagonal) - generate a two-dimensional Bézier connector, as in a node-link diagram.
* [diagonal.source](SVG-Shapes.md#diagonal_source) - get or set the source point accessor.
* [diagonal.target](SVG-Shapes.md#diagonal_target) - get or set the target point accessor.
* [diagonal.projection](SVG-Shapes.md#diagonal_projection) - get or set an optional point transform.
* [d3.svg.diagonal.radial](SVG-Shapes.md#diagonal_radial) - create a new diagonal generator.
* [diagonal](SVG-Shapes.md#_diagonal_radial) - generate a two-dimensional Bézier connector, as in a node-link diagram.

### [Axes](SVG-Axes.md)

* [d3.svg.axis](SVG-Axes.md#axis) - create a new axis generator.
* [axis](SVG-Axes.md#_axis) - creates or updates an axis for the given selection or transition.
* [axis.scale](SVG-Axes.md#scale) - get or set the axis scale.
* [axis.orient](SVG-Axes.md#orient) - get or set the axis orientation.
* [axis.ticks](SVG-Axes.md#ticks) - control how ticks are generated for the axis.
* [axis.tickValues](SVG-Axes.md#tickValues) - specify tick values explicitly.
* [axis.tickSize](SVG-Axes.md#tickSize) - specify the size of major, minor and end ticks.
* [axis.innerTickSize](SVG-Axes.md#innerTickSize) - specify the size of inner ticks.
* [axis.outerTickSize](SVG-Axes.md#outerTickSize) - specify the size of outer ticks.
* [axis.tickPadding](SVG-Axes.md#tickPadding) - specify padding between ticks and tick labels.
* [axis.tickFormat](SVG-Axes.md#tickFormat) - override the tick formatting for labels.

### [Controls](SVG-Controls.md)

* [d3.svg.brush](SVG-Controls.md#brush) - click and drag to select one- or two-dimensional regions.
* [brush](SVG-Controls.md#_brush) - apply a brush to the given selection or transition.
* [brush.x](SVG-Controls.md#brush_x) - the brush’s <i>x</i>-scale, for horizontal brushing.
* [brush.y](SVG-Controls.md#brush_y) - the brush’s <i>y</i>-scale, for vertical brushing.
* [brush.extent](SVG-Controls.md#brush_extent) - the brush’s extent in zero, one or two dimensions.
* [brush.clear](SVG-Controls.md#brush_clear) - reset the brush extent.
* [brush.empty](SVG-Controls.md#brush_empty) - whether or not the brush extent is empty.
* [brush.on](SVG-Controls.md#brush_on) - listeners for when the brush is moved.
* [brush.event](SVG-Controls.md#brush_event) - dispatch brush events after setting the extent.

## [d3.time (Time)](Time.md)

### [Time Formatting](Time-Formatting.md)

* [d3.time.format](Time-Formatting.md#format) - create a new local time formatter for a given specifier.
* [format](Time-Formatting.md#_format) - format a date into a string.
* [format.parse](Time-Formatting.md#parse) - parse a string into a date.
* [d3.time.format.multi](Time-Formatting.md#format_multi) - create a new local multi-resolution time formatter.
* [d3.time.format.utc](Time-Formatting.md#format_utc) - create a new UTC time formatter for a given specifier.
* [d3.time.format.iso](Time-Formatting.md#format_iso) - the ISO 8601 UTC time formatter.

### [Time Scales](Time-Scales.md)

* [d3.time.scale](Time-Scales.md#scale) - construct a linear time scale.
* [scale](Time-Scales.md#_scale) - get the range value corresponding to a given domain value.
* [scale.invert](Time-Scales.md#invert) - get the domain value corresponding to a given range value.
* [scale.domain](Time-Scales.md#domain) - get or set the scale's input domain.
* [scale.nice](Time-Scales.md#nice) - extend the scale domain to nice round numbers.
* [scale.range](Time-Scales.md#range) - get or set the scale's output range.
* [scale.rangeRound](Time-Scales.md#rangeRound) - set the scale's output range, and enable rounding.
* [scale.interpolate](Time-Scales.md#interpolate) - get or set the scale's output interpolator.
* [scale.clamp](Time-Scales.md#clamp) - enable or disable clamping of the output range.
* [scale.ticks](Time-Scales.md#ticks) - get representative values from the input domain.
* [scale.tickFormat](Time-Scales.md#tickFormat) - get a formatter for displaying tick values.
* [scale.copy](Time-Scales.md#copy) - create a new scale from an existing scale.

### [Time Intervals](Time-Intervals.md)

* [d3.time.interval](Time-Intervals.md#interval) - a time interval in local time.
* [interval](Time-Intervals.md#_interval) - alias for interval.floor.
* [interval.range](Time-Intervals.md#interval_range) - returns dates within the specified range.
* [interval.floor](Time-Intervals.md#interval_floor) - rounds down to the nearest interval.
* [interval.round](Time-Intervals.md#interval_round) - rounds up or down to the nearest interval.
* [interval.ceil](Time-Intervals.md#interval_ceil) - rounds up to the nearest interval.
* [interval.offset](Time-Intervals.md#interval_offset) - returns a date offset by some interval.
* [interval.utc](Time-Intervals.md#interval_utc) - returns the UTC-equivalent time interval.
* [d3.time.day](Time-Intervals.md#day) - every day (12:00 AM).
* [d3.time.days](Time-Intervals.md#day) - alias for day.range.
* [d3.time.dayOfYear](Time-Intervals.md#dayOfYear) - computes the day number.
* [d3.time.hour](Time-Intervals.md#hour) - every hour (e.g., 1:00 AM).
* [d3.time.hours](Time-Intervals.md#hours) - alias for hour.range.
* [d3.time.minute](Time-Intervals.md#minute) - every minute (e.g., 1:02 AM).
* [d3.time.minutes](Time-Intervals.md#minutes) - alias for minute.range.
* [d3.time.month](Time-Intervals.md#month) - every month (e.g., February 1, 12:00 AM).
* [d3.time.months](Time-Intervals.md#months) - alias for month.range.
* [d3.time.second](Time-Intervals.md#second) - every second (e.g., 1:02:03 AM).
* [d3.time.seconds](Time-Intervals.md#seconds) - alias for second.range.
* [d3.time.sunday](Time-Intervals.md#sunday) - every Sunday (e.g., February 5, 12:00 AM).
* [d3.time.sundays](Time-Intervals.md#sundays) - alias for sunday.range.
* [d3.time.sundayOfYear](Time-Intervals.md#sundayOfYear) - computes the sunday-based week number.
* [d3.time.monday](Time-Intervals.md#monday) - every Monday (e.g., February 5, 12:00 AM).
* [d3.time.mondays](Time-Intervals.md#mondays) - alias for monday.range.
* [d3.time.mondayOfYear](Time-Intervals.md#mondayOfYear) - computes the monday-based week number.
* [d3.time.tuesday](Time-Intervals.md#tuesday) - every Tuesday (e.g., February 5, 12:00 AM).
* [d3.time.tuesdays](Time-Intervals.md#tuesdays) - alias for tuesday.range.
* [d3.time.tuesdayOfYear](Time-Intervals.md#tuesdayOfYear) - computes the tuesday-based week number.
* [d3.time.wednesday](Time-Intervals.md#wednesday) - every Wednesday (e.g., February 5, 12:00 AM).
* [d3.time.wednesdays](Time-Intervals.md#wednesdays) - alias for wednesday.range.
* [d3.time.wednesdayOfYear](Time-Intervals.md#tuesdayOfYear) - computes the wednesday-based week number.
* [d3.time.thursday](Time-Intervals.md#thursday) - every Thursday (e.g., February 5, 12:00 AM).
* [d3.time.thursdays](Time-Intervals.md#thursdays) - alias for thursday.range.
* [d3.time.thursdayOfYear](Time-Intervals.md#thursdayOfYear) - computes the thursday-based week number.
* [d3.time.friday](Time-Intervals.md#friday) - every Friday (e.g., February 5, 12:00 AM).
* [d3.time.fridays](Time-Intervals.md#fridays) - alias for friday.range.
* [d3.time.fridayOfYear](Time-Intervals.md#fridayOfYear) - computes the friday-based week number.
* [d3.time.saturday](Time-Intervals.md#saturday) - every Saturday (e.g., February 5, 12:00 AM).
* [d3.time.saturdays](Time-Intervals.md#saturdays) - alias for saturday.range.
* [d3.time.saturdayOfYear](Time-Intervals.md#saturdayOfYear) - computes the saturday-based week number.
* [d3.time.week](Time-Intervals.md#week) - alias for sunday.
* [d3.time.weeks](Time-Intervals.md#weeks) - alias for sunday.range.
* [d3.time.weekOfYear](Time-Intervals.md#weekOfYear) - alias for sundayOfYear.
* [d3.time.year](Time-Intervals.md#year) - every year (e.g., January 1, 12:00 AM).
* [d3.time.years](Time-Intervals.md#years) - alias for year.range.

## [d3.layout (Layouts)](Layouts.md)

### [Bundle](Bundle-Layout.md)

* [d3.layout.bundle](Bundle-Layout.md#bundle) - construct a new default bundle layout.
* [bundle](Bundle-Layout.md#_bundle) - apply Holten's *hierarchical bundling* algorithm to edges.

### [Chord](Chord-Layout.md)

* [d3.layout.chord](Chord-Layout.md#chord) - produce a chord diagram from a matrix of relationships.
* [chord.matrix](Chord-Layout.md#matrix) - get or set the matrix data backing the layout.
* [chord.padding](Chord-Layout.md#padding) - get or set the angular padding between chord segments.
* [chord.sortGroups](Chord-Layout.md#sortGroups) - get or set the comparator function for groups.
* [chord.sortSubgroups](Chord-Layout.md#sortSubgroups) - get or set the comparator function for subgroups.
* [chord.sortChords](Chord-Layout.md#sortChords) - get or set the comparator function for chords (z-order).
* [chord.chords](Chord-Layout.md#chords) - retrieve the computed chord angles.
* [chord.groups](Chord-Layout.md#groups) - retrieve the computed group angles.

### [Cluster](Cluster-Layout.md)

* [d3.layout.cluster](Cluster-Layout.md#cluster) - cluster entities into a dendrogram.
* [cluster](Cluster-Layout.md#_cluster) - alias for cluster.nodes.
* [cluster.nodes](Cluster-Layout.md#nodes) - compute the cluster layout and return the array of nodes.
* [cluster.links](Cluster-Layout.md#links) - compute the parent-child links between tree nodes.
* [cluster.children](Cluster-Layout.md#children) - get or set the accessor function for child nodes.
* [cluster.sort](Cluster-Layout.md#sort) - get or set the comparator function for sibling nodes.
* [cluster.separation](Cluster-Layout.md#separation) - get or set the spacing function between neighboring nodes.
* [cluster.size](Cluster-Layout.md#size) - get or set the layout size in *x* and *y*.
* [cluster.nodeSize](Cluster-Layout.md#nodeSize) - specify a fixed size for each node.

### [Force](Force-Layout.md)

* [d3.layout.force](Force-Layout.md#force) - position linked nodes using physical simulation.
* [force.on](Force-Layout.md#on) - listen to updates in the computed layout positions.
* [force.nodes](Force-Layout.md#nodes) - get or set the array of nodes to layout.
* [force.links](Force-Layout.md#links) - get or set the array of links between nodes.
* [force.size](Force-Layout.md#size) - get or set the layout size in *x* and *y*.
* [force.linkDistance](Force-Layout.md#linkDistance) - get or set the link distance.
* [force.linkStrength](Force-Layout.md#linkStrength) - get or set the link strength.
* [force.friction](Force-Layout.md#friction) - get or set the friction coefficient.
* [force.charge](Force-Layout.md#charge) - get or set the charge strength.
* [force.chargeDistance](Force-Layout.md#chargeDistance) - get or set the maximum charge distance.
* [force.gravity](Force-Layout.md#gravity) - get or set the gravity strength.
* [force.theta](Force-Layout.md#theta) - get or set the accuracy of the charge interaction.
* [force.start](Force-Layout.md#start) - start or restart the simulation when the nodes change.
* [force.resume](Force-Layout.md#resume) - reheat the cooling parameter and restart simulation.
* [force.stop](Force-Layout.md#stop) - immediately terminate the simulation.
* [force.alpha](Force-Layout.md#alpha) - get or set the layout's cooling parameter.
* [force.tick](Force-Layout.md#tick) - run the layout simulation one step.
* [force.drag](Force-Layout.md#drag) - bind a behavior to nodes to allow interactive dragging.

### [Hierarchy](Hierarchy-Layout.md)

* [d3.layout.hierarchy](Hierarchy-Layout.md#hierarchy) - derive a custom hierarchical layout implementation.
* [hierarchy](Hierarchy-Layout.md#_hierarchy) - alias for hierarchy.nodes.
* [hierarchy.nodes](Hierarchy-Layout.md#nodes) - compute the layout and return the array of nodes.
* [hierarchy.links](Hierarchy-Layout.md#links) - compute the parent-child links between tree nodes.
* [hierarchy.children](Hierarchy-Layout.md#children) - get or set the accessor function for child nodes.
* [hierarchy.sort](Hierarchy-Layout.md#sort) - get or set the comparator function for sibling nodes.
* [hierarchy.value](Hierarchy-Layout.md#value) - get or set the value accessor function.
* [hierarchy.revalue](Hierarchy-Layout.md#revalue) - recompute the hierarchy values.

### [Histogram](Histogram-Layout.md)

* [d3.layout.histogram](Histogram-Layout.md#histogram) - construct a new default histogram layout.
* [histogram](Histogram-Layout.md#_histogram) - compute the distribution of data using quantized bins.
* [histogram.value](Histogram-Layout.md#value) - get or set the value accessor function.
* [histogram.range](Histogram-Layout.md#range) - get or set the considered value range.
* [histogram.bins](Histogram-Layout.md#bins) - specify how values are organized into bins.
* [histogram.frequency](Histogram-Layout.md#frequency) - compute the distribution as counts or probabilities.

### [Pack](Pack-Layout.md)

* [d3.layout.pack](Pack-Layout.md#pack) - produce a hierarchical layout using recursive circle-packing.
* [pack](Pack-Layout.md#_pack) - alias for pack.nodes.
* [pack.nodes](Pack-Layout.md#nodes) - compute the pack layout and return the array of nodes.
* [pack.links](Pack-Layout.md#links) - compute the parent-child links between tree nodes.
* [pack.children](Pack-Layout.md#children) - get or set the children accessor function.
* [pack.sort](Pack-Layout.md#sort) - control the order in which sibling nodes are traversed.
* [pack.value](Pack-Layout.md#value) - get or set the value accessor used to size circles.
* [pack.size](Pack-Layout.md#size) - specify the layout size in *x* and *y*.
* [pack.radius](Pack-Layout.md#radius) - specify the node radius, rather than deriving it from value.
* [pack.padding](Pack-Layout.md#padding) - specify the layout padding in (approximate) pixels.

### [Partition](Partition-Layout.md)

* [d3.layout.partition](Partition-Layout.md#partition) - recursively partition a node tree into a sunburst or icicle.
* [partition](Partition-Layout.md#_partition) - alias for partition.nodes.
* [partition.nodes](Partition-Layout.md#nodes) - compute the partition layout and return the array of nodes.
* [partition.links](Partition-Layout.md#links) - compute the parent-child links between tree nodes.
* [partition.children](Partition-Layout.md#children) - get or set the children accessor function.
* [partition.sort](Partition-Layout.md#sort) - control the order in which sibling nodes are traversed.
* [partition.value](Partition-Layout.md#value) - get or set the value accessor used to size circles.
* [partition.size](Partition-Layout.md#size) - specify the layout size in *x* and *y*.

### [Pie](Pie-Layout.md)

* [d3.layout.pie](Pie-Layout.md#pie) - construct a new default pie layout.
* [pie](Pie-Layout.md#_pie) - compute the start and end angles for arcs in a pie or donut chart.
* [pie.value](Pie-Layout.md#value) - get or set the value accessor function.
* [pie.sort](Pie-Layout.md#sort) - control the clockwise order of pie slices.
* [pie.startAngle](Pie-Layout.md#startAngle) - get or set the overall start angle of the pie.
* [pie.endAngle](Pie-Layout.md#endAngle) - get or set the overall end angle of the pie.
* [pie.padAngle](Pie-Layout.md#padAngle) - get or set the pad angle of the pie.

### [Stack](Stack-Layout.md)

* [d3.layout.stack](Stack-Layout.md#stack) - construct a new default stack layout.
* [stack](Stack-Layout.md#_stack) - compute the baseline for each series in a stacked bar or area chart.
* [stack.values](Stack-Layout.md#values) - get or set the values accessor function per series.
* [stack.order](Stack-Layout.md#order) - control the order in which series are stacked.
* [stack.offset](Stack-Layout.md#offset) - specify the overall baseline algorithm.
* [stack.x](Stack-Layout.md#x) - get or set the *x*-dimension accessor function.
* [stack.y](Stack-Layout.md#y) - get or set the *y*-dimension accessor function.
* [stack.out](Stack-Layout.md#out) - get or set the output function for storing the baseline.

### [Tree](Tree-Layout.md)

* [d3.layout.tree](Tree-Layout.md#tree) - position a tree of nodes tidily.
* [tree](Tree-Layout.md#_tree) - alias for tree.nodes.
* [tree.nodes](Tree-Layout.md#nodes) - compute the tree layout and return the array of nodes.
* [tree.links](Tree-Layout.md#links) - compute the parent-child links between tree nodes.
* [tree.children](Tree-Layout.md#children) - get or set the children accessor function.
* [tree.sort](Tree-Layout.md#sort) - control the order in which sibling nodes are traversed.
* [tree.separation](Tree-Layout.md#separation) - get or set the spacing function between neighboring nodes.
* [tree.size](Tree-Layout.md#size) - specify the layout size in *x* and *y*.
* [tree.nodeSize](Tree-Layout.md#nodeSize) - specify a fixed size for each node.

### [Treemap](Treemap-Layout.md)

* [d3.layout.treemap](Treemap-Layout.md#treemap) - use recursive spatial subdivision to display a tree of nodes.
* [treemap](Treemap-Layout.md#_treemap) - alias for treemap.nodes.
* [treemap.nodes](Treemap-Layout.md#nodes) - compute the treemap layout and return the array of nodes.
* [treemap.links](Treemap-Layout.md#links) - compute the parent-child links between tree nodes.
* [treemap.children](Treemap-Layout.md#children) - get or set the children accessor function.
* [treemap.sort](Treemap-Layout.md#sort) - control the order in which sibling nodes are traversed.
* [treemap.value](Treemap-Layout.md#value) - get or set the value accessor used to size treemap cells.
* [treemap.size](Treemap-Layout.md#size) - specify the layout size in *x* and *y*.
* [treemap.padding](Treemap-Layout.md#padding) - specify the padding between a parent and its children.
* [treemap.round](Treemap-Layout.md#round) - enable or disable rounding to exact pixels.
* [treemap.sticky](Treemap-Layout.md#sticky) - make the layout sticky for stable updates.
* [treemap.mode](Treemap-Layout.md#mode) - change the treemap layout algorithm.

## [d3.geo (Geography)](Geo.md)

### [Paths](Geo-Paths.md)

* [d3.geo.path](Geo-Paths.md#path) - create a new geographic path generator.
* [path](Geo-Paths.md#_path) - project the specified feature and render it to the context.
* [path.projection](Geo-Paths.md#path_projection) - get or set the geographic projection.
* [path.context](Geo-Paths.md#path_context) - get or set the render context.
* [path.pointRadius](Geo-Paths.md#path_pointRadius) - get or set the radius to display point features.
* [path.area](Geo-Paths.md#path_area) - compute the projected area of a given feature.
* [path.centroid](Geo-Paths.md#path_centroid) - compute the projected centroid of a given feature.
* [path.bounds](Geo-Paths.md#path_bounds) - compute the projected bounds of a given feature.
* [d3.geo.graticule](Geo-Paths.md#graticule) - create a graticule generator.
* [graticule](Geo-Paths.md#_graticule) - generate a MultiLineString of meridians and parallels.
* [graticule.lines](Geo-Paths.md#graticule_lines) - generate an array of LineStrings of meridians and parallels.
* [graticule.outline](Geo-Paths.md#graticule_outline) - generate a Polygon of the graticule’s extent.
* [graticule.extent](Geo-Paths.md#graticule_extent) - get or set the major & minor extents.
* [graticule.majorExtent](Geo-Paths.md#graticule_majorExtent) - get or set the major extent.
* [graticule.minorExtent](Geo-Paths.md#graticule_minorExtent) - get or set the minor extent.
* [graticule.step](Geo-Paths.md#graticule_step) - get or set the major & minor step intervals.
* [graticule.majorStep](Geo-Paths.md#graticule_majorStep) - get or set the major step intervals.
* [graticule.minorStep](Geo-Paths.md#graticule_minorStep) - get or set the minor step intervals.
* [graticule.precision](Geo-Paths.md#graticule_precision) - get or set the latitudinal precision.
* [d3.geo.circle](Geo-Paths.md#circle) - create a circle generator.
* [circle](Geo-Paths.md#_circle) - generate a piecewise circle as a Polygon.
* [circle.origin](Geo-Paths.md#circle_origin) - specify the origin in latitude and longitude.
* [circle.angle](Geo-Paths.md#circle_angle) - specify the angular radius in degrees.
* [circle.precision](Geo-Paths.md#circle_precision) - specify the precision of the piecewise circle.
* [d3.geo.area](Geo-Paths.md#area) - compute the spherical area of a given feature.
* [d3.geo.bounds](Geo-Paths.md#bounds) - compute the latitude-longitude bounding box for a given feature.
* [d3.geo.centroid](Geo-Paths.md#centroid) - compute the spherical centroid of a given feature.
* [d3.geo.distance](Geo-Paths.md#distance) - compute the great-arc distance between two points.
* [d3.geo.interpolate](Geo-Paths.md#interpolate) - interpolate between two points along a great arc.
* [d3.geo.length](Geo-Paths.md#length) - compute the length of a line string or the perimeter of a polygon.
* [d3.geo.rotation](Geo-Paths.md#rotation) - create a rotation function for the specified angles [λ, φ, γ].
* [rotation](Geo-Paths.md#_rotation) - rotate the given location around the sphere.
* [rotation.invert](Geo-Paths.md#rotation_invert) - inverse-rotate the given location around the sphere.

### [Projections](Geo-Projections.md)

* [d3.geo.projection](Geo-Projections.md#projection) - create a standard projection from a raw projection.
* [projection](Geo-Projections.md#_projection) - project the specified location.
* [projection.invert](Geo-Projections.md#invert) - invert the projection for the specified point.
* [projection.rotate](Geo-Projections.md#rotate) - get or set the projection’s three-axis rotation.
* [projection.center](Geo-Projections.md#center) - get or set the projection’s center location.
* [projection.translate](Geo-Projections.md#translate) - get or set the projection’s translation position.
* [projection.scale](Geo-Projections.md#scale) - get or set the projection’s scale factor.
* [projection.clipAngle](Geo-Projections.md#clipAngle) - get or set the radius of the projection’s clip circle.
* [projection.clipExtent](Geo-Projections.md#clipExtent) - get or set the projection’s viewport clip extent, in pixels.
* [projection.precision](Geo-Projections.md#precision) - get or set the precision threshold for adaptive resampling.
* [projection.stream](Geo-Projections.md#stream) - wrap the specified stream listener, projecting input geometry.
* [d3.geo.projectionMutator](Geo-Projections.md#projectionMutator) - create a standard projection from a mutable raw projection.
* [d3.geo.albers](Geo-Projections.md#albers) - the Albers equal-area conic projection.
* [albers.parallels](Geo-Projections.md#albers_parallels) - get or set the projection's two standard parallels.
* [d3.geo.albersUsa](Geo-Projections.md#albersUsa) - a composite Albers projection for the United States.
* [d3.geo.azimuthalEqualArea](Geo-Projections.md#azimuthalEqualArea) - the azimuthal equal-area projection.
* [d3.geo.azimuthalEquidistant](Geo-Projections.md#azimuthalEquidistant) - the azimuthal equidistant projection.
* [d3.geo.conicConformal](Geo-Projections.md#conicConformal) - the conic conformal projection.
* [d3.geo.conicEquidistant](Geo-Projections.md#conicEquidistant) - the conic equidistant projection.
* [d3.geo.conicEqualArea](Geo-Projections.md#conicEqualArea) the conic equal-area (a.k.a. Albers) projection.
* [d3.geo.equirectangular](Geo-Projections.md#equirectangular) - the equirectangular (plate carreé) projection.
* [d3.geo.gnomonic](Geo-Projections.md#gnomonic) - the gnomonic projection.
* [d3.geo.mercator](Geo-Projections.md#mercator) - the spherical Mercator projection.
* [d3.geo.orthographic](Geo-Projections.md#orthographic) - the azimuthal orthographic projection.
* [d3.geo.stereographic](Geo-Projections.md#stereographic) - the azimuthal stereographic projection.
* [d3.geo.azimuthalEqualArea.raw](Geo-Projections.md#azimuthalEqualArea_raw) - the raw azimuthal equal-area projection.
* [d3.geo.azimuthalEquidistant.raw](Geo-Projections.md#azimuthalEquidistant_raw) - the azimuthal equidistant projection.
* [d3.geo.conicConformal.raw](Geo-Projections.md#conicConformal_raw) - the raw conic conformal projection.
* [d3.geo.conicEquidistant.raw](Geo-Projections.md#conicEquidistant_raw) - the raw conic equidistant projection.
* [d3.geo.conicEqualArea.raw](Geo-Projections.md#conicEqualArea_raw) the raw conic equal-area (a.k.a. Albers) projection.
* [d3.geo.equirectangular.raw](Geo-Projections.md#equirectangular_raw) - the raw equirectangular (plate carrée) projection.
* [d3.geo.gnomonic.raw](Geo-Projections.md#gnomonic_raw) - the raw gnomonic projection.
* [d3.geo.mercator.raw](Geo-Projections.md#mercator_raw) - the raw Mercator projection.
* [d3.geo.orthographic.raw](Geo-Projections.md#orthographic_raw) - the raw azimuthal orthographic projection.
* [d3.geo.stereographic.raw](Geo-Projections.md#stereographic_raw) - the raw azimuthal stereographic projection.
* [d3.geo.transverseMercator.raw](Geo-Projections.md#transverseMercator_raw) - the raw transverse Mercator projection.

### [Streams](Geo-Streams.md)

* [d3.geo.stream](Geo-Streams.md#stream) - convert a GeoJSON object to a geometry stream.
* [stream.point](Geo-Streams.md#stream_point) - indicate an *x*, *y* (and optionally *z*) coordinate.
* [stream.lineStart](Geo-Streams.md#stream_lineStart) - indicate the start of a line or ring.
* [stream.lineEnd](Geo-Streams.md#stream_lineEnd) - indicate the end of a line or ring.
* [stream.polygonStart](Geo-Streams.md#stream_polygonStart) - indicate the start of a polygon.
* [stream.polygonEnd](Geo-Streams.md#stream_polygonEnd) - indicate the end of a polygon.
* [stream.sphere](Geo-Streams.md#stream_sphere) - indicate a sphere.
* [d3.geo.transform](Geo-Streams.md#transform) - transform streaming geometries.
* [transform.stream](Geo-Streams.md#transform_stream) - wraps a given stream.
* [d3.geo.clipExtent](Geo-Streams.md#clipExtent) - a stream transform that clips geometries to a given axis-aligned rectangle.
* [clipExtent.extent](Geo-Streams.md#clipExtent_extent) - sets the clip extent.

## [d3.geom (Geometry)](Geometry.md)

### [Voronoi](Voronoi-Geom.md)

* [d3.geom.voronoi](Voronoi-Geom.md#voronoi) - create a Voronoi layout with default accessors.
* [voronoi](Voronoi-Geom.md#_voronoi) - compute the Voronoi tessellation for the specified points.
* [voronoi.x](Voronoi-Geom.md#x) - get or set the x-coordinate accessor for each point.
* [voronoi.y](Voronoi-Geom.md#y) - get or set the y-coordinate accessor for each point.
* [voronoi.clipExtent](Voronoi-Geom.md#clipExtent) - get or set the clip extent for the tesselation.
* [voronoi.links](Voronoi-Geom.md#links) - compute the Delaunay mesh as a network of links.
* [voronoi.triangles](Voronoi-Geom.md#triangles) - compute the Delaunay mesh as a triangular tessellation.

### [Quadtree](Quadtree-Geom.md)

* [d3.geom.quadtree](Quadtree-Geom.md#quadtree) - constructs a quadtree for an array of points.
* [quadtree.add](Quadtree-Geom.md#add) - add a point to the quadtree.
* [quadtree.visit](Quadtree-Geom.md#visit) - recursively visit nodes in the quadtree.
* [quadtree.find](Quadtree-Geom.md#find) - find the closest point in the quadtree.

### [Polygon](Polygon-Geom.md)

* [d3.geom.polygon](Polygon-Geom.md#polygon) - create a polygon from the specified array of points.
* [polygon.area](Polygon-Geom.md#area) - compute the counterclockwise area of this polygon.
* [polygon.centroid](Polygon-Geom.md#centroid) - compute the area centroid of this polygon.
* [polygon.clip](Polygon-Geom.md#clip) - clip the specified polygon to this polygon.

### [Hull](Hull-Geom.md)

* [d3.geom.hull](Hull-Geom.md#hull) - create a convex hull layout with default accessors.
* [hull](Hull-Geom.md#_hull) - compute the convex hull for the given array of points.
* [hull.x](Hull-Geom.md#x) - get or set the *x*-coordinate accessor.
* [hull.y](Hull-Geom.md#y) - get or set the *y*-coordinate accessor.

## [d3.behavior (Behaviors)](Behaviors.md)

### [Drag](Drag-Behavior.md)

* [d3.behavior.drag](Drag-Behavior.md#drag)
* [drag.origin](Drag-Behavior.md#origin)
* [drag.on](Drag-Behavior.md#on)

### [Zoom](Zoom-Behavior.md)

* [d3.behavior.zoom](Zoom-Behavior.md#zoom) - create a zoom behavior.
* [zoom](Zoom-Behavior.md#_zoom) - apply the zoom behavior to the selected elements.
* [zoom.scale](Zoom-Behavior.md#scale) - the current scale factor.
* [zoom.translate](Zoom-Behavior.md#translate) - the current translate offset.
* [zoom.scaleExtent](Zoom-Behavior.md#scaleExtent) - optional limits on the scale factor.
* [zoom.center](Zoom-Behavior.md#center) - an optional focal point for mousewheel zooming.
* [zoom.size](Zoom-Behavior.md#size) - the dimensions of the viewport.
* [zoom.duration](Zoom-Behavior.md#duration) - get or set the dblclick transition duration.
* [zoom.x](Zoom-Behavior.md#x) - an optional scale whose domain is bound to the _x_ extent of the viewport.
* [zoom.y](Zoom-Behavior.md#y) - an optional scale whose domain is bound to the _y_ extent of the viewport.
* [zoom.on](Zoom-Behavior.md#on) - listeners for when the scale or translate changes.
* [zoom.event](Zoom-Behavior.md#event) - dispatch zoom events after setting the scale or translate.
