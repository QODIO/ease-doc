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

#### Description

```twig
{% Ease_slideshow(int slideshowId = 1) %}
```

The method `Ease_slideshow` generates an Ease slideshow. 
The initial constructor method takes one parameter, the id of the slideshow (this `Id` is the same `Id` which is used in the table in the database, and therefor must exist in the database beforehand). 
The default value of the parameter is `1`

#### Parameters

Parameter | Default value | Description
slideshowId | 1 | The id of the slideshow

#### Settings

Method name | Parameters | Description
--- | --- | ---
setSlideshowId | | Set the Id of the slideshow
setWidth | | 
setHeight | | 
setTemplate | | 
setPadding | | 
setIgnorePadding | | 
setButtonPosition | | 

#### Examples

Ease_slideshow(2)|setWidth(200)

