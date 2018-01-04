# js-best-practise
The result is based on [jeben](http://jsben.ch/browse).

During the test, I got different result in different result, in one benchmark.Some times the chart even has some error.
worng result
![](img/C8227164-B8C0-4E65-B0B8-A1962B0E4E58.png)

##### Array grouping

use reduce [link](http://jsben.ch/hVhEV)

```js
var groupable = [];
var keyPropertyName = 'key';
var valuePropertyName = 'value';

var keys = ["Lord", "Of", "The", "Rings"];
for (var i = 0; i < 1000; i++) {
    var keyIndex = Math.round(Math.random() * 4);
    var obj = {};

    obj[keyPropertyName] = keys[keyIndex];
    obj[valuePropertyName] = i;

    groupable.push(obj);
}

groupable.reduce(function (obj, item) {
    (obj[item[keyPropertyName]] = obj[item[keyPropertyName]] || []).push(item);
    return obj;
}, groups);

var result = Object.keys(groups) === 4;

```
![](img/C40D36AC-7E9F-48C9-BE89-7F1D5158FDE5.png)

##### check object key
use in or hasOwnProperty [link](http://jsben.ch/WqlIl)

```js
var testObj = {a: 28, b: 82, c: "hello", d: 983, e: 'lara', o: "key", f: '82828', g: 8};

var result;
if ("key" in testObj) {
    result = true;
}

var result;
if (testObj.hasOwnProperty("key")) {
    result = true;
}

```
![](img/0590FE53-F2C4-4C5D-90E3-5B1CC07EC697.png)

##### JS loop
```js

```
worng result
![](img/C8227164-B8C0-4E65-B0B8-A1962B0E4E58.png)

##### JS loop
```js

```
worng result
![](img/C8227164-B8C0-4E65-B0B8-A1962B0E4E58.png)

##### JS loop
```js

```
worng result
![](img/C8227164-B8C0-4E65-B0B8-A1962B0E4E58.png)



##### PieChartLabels
Inspired by [Pie charts labels](http://bl.ocks.org/dbuezas/9306799)

![](preview/pieLabel.png)

##### Radia
Inspired by [基于D3.js的雷达图的实现](http://xgfe.github.io/2015/11/24/chenwubai/d3-basicCharts-radar/)

![](preview/radia.png)
