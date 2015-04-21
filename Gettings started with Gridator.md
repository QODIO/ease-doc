# Gettings started with Gridator

* [The Core](#the-core)
* [The Elements](#the-elements)
* [The Utilities](#the-utilities)
* [The Functions](#the-functions)

&nbsp;
&nbsp;
## The Core

### Grid
Create powerful multi-device layouts quickly and easily with the default 12-column, nest-able Gridator grid. If you're familiar with grid systems, you'll feel right at home. If not, you'll learn quickly.

![Image of Grid](https://github.com/ingipingi/Work/blob/master/images/grid.png)


### Block Grid
Block grids give you a way to evenly split contents of a list within the grid. If you wanted to create a row of five images or paragraphs that need to stay evenly spaced no matter the screen size, the block grid is for you.


&nbsp;
&nbsp;
## The Elements

### Buttons
Clicking on stuff is awesome, so hook up your users with buttons to do stuff. There are some lightweight button styles for size, presentation, and color to make customizing your own button as easy as adding a class. There are also button groups, dropdown buttons, and spilt buttons.

### Alert Boxes
Alerts are handy elements you can drop into a form or inline on a page to communicate success, warnings, failure or just information. They'll conform to 100% of the container width you put them in.

### Breadcrumbs
Breadcrumbs come in handy to show a navigation trail for users clicking through a site or app. They'll fill out 100% of the width of their parent container.

### Forms
Creating a form in Foundation is designed to be easy but extremely flexible. Forms are built with a combination of standard form elements, as well as the Grid (rows and columns).

### Video
Flex Video lets browsers automatically scale video objects in your webpages. If you're embedding a video from YouTube, Vimeo, or another site that uses iframe, embed or object elements, you can wrap your video in div.video to create an intrinsic ratio that will properly scale your video on any device.

### Inline Lists
This simple construct creates a horizontal list of links, like in a footer. Use it when you want more control than spaces between links.

### Keystroke
If you have keyboard affordances, you might need to explain them to users. For example, to quit your browser hit `Cmd` + `Q`. (Don't actually type that now - there are more docs to read.) Keystroke is Gridator's simple character affordance tool.

### Pagination
Pagination is a type of navigation that lets users tap through a series of related pages. Moving between pages has become less common with the advent of longer pages and AJAX loading, but if you need pagination, Gridator has you covered.

### Panels
A panel is a simple, helpful Foundation component that enables you to outline sections of your page easily. This allows you to view your page sections as you add content to them, or add emphasis to a section. The width is controlled by the grid columns you put them inside.

### Progress Bars
A simple way to add progress bars to your layouts. You only need two HTML elements to make them and they're easy to customize.

### Tables
They're not the best looking things ever, but tables get the job done (for tabular data, of course).

### Type
Typography in Gridator is meant to make your life easier by providing clean, attractive, simple default styles for all of the most basic typographical elements.

### Blockquotes
Sometimes other people say smart things, and you may want to mention that through a blockquote callout. We've got you covered.

&nbsp;
&nbsp;
## The Utilities

### Float Classes

### Radius and Rounded Classes

### Text Align Classes

### Visibility Classes

### 

### 


&nbsp;
&nbsp;
## The Functions

### blend_colors
Used to blend two colors together
##### Definition:
```stylus
blend_colors(source_color, percent = 50%, blend_width = #ccc)
```
##### Example:
```stylus
blend_colors(#f00, 50%, #00f)
/* Should return approx. #808 */
```

### clearfix
Returns clearfix to the class

### is_dark
Check if a color is dark by passing a color as the first argument, return second argument if true, third argument if not.
##### Definition:
```stylus
is_dark(color, then_color = #fff, else_color = #000)
```
##### Example:
```stylus
is_dark(#333, #f00, #00f)
/* Returns #f00 */
```

### is_light
Check if a color is light by passing a color as the first argument, return second argument if true, third argument if not.
##### Definition:
```stylus
is_light(color, then_color = #fff, else_color = #000)
```
##### Example:
```stylus
is_light(#333, #f00, #00f)
/* Returns #00f */
```

### overflow
Adds ellipsis support for overflow

### fixed
Shorthand for setting up a fixed element
```stylus
fixed('left 10px top 5px')
```
Is the same as writing:
```css
position: fixed;
left: 10px
top: 5px;
```

### absolute
Shorthand for setting up a absolute element
```stylus
absolute('left 10px top 5px')
```
Is the same as writing:
```css
position: absolute;
left: 10px
top: 5px;
```

### relative
Shorthand for setting up a relative element
```stylus
relative('left 10px top 5px')
```
Is the same as writing:
```css
position: relative;
left: 10px
top: 5px;
```

### size
Set the size of an element. If only first parameter is given, then both width and height will be set to that.
##### Definition:
```stylus
size(width[, height])
```
##### Example:
```stylus
size(300px, 200px)
```
Is the same as writing:
```css
width: 300px
height: 200px;
```

### border
Adds the ability to omit border style when setting border. E.g.:
```stylus
border 3px #f00
```
Is the same as writing:
```css
border: 3px solid #f00;
```
