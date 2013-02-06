# jquery-imagefit-plugin

This jQuery plugin makes it easy to have images resize horizontally and vertically to fit the available container width.

It is useful for flexible or fluid web page layouts or when the you don’t have control over the dimensions of the images being loaded.

## How to use
### In your HTML
Link the plugin into your page along with jQuery:

	<script type="text/javascript" src="jquery.js"></script>
	<script type="text/javascript" src="jquery.imagefit.js"></script>
### In your JavaScript
Where '#content' is a jQuery selector for the container (or containers) inside which you want images to resize:

	$(function(){
		$('#content').imagefit();
	});
If the images do not have widths and heights explicitly set it is important to ensure they are loaded before the plugin is applied:

	$(window).load(function(){
		$('#content').imagefit();
	});
Only images whose native size is wider than their container will be resized. Resizing the browser window will cause the images to scale dynamically. Works beautifully in webkit. Needs some work before it is Internet Explorer friendly.

## More info
Demo <http://www.ollicle.com/eg/jquery/imagefit/>

Original <http://www.ollicle.com/2007/aug/17/nnwstyle_jquery_template.html>

Used in <http://wordpress.org/extend/plugins/wp-imagefit/>