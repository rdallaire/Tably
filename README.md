# Tably

a simple, lightweight plugin for creating tabbed content and storing active tab to cookie.

## Installation

This script requires the use of the jQuery cookies to take advantage of the active tab being stored to a cookie. It is recommended that you use this feature. You can download the jQuery Cookie library <a href="https://github.com/carhartl/jquery-cookie">here</a>, thanks to <a href="https://github.com/carhartl">Klaus Hartl</a>. This plugin creates a tab:content relationship by assigning 'data-index' to a tab and it's corresponding content. All you have to do is define your tab selectors, and the corresponding content selectors, and this scipt does the rest!

```html
<script src="/path/to/jquery.cookie.js"></script>
<script src="/path/to/tably.js"></script>
```

**Please do not unclude the scripts directly from GitHub.**

## Usage

Instantiate the Tably Plugin.
```javascript
$(function() {
	$.tably({
		// Define your options here
	});
}
```

## Configure

Setup options & selectors for your plugin config.
```javascript
$(function() {
	$.tably({
		activeClass:          	'active',					// Class assigned to active tab + content
		tabContainer:         	'#tabContainer',			// Container holding your tabs
		tabContentContainer:  	'#tabContentContainer',		// Container holding tabbed content
		tabSelector:          	'.tab',						// Selector for your tabs
		contentSelector:      	'.tabContent',				// Selector for your tabbed content
		tabTransition:        	true						// Whether or not to fade between tabbed content
		enableSaving:			true						// Enable cookies to save active tab
	});
}
```
## Sample HTML Markup

Use the configuration script *above* to help better understand the relationship between the Tably Plugin and the HTML Markup provide below. The above config settings are the defaults setup in the Tably Plugin. The HTML markup below assumes the default settings in the Tably Plugin. 

**Note: There should be me as many tabContent's as there are tabs, to create even tab:content relationship**


```html
<nav id="tabContainer">
	<a href="#" class="tab"></a>
	<a href="#" class="tab"></a>
	<a href="#" class="tab"></a>
	<a href="#" class="tab"></a>
</nav>
		
<section id="tabContentContainer">
	<div class="tabContent"></div>
	<div class="tabContent"></div>
	<div class="tabContent"></div>
	<div class="tabContent"></div>
</section>
```






