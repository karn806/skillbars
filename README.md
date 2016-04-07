# Skillbars

Skillbars is a lightweight, responsive solution to adding skill-based progress bars to your website. Skillbars can be easily generated using jQuery and used on portfolios, company pages, and more.

## Installation & Setup

All the installation that is required is simply including the compiled CSS and JS files in your document:

```html
<link rel="stylesheet" type="text/css" href="path/to/skillbars.css">
...
<script src="text/css" href="path/to/skillbars.js"></script>
```

Skillbars will now be available on every page it is included on.
 
## Configuration

There are a number of parameters you may override, or simply use the default provided ones:

 Parameter  | Description | Default
 -------- | ------------- | -----------
color | The color of the progress bars (this can also be overwritten with custom css if left at default | #000
style | Choose a style that comes with the plugin or make your own (see below) | 1
showLevel | Choose whether or not to show the numerical value of the skillbar | false
animate | Choose whether or not to animate the skillbars when loaded | true
speed | The speed at which the bars are animated (in milliseconds) | 300

## Example Usage

An example usage showing each parameter is as follows:

```javascript
$('#myID').skillbars({
    color: '#000',
    style: 1,
    showLevel: true,
    animate: true,
    speed: 300
});
```

## Customization

### Option 1 - Changing Defaults

There are 2 basic defaults that can be changed in order to alter the styles: *color* and *style* (see above).

If you wish to have customization beyond the bar color and general styles provided with the plugin, see option 2.

### Option 2 - Creating Custom Styles

You can easily create custom styles by overriding the generated elements. The elements and their corresponding functions are:

 Element  | Description
 -------- | ------------- |
 .skillbars | Overall ul that contains all the skillbars
 .skillbar | Individual skillbar wrapper
 .skillbar-text | The individual skillbar label
 .skillbar-bar | The skillbar background
 .skillbar-level | The colored skillbar that shows the level
 .skillbar-percent | The percentage value of the skillbar level (on created if *showLevel* set to true)
 
Alternative, you can also create your own styles and only apply them to certain skillbar groups by using the *style* parameter. For example:

```javascript
$('#myID').skillbars({
    style: 'coolstyle',
});
```

Which would add *skillbar-style-coolstyle* to the wrapper, which can be customized by separate CSS:

```CSS
ul.skillbar-style-coolstyle span.skillbar-bar {
    -webkit-border-radius: 10px;
    -moz-border-radius: 10px;
    border-radius: 10px;
}
```

## Demo

For a demo, click [here](http://ryanfitzgerald.github.io/skillbars/)

## License

MIT License (see LICENSE.md)
