# Ease methods<br>Ease Templates Reference

### Core methods
* [Ease_openGraph](#ease_opengraph)
* [Ease_header](#ease_header)
* [Ease_css](#ease_css)
* [Ease_javascript](#ease_javascript)
* [Ease_javascriptInline](#ease_javascriptinline)
* [Ease_masterpageContent](#ease_masterpagecontent)
* [Ease_searchbox](#ease_searchbox)
* [Ease_menu](#ease_menu)
* [Ease_pagemenuElements](#ease_pagemenuelements)
* [Ease_loginButton](#ease_loginbutton)
* [Ease_content](#ease_content)

### Module methods
Adgroups
 * [Ease_adgroup](#ease_adgroup)

Calendars
 * [Ease_calendar](#ease_calendar)
 * [Ease_calendaritem](#ease_calendaritem)

Menulists
 * [Ease_menulist](#ease_menulist)

Newsgroups
 * [Ease_newsgroup](#ease_newsgroup)
 * [Ease_newsarticle](#ease_newsarticle)

Products
 * [Ease_products_filtergroup](#ease_products_filtergroup)
 * [Ease_products_activeFilters](#ease_products_activefilters)
 * [Ease_products](#ease_products)
 * [Ease_product](#ease_product)

Simpleitems
 * [Ease_simpleitem](#ease_simpleitem)

Slideshows
 * [Ease_slideshow](#ease_slideshow)


# Core methods

### Ease_openGraph

### Ease_header

### Ease_css

### Ease_javascript

### Ease_javascriptInline

### Ease_masterpageContent

### Ease_searchbox

### Ease_menu

### Ease_pagemenuElements

### Ease_loginButton

### Ease_content


# Module methods


## Adgroups

### Ease_adgroup


## Calendars

### Ease_calendar

### Ease_calendaritem


## Menulists

### Ease_menulist


## Newsgroups

### Ease_newsgroup

### Ease_newsarticle


## Products

### Ease_products_filtergroup

### Ease_products_activeFilters

### Ease_products

### Ease_product


## Simpleitems

### Ease_simpleitem


## Slideshows

### Ease_slideshow

```twig
{% Ease_slideshow(int slideshowId = 1) %}
```

The method `Ease_slideshow` generates an Ease slideshow. 
The initial constructor method takes one argument, the id of the slideshow (this id is the same id which is used in the table in the database, and therefor must exist in the database beforehand). 
The default value of the parameter is **1**

#### Constructor arguments

Argument | Default value | Description
--- | --- | ---
slideshowId | 1 | The id of the slideshow

#### Parameters

Parameter | Default value | Action name | Description
--- | --- | --- | ---
slideshowId | 1 | setSlideshowId | Set the id of the slideshow
width | none | setWidth | Set the width of the slideshow
height | none | setHeight | Set the height of the slideshow
template | 'globalitems/slideshow' | setTemplate | Set the template file to use for the slideshow
padding | 0 | setPadding | Set the padding of the ease overlay on the slideshow
ignorePadding | false |  setIgnorePadding | Set the ease overlay to ignore the padding of the element
buttonPosition | 'outside' | setButtonPosition | Set the button position of the ease overlay on the slideshow

#### Examples

```twig
Ease_slideshow(2)|setWidth(800)|setHeight(300)
{# Generates a slideshow from the Id 2, and sets the size of the slides to be 800x300  #}
```
