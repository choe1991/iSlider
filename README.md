<h1 id="intro">iSlider，Smooth slider for webapps</h1>

iSlider is a high performance，dependency free, mobile-platform javascript slider.
It can handle any elements that need to be slide, like picture list or different dom elements. 
It features:

* Animation can be customized with user defined functions (rotate, 3d, default).
* You can easily hook to a plethora of custom events (onslidestart, onslide, onslideend, onslidechange)
* Damping effect, Infinite Looping, Autometic sliding and Vertical/Horizontal Sliding can be configured.

<h2 id="getting-started">Getting Started</h2>
The best way to learn the iScroll is by looking at the demos. In the archive you'll find a demo folderMost of the script features are outlined there.
*iSlider* is a class that needs to be initiated for each dom area. 

Before you start, you need to prepare some data for iSlider:

``` javascript
var data = [{
	height: 475,
	width: 400,
	content: "imgs/1.jpg",
},{
	height: 527,
	width: 400,
	content: "imgs/2.jpg",
},{
 	height: 400,
 	width: 512,
 	content: "imgs/3.jpg",
}];
```

HTML structure you only need to prepare is :
	
	<div id="iSlider-wrapper"></div>

To make it runnable, all you need to do is to initiate:

 	<script type="text/javascript">
    	var mySlider = new ISlider({
    		dom : document.getElementById('iSlider-wrapper'),
    		data : data
    	});
    </script>

That's it. 

<h2 id="configuration">Configure the iSlider</h2>
Besides the basic ways you can do with iSlider, you can customized the features we provide. For example, if you prefers to put dom elements on the list, you can change the data array like this:

``` javascript
var data = [{
	'height' : '100%',
	'width' : '100%',
	'content' : '<div><h1>Home</h1><h2>This is home page</h2><p>home is pretty awsome</p><div>'
},{
	'height' : '100%',
	'width' : '100%',
	'content' : '<div><h1>Page1</h1><h2>This is page1</h2><p>page1 is pretty awsome</p><div>'
},{
	'height' : '100%',
	'width' : '100%',
	'content' : '<div><h1>Page2</h1><h2>This is Page2</h2><p>Page2 is pretty awsome</p><div>'
}];
```
If you hope to implement the effects mentioned in introduction part, you can:

	<script type="text/javascript">
    	var mySlider = new ISlider({
    		dom : document.getElementById('iSlider-wrapper'),
    		data : data,
    		duration: 2000,
		    isVertical: true,
		    isLooping: true,
		    isDebug: true,
		    isAutoplay: true
    	});
    </script>

<h2 id="understanding">Understand The iSlider</h2>
<table>
<thead>
	<tr>
		<td>Option</td>
		<td>Value</td>
		<td>Description</td>
	</tr>
</thead>
<tbody>
	<tr>
		<td>dom</td>
		<td>HTML Object</td>
		<td>The DOM element that wraps image list</td>
	</tr>
	<tr>
		<td>data</td>
		<td>Array of Content(picture | html)</td>
		<td>Picture data, for example:
		<pre>
[{
	height: 377,
	width: 600,
	content:"pics/1.jpg"
}]
		</pre>
		</td>
	</tr>
	<tr>
		<td>type</td>
		<td>String (pic | dom)</td>
		<td>Default value is 'pic', 'dom' is also supported</td>
	</tr>
	<tr>
		<td>duration</td>
		<td>Integer (1000 == 1s)</td>
		<td>Time gap when an image slides</td>
	</tr>
	<tr>
		<td>ulClass</td>
		<td>String</td>
		<td>CSS class name of ul</td>
	</tr>
	<tr>
		<td>liClass</td>
		<td>String</td>
		<td>CSS class name of li</td>
	</tr>
	<tr>
		<td>onslide</td>
		<td>Function</td>
		<td>Callback function when your finger is moving</td>
	</tr>
	<tr>
		<td>onslidestart</td>
		<td>Function</td>
		<td>Callback function when your finger touch the screen</td>
	</tr>
	<tr>
		<td>onslideend</td>
		<td>Function</td>
		<td>Callback function when your finger move out of the screen</td>
	</tr>
	<tr>
		<td>onslidechange</td>
		<td>Function</td>
		<td>Callback function when the autoplay mode is on and one image slides</td>
	</tr>
	<tr>
		<td>isDebug</td>
		<td>Boolean (true | false)</td>
		<td>Turn on/off the debug mode. Some debug message will output</td>
	</tr>
	<tr>
		<td>isLooping</td>
		<td>Boolean (true | false)</td>
		<td>Turn on/off infinite looping mode</td>
	</tr>
	<tr>
		<td>isAutoplay</td>
		<td>Boolean (true | false)</td>
		<td>Turn of/off autoplay mode</td>
	</tr>
		<tr>
		<td>isVertical</td>
		<td>Boolean (true | fasle)</td>
		<td>Slide verically or horizontally</td>
	</tr>
</tbody>
</table>

<h2 id="license">License (MIT)</h2>

Copyright (c) 2014 Matteo Spinelli

[MIT](https://github.com/BE-FE/MSlider/blob/master/LICENSE)