## Classes

<dl>
<dt><a href="#BubbleChart">BubbleChart</a></dt>
<dd></dd>
</dl>

## Typedefs

<dl>
<dt><a href="#settings">settings</a> : <code>object</code></dt>
<dd><p>Settings of bubble chart</p>
</dd>
<dt><a href="#data">data</a> : <code>object</code></dt>
<dd><p>Data information</p>
</dd>
</dl>

<a name="BubbleChart"></a>

## BubbleChart
**Kind**: global class  
<a name="new_BubbleChart_new"></a>

### new BubbleChart(settings)
Bubble Chart implementation using [d3js](d3js.org)


| Param | Type | Description |
| --- | --- | --- |
| settings | <code>[settings](#settings)</code> | Settings of bubble chart |

**Example**  
```js
- [test-bubble-chart](../test/test-bubble-chart.html)
```
<a name="settings"></a>

## settings : <code>object</code>
Settings of bubble chart

**Kind**: global typedef  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| plugins | <code>Array.&lt;object&gt;</code> &#124; <code>Array.&lt;string&gt;</code> |  | Array of plugin [microplugin](https://github.com/brianreavis/microplugin.js|microplugin) |
| [container] | <code>string</code> | <code>&quot;\&quot;.bubbleChart\&quot;&quot;</code> | Jquery selector which will contain the chart |
| size | <code>number</code> |  | Size of the chart, in pixel |
| [viewBoxSize] | <code>number</code> | <code>size</code> | Size of the viewport of the chart, in pixel [ViewBoxAttribute](http://www.w3.org/TR/SVG/coords.html#ViewBoxAttribute) |
| [innerRadius] | <code>number</code> | <code>size/3</code> | Radius of the Inner Circle, in pixel |
| [outerRadius] | <code>number</code> | <code>size/2</code> | Radius of the Outer Circle, in pixel |
| [radiusMin] | <code>number</code> | <code>size/10</code> | Minimum radius, in pixel |
| [radiusMax] | <code>number</code> | <code>(outerRadius  innerRadius)/2</code> | Maximum radius, in pixel |
| [intersectDelta] | <code>number</code> | <code>0</code> | Intersection between circles, in pixel |
| [intersectInc] | <code>number</code> | <code>intersectDelta</code> | Increment of settings.intersectDelta, in pixel |
| [transitDuration] | <code>number</code> | <code>1000</code> | Duration of transition when do animations, in mili-seconds |
| data | <code>[data](#data)</code> |  | Data information |

<a name="data"></a>

## data : <code>object</code>
Data information

**Kind**: global typedef  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| items | <code>Array.&lt;object&gt;</code> |  | Array of items <br/> ex: ```js data.items = [{number: 179, label: "something"}, {number: 220, label: "everything"}] ``` |
| eval | <code>function</code> |  | Function should return a number used to evaluate an item <br/> ex: ```js data.eval = function(d){   return d.number; } ``` |
| [color] | <code>function</code> | <code>d3.scale.category20</code> | Function should return a string used to fill bubbles <br/>ex: ```js data.color = function(d){   return "white"; } ``` |

