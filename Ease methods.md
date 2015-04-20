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


&nbsp;

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


&nbsp;

&nbsp;

# Module methods


&nbsp;

## Adgroups

### Ease_adgroup


&nbsp;

## Calendars

### Ease_calendar

### Ease_calendaritem


&nbsp;

## Menulists

### Ease_menulist


&nbsp;

## Newsgroups

### Ease_newsgroup

### Ease_newsarticle


&nbsp;

## Products

### Ease_products_filtergroup

### Ease_products_activeFilters

```twig
{% Ease_products_activeFilters(string productFilterIds) %}
```

The method `Ease_products_activeFilters` generates a list of currently active product filters.<br>
The initial constructor method takes one argument, a comma seperated list of active filter ids.

#### Constructor arguments

Argument | Default value | Description
--- | --- | ---
productFilterIds | *none* | A comma seperated list of active filter ids.

#### Parameters

Parameter | Default value | Action name | Description
--- | --- | --- | ---
productFilterIds | *none* | `setProductFilterIds` | Set the comma seperated list of active filter ids.
ancestorDelimiter | ' > ' | `setAncestorDelimiter` | Set the delimiter to show between the ancestors of the filters.
--- | --- | --- | ---
template | 'globalitems/products_active_filters' | `setTemplate` | Set the template file to use for the active filters list

#### Examples

```twig
Ease_products_activeFilters('2,10,11')
{# Generates a filters list of the filters 2, 10 and 11 #}

Ease_products_activeFilters('2,10,11')|setAncestorDelimiter(' : ')
{# Generates a filters list of the filters 2, 10 and 11, and sets the ancestor delimiter to ' : ' #}
```


### Ease_products

```twig
{% Ease_products(string productFilterIds) %}
```

The method `Ease_products` generates a list of Ease products.<br>
The initial constructor method takes one argument, a comma seperated list of filter ids.<br>

#### Constructor arguments

Argument | Default value | Description
--- | --- | ---
productFilterIds | *none* | A comma seperated list of filter ids, that products have.

#### Parameters

Parameter | Default value | Action name | Description
--- | --- | --- | ---
productFilterIds | *none* | `setProductFilterIds` | Set the comma seperated list of filter ids, that products should have.
excludeProductId | *none* | `setExcludeProductId` | Set the id of a product to exclude (This is helpful if show a product list on the same page as a single product, but don't want the single product to show up in the list).
offset | 0 | `setOffset` | Set the offset of the products list. (E.g. if 10, then the first 10 products will be skipped.)
limit | 20 | `setLimit` | Set the limit of the products list. (How many products should be shown initially).
interval | 20 | `setInterval` | Set the interval of the products list more function. (This controls how many new products will be added to the list every time a user presses the more products button)
orderBy | 'title_asc' | `setOrderBy` | Set the order of the products in the list. Accepted values are: `title_asc`, `title_desc`, `price_asc`, `price_desc`, `created_asc`, `created_desc`, `hits_asc`, `hits_desc`.
--- | --- | --- | ---
template | 'globalitems/products' | `setTemplate` | Set the template file to use for the products list
padding | 4 | `setPadding` | Set the padding of the ease overlay on the products list
ignorePadding | false | `setIgnorePadding` | Set the ease overlay to ignore the padding of the elements

#### Examples

```twig
Ease_products
{# Generates a products list of all items  #}

Ease_products('2,10')|setTemplate('some_folder/products')
{# Generates a products list, where the products have the filter 2 or 10, and sets the template to use to something other than default (the extension .ease is optional) #}

Ease_products('2')|setLimit(40)
{# Generates a products list, where the products have the filter 2, and sets the limit to 40, so 40 products will be shown #}
```


### Ease_product

```twig
{% Ease_product(int productId) %}
```

The method `Ease_product` generates a single Ease product.<br>
The initial constructor method takes one argument, the id of the product.<br>

#### Constructor arguments

Argument | Default value | Description
--- | --- | ---
productId | 1 | The id of the product

#### Parameters

Parameter | Default value | Action name | Description
--- | --- | --- | ---
productId | *none* | `setSlideshowId` | Set the id of the product
--- | --- | --- | ---
template | 'globalitems/product' | `setTemplate` | Set the template file to use for the product
padding | 0 | `setPadding` | Set the padding of the ease overlay on the product
ignorePadding | false | `setIgnorePadding` | Set the ease overlay to ignore the padding of the element
buttonPosition | 'outside' | `setButtonPosition` | Set the button position of the ease overlay on the product

#### Examples

```twig
Ease_product(2)
{# Generates a product with the `Id` 1, and sets the size of the slides to be 800x300  #}

Ease_product(2)|setTemplate('some_folder/product')
{# Generates a product with the `Id` 2, and sets the template to use to something other than default (the extension .ease is optional) #}

```


&nbsp;

## Simpleitems

### Ease_simpleitem

```twig
{% Ease_simpleitem(int simpleitemId) %}
```

The method `Ease_simpleitem` generates an Ease simple item.<br>
A simpleitem can be a text, richtext or an image (NOT YET SUPPORTED).<br>
The initial constructor method takes one argument, the id of the simple item (this id is the same id which is used in the table in the database, and therefor must exist in the database beforehand).<br>
The type of the simple item is also controlled from the database. E.g. text, richtext or image.

#### Constructor arguments

Argument | Default value | Description
--- | --- | ---
simpleitemId | *none* | The id of the simple item

#### Parameters

Parameter | Default value | Action name | Description
--- | --- | --- | ---
simpleitemId | *none* | `setSimpleitemId` | Set the id of the simple item
imageWidth | *none* | `setImageWidth` | Set the width of the simple item, if it is an image (NOT YET SUPPORTED)
imageHeight | *none* | `setImageHeight` | Set the height of the simple item, if it is an image (NOT YET SUPPORTED)
class | *none* | `setClass` | Add a class to the generated simple item element
--- | --- | --- | ---
template | 'globalitems/simpleitem' | `setTemplate` | Set the template file to use for the simple item
padding | 0 | `setPadding` | Set the padding of the ease overlay on the simple item
ignorePadding | false | `setIgnorePadding` | Set the ease overlay to ignore the padding of the element
buttonPosition | 'outside' | `setButtonPosition` | Set the button position of the ease overlay on the simple item

#### Examples

```twig
Ease_simpleitem(1)
{# Generates a simple item with the `Id` 1  #}

Ease_simpleitem(2)|setClass('some_class')
{# Generates a simple item with the `Id` 2, and adds a class to the generated simple item  #}

```


&nbsp;

## Slideshows

### Ease_slideshow

```twig
{% Ease_slideshow(int slideshowId = 1) %}
```

The method `Ease_slideshow` generates an Ease slideshow.<br>
The initial constructor method takes one argument, the id of the slideshow (this id is the same id which is used in the table in the database, and therefor must exist in the database beforehand).<br>
The default value of the parameter is **1**

#### Constructor arguments

Argument | Default value | Description
--- | --- | ---
slideshowId | 1 | The id of the slideshow

#### Parameters

Parameter | Default value | Action name | Description
--- | --- | --- | ---
slideshowId | 1 | `setSlideshowId` | Set the id of the slideshow
width | *none* | `setWidth` | Set the width of the slideshow
height | *none* | `setHeight` | Set the height of the slideshow
--- | --- | --- | ---
template | 'globalitems/slideshow' | `setTemplate` | Set the template file to use for the slideshow
padding | 0 | `setPadding` | Set the padding of the ease overlay on the slideshow
ignorePadding | false | `setIgnorePadding` | Set the ease overlay to ignore the padding of the element
buttonPosition | 'outside' | `setButtonPosition` | Set the button position of the ease overlay on the slideshow

#### Examples

```twig
Ease_slideshow(2)|setWidth(800)|setHeight(300)
{# Generates a slideshow with the `Id` 2, and sets the size of the slides to be 800x300  #}

Ease_slideshow|setTemplate('some_folder/slideshow.ease')
{# Generates a slideshow with the `Id` 1, and sets the template to use to something other than default  #}

```
