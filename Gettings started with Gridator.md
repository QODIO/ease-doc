# Gettings started with Gridator

* [The Core](#the-core)
* [The Elements](#the-elements)
* [The Utilities](#the-utilities)
* [The Functions](#the-functions)
* [The Media Queries](#the-media-queries)

&nbsp;
&nbsp;
## The Core

### Grid
Create powerful multi-device layouts quickly and easily with the default 12-column, nest-able Gridator grid. If you're familiar with grid systems, you'll feel right at home. If not, you'll learn quickly.<br>
See an [example](Gridator%20Kitchen%20Sink.md#grid).


&nbsp;
### Block Grid
Block grids give you a way to evenly split contents of a list within the grid. If you wanted to create a row of five images or paragraphs that need to stay evenly spaced no matter the screen size, the block grid is for you.<br>
See an [example](Gridator%20Kitchen%20Sink.md#block-grid).


&nbsp;
&nbsp;
## The Elements

### Buttons
Clicking on stuff is awesome, so hook up your users with buttons to do stuff. There are some lightweight button styles for size, presentation, and color to make customizing your own button as easy as adding a class. There are also [button groups](Gridator%20Kitchen%20Sink.md#button-groups), [dropdown buttons](Gridator%20Kitchen%20Sink.md#dropdown-buttons), and [spilt buttons](Gridator%20Kitchen%20Sink.md#split-buttons).<br>
See an [example](Gridator%20Kitchen%20Sink.md#buttons-and-busy-buttons).

### Alert Boxes
Alerts are handy elements you can drop into a form or inline on a page to communicate success, warnings, failure or just information. They'll conform to 100% of the container width you put them in.<br>
See an [example](Gridator%20Kitchen%20Sink.md#alert-boxes).

### Breadcrumbs
Breadcrumbs come in handy to show a navigation trail for users clicking through a site or app. They'll fill out 100% of the width of their parent container.<br>
See an [example](Gridator%20Kitchen%20Sink.md#breadcrumbs).

### Forms
Creating a form in Foundation is designed to be easy but extremely flexible. Forms are built with a combination of standard form elements, as well as the Grid (rows and columns).<br>
See an [example](Gridator%20Kitchen%20Sink.md#forms).

### Video
Flex Video lets browsers automatically scale video objects in your webpages. If you're embedding a video from YouTube, Vimeo, or another site that uses iframe, embed or object elements, you can wrap your video in div.video to create an intrinsic ratio that will properly scale your video on any device.<br>
See an [example](Gridator%20Kitchen%20Sink.md#video).

### Inline Lists
This simple construct creates a horizontal list of links, like in a footer. Use it when you want more control than spaces between links.<br>
See an [example](Gridator%20Kitchen%20Sink.md#inline-lists).

### Keystroke
If you have keyboard affordances, you might need to explain them to users. For example, to quit your browser hit `Cmd` + `Q`. (Don't actually type that now - there are more docs to read.) Keystroke is Gridator's simple character affordance tool.<br>
See an [example](Gridator%20Kitchen%20Sink.md#keystroke).

### Pagination
Pagination is a type of navigation that lets users tap through a series of related pages. Moving between pages has become less common with the advent of longer pages and AJAX loading, but if you need pagination, Gridator has you covered.<br>
See an [example](Gridator%20Kitchen%20Sink.md#pagination).

### Panels
A panel is a simple, helpful Foundation component that enables you to outline sections of your page easily. This allows you to view your page sections as you add content to them, or add emphasis to a section. The width is controlled by the grid columns you put them inside.<br>
See an [example](Gridator%20Kitchen%20Sink.md#panels).

### Progressbars
A simple way to add progressbars to your layouts. You only need two HTML elements to make them and they're easy to customize.<br>
See an [example](Gridator%20Kitchen%20Sink.md#progressbars).

### Type
Typography in Gridator is meant to make your life easier by providing clean, attractive, simple default styles for all of the most basic typographical elements.<br>
See an [example](Gridator%20Kitchen%20Sink.md#type).

### Blockquotes
Sometimes other people say smart things, and you may want to mention that through a blockquote callout. We've got you covered.<br>
See an [example](Gridator%20Kitchen%20Sink.md#blockquote).

&nbsp;
&nbsp;
## The Utilities

### Float Classes
You can change the float behavior of an element by adding `.pull-left` or `.pull-right` to an HTML element. To clear floats, add the class `.clearfix` to the parent element.<br>
The floats classes also have responsive equivilants. E.g. `.small-pull-right` or `.large-pull-right`.

### Radius and Rounded Classes
The `.radius` and `.round` classes allow you to easily apply a border-radius to a UI-element. Adding the class to a button group will apply the border radius only to the outside corners.

### Text Align Classes
You can change the text alignment of an element by adding `.text-left`, `.text-right`, `.text-center` or `.text-justify` to an element.
The alignment classes also have responsive equivilants. E.g. `.small-text-right` or `.large-text-right`.

### Visibility Classes
You can add the class `.hide` to an element to hide it. This will add the property *display: none;* to the element.
You can also control the visibility of elements responsively with the following classes:

Class | Description
--- | ---
`.landscape-only` | Will only show the element when landscape mode is detected
`.portrait-only` | Will only show the element when portrait mode is detected
`.small-only` | Will only show the element on small screens
`.small-up` | Will show the element on small and larger screens
`.medium-only` | Will only show the element on medium size screens
`.medium-up` | Will show the element on medium and larger screens
`.medium-down` | Will show the element on medium and smaller screens
`.large-only` | Will only show the element on large size screens
`.large-up` | Will show the element on large and larger screens
`.large-down` | Will show the element on large and smaller screens
`.xlarge-only` | Will only show the element on xlarge size screens
`.xlarge-up` | Will show the element on xlarge and larger screens
`.xlarge-down` | Will show the element on xlarge and smaller screens
`.xxlarge-only` | Will only show the element on xxlarge size screens
`.xxlarge-up` | Will show the element on xxlarge and larger screens
`.xxlarge-down` | Will show the element on xxlarge and smaller screens

For good measure, you also have the ability to hide elementsbased on the size of the screen

Class | Description
--- | ---
`.landscape-hide` | Will only hide the element when landscape mode is detected
`.portrait-hide` | Will only hide the element when portrait mode is detected
`.small-only-hide` | Will only hide the element on small screens
`.small-up-hide` | Will hide the element on small and larger screens
`.medium-only-hide` | Will only hide the element on medium size screens
`.medium-up-hide` | Will hide the element on medium and larger screens
`.medium-down-hide` | Will hide the element on medium and smaller screens
`.large-only-hide` | Will only hide the element on large size screens
`.large-up-hide` | Will hide the element on large and larger screens
`.large-down-hide` | Will hide the element on large and smaller screens
`.xlarge-only-hide` | Will only hide the element on xlarge size screens
`.xlarge-up-hide` | Will hide the element on xlarge and larger screens
`.xlarge-down-hide` | Will hide the element on xlarge and smaller screens
`.xxlarge-only-hide` | Will only hide the element on xxlarge size screens
`.xxlarge-up-hide` | Will hide the element on xxlarge and larger screens
`.xxlarge-down-hide` | Will hide the element on xxlarge and smaller screens


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
background-color blend_colors(#f00, 50%, #00f)
/* Returns: background-color: #800080; */
```

&nbsp;
### clearfix
Returns clearfix to the class
##### Example:
```stylus
.awesome_div
  background-color #000
  clearfix()
```

&nbsp;
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

&nbsp;
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

&nbsp;
### overflow
Adds ellipsis support for overflow
##### Example:
```stylus
overflow ellipsis
```
Is the same as writing:
```css
white-space: nowrap;
overflow: hidden;
text-overflow: ellipsis;
```

&nbsp;
### fixed
Shorthand for setting up a fixed element
```stylus
fixed left 10px top 5px
```
Is the same as writing:
```css
position: fixed;
left: 10px
top: 5px;
```

&nbsp;
### absolute
Shorthand for setting up a absolute element
```stylus
absolute left 10px top 5px
```
Is the same as writing:
```css
position: absolute;
left: 10px
top: 5px;
```

&nbsp;
### relative
Shorthand for setting up a relative element
```stylus
relative left 10px top 5px
```
Is the same as writing:
```css
position: relative;
left: 10px
top: 5px;
```

&nbsp;
### size
Set the size of an element. If only first parameter is given, then both width and height will be set to that.
##### Definition:
```stylus
size width [height]
```
##### Example:
```stylus
size 300px 200px
```
Is the same as writing:
```css
width: 300px
height: 200px;
```

&nbsp;
### border
Extends the functionality of border to have some default values if not expressed. E.g.:
```stylus
border red
border 5px blue
```
Is the same as writing:
```css
border: 1px solid red;
border: 5px solid blue;
```


&nbsp;
&nbsp;
## The Media Queries

##### Theese are the ranges the media queries use:
* small-range-lower 	= 0px
* small-range-upper 	= 640px
* medium-range-lower 	= 641px
* medium-range-upper 	= 1024px
* large-range-lower 	= 1025px
* large-range-upper 	= 1440px
* xlarge-range-lower 	= 1441px
* xlarge-range-upper 	= 1920px
* xxlarge-range-lower = 1921px

##### These are the available media sizes you can use
Query variable | CSS equivelant
--- | ---
`$screen` | "only screen"
`$landscape` | "only screen and (orientation: landscape)"
`$portrait` | "only screen and (orientation: portrait)"
`$small-up` | "only screen"
`$small-down` | "only screen and (max-width: 640px)"
`$small-only` | "only screen and (max-width: 640px)"
`$medium-up` | "only screen and (min-width: 641px)"
`$medium-down` | "only screen and (max-width: 1024px)"
`$medium-only` | "only screen and (min-width: 641px) and (max-width: 1024px)"
`$large-up` | "only screen and (min-width: 1025px)"
`$large-down` | "only screen and (max-width: 1440px)"
`$large-only` | "only screen and (min-width: 1025px) and (max-width: 1440px)"
`$xlarge-up` | "only screen and (min-width: 1441px)"
`$xlarge-down` | "only screen and (max-width: 1920px)"
`$xlarge-only` | "only screen and (min-width: 1441px) and (max-width: 1920px)"
`$xxlarge-up` | "only screen and (min-width: 1921px)"
`$xxlarge-down` | "only screen"
`$xxlarge-only` | "only screen and (min-width: 1921px)"

##### Examples:
if you want to the included classes to only be used at specefik size:
```stylus
@media $large-down
  .header
    background-color red
```
or if you want to do it inside a class (helpful for the flow of the style):
```stylus
.header
  @media $large-down
    background-color red
```
