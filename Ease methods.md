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
```twig
{% Ease_openGraph(int adgroupId) %}
```


&nbsp;
### Ease_header
```twig
{% Ease_header(int adgroupId) %}
```


&nbsp;
### Ease_css
```twig
{% Ease_css %}
```
The method `Ease_css`, returns all css link tags Ease uses. It's a helpful method to make sure all needed css files get included.


&nbsp;
### Ease_javascript
```twig
{% Ease_javascript(int adgroupId) %}
```
The method `Ease_javascript`, returns all javascript link tags Ease uses. It's a helpful method to make sure all needed javascript files get included.


&nbsp;
### Ease_javascriptInline
```twig
{% Ease_javascriptInline(int adgroupId) %}
```


&nbsp;
### Ease_masterpageContent
```twig
{% Ease_masterpageContent(int adgroupId) %}
```

&nbsp;
### Ease_searchbox
```twig
{% Ease_searchbox(int adgroupId) %}
```


&nbsp;
### Ease_menu
```twig
{% Ease_menu(int adgroupId) %}
```


&nbsp;
### Ease_pagemenuElements
```twig
{% Ease_pagemenuElements(int adgroupId) %}
```


&nbsp;
### Ease_loginButton
```twig
{% Ease_loginButton(int adgroupId) %}
```


&nbsp;
### Ease_content
```twig
{% Ease_content(int adgroupId) %}
```


&nbsp;
&nbsp;
# Module methods


&nbsp;
## Adgroups
### Ease_adgroup
```twig
{% Ease_adgroup(int adgroupId) %}
```
The method `Ease_adgroup` generates an Ease adgroup.<br>
The initial constructor method takes one argument, the id of the adgroup (this id is the same id which is used in the table in the database, and therefor must exist in the database beforehand).

#### Constructor arguments
Argument | Default value | Description
--- | --- | ---
adgroupId | 1 | The id of the adgroup

#### Parameters
Parameter | Default value | Action name | Description
--- | --- | --- | ---
adgroupId | 1 | `setSlideshowId` | Set the id of the adgroup
width | 300 | `setWidth` | Set the width of the adgroup
height | 250 | `setHeight` | Set the height of the adgroup
quantity | 1 | `setHeight` | Set the number of ads to show
--- | --- | --- | ---
template | 'globalitems/adgroup' | `setTemplate` | Set the template file to use for the adgroup
padding | 4 | `setPadding` | Set the padding of the ease overlay on the adgroup
ignorePadding | false | `setIgnorePadding` | Set the ease overlay to ignore the padding of the element
buttonPosition | 'outside' | `setButtonPosition` | Set the button position of the ease overlay on the adgroup

#### Examples
```twig
Ease_adgroup(2)|setWidth(800)|setHeight(300)
{# Generates a adgroup with the `Id` 2, and sets the size of the slides to be 800x300  #}

Ease_adgroup(2)|setTemplate('some_folder/adgroup')
{# Generates a adgroup with the `Id` 1, and sets the template to use something other than default (the extension .ease is optional)  #}
```


&nbsp;
## Calendars
### Ease_calendar
```twig
{% Ease_calendar(int calendarId) %}
```
The method `Ease_calendar` generates a list of Ease calander events.<br>
The initial constructor method takes one argument, the id of the calendar.

#### Constructor arguments
Argument | Default value | Description
--- | --- | ---
calendarId | *none* | The id of the calendar.

#### Parameters
Parameter | Default value | Action name | Description
--- | --- | --- | ---
calendarId | *none* | `setCalendarId` | Set the id of the calendar.
excludeCalendarItemId | *none* | `setExcludeCalendarItemId` | Set the id of a calendar event to exclude (This is helpful if show a calendar on the same page as a calendar event, but don't want the calendar event to show up in the list).
offset | 0 | `setOffset` | Set the offset of the calendar. (E.g. if 10, then the first 10 calendar events will be skipped.)
limit | 20 | `setLimit` | Set the limit of the calendar events. (How many calendar events should be shown initially).
imageWidth | 200 | `setImageWidth` | Set the width of the images of the calendar events.
imageHeight | 150 | `setImageHeight` | Set the height of the images of the calendar events.
disableGroupEdit | false | `setDisableGroupEdit` | If true, then Ease overlays for the calendar is disabled 
disableItemEdit | false | `setDisableItemEdit` | If true, then Ease overlays for the calendar events are disabled 
--- | --- | --- | ---
template | 'globalitems/calendar' | `setTemplate` | Set the template file to use for the calendar
padding | 4 | `setPadding` | Set the padding of the ease overlay on the calendar
ignorePadding | false | `setIgnorePadding` | Set the ease overlay to ignore the padding of the elements

#### Examples
```twig
Ease_calendar(1)
{# Generates a calendar of all items  #}

Ease_calendar(2)|setTemplate('some_folder/calendar')
{# Generates a calendar, with the id 2, and sets the template to use something other than default (the extension .ease is optional) #}

Ease_calendar(2)|setLimit(40)
{# Generates a calendar, with the id 2, and sets the limit to 40, so 40 events will be shown #}
```


&nbsp;
### Ease_calendaritem
```twig
{% Ease_calendaritem(int calendarItemId) %}
```
The method `Ease_calendaritem` generates a Ease calendar event.<br>
The initial constructor method takes one argument, the id of the calendar event.<br>

#### Constructor arguments
Argument | Default value | Description
--- | --- | ---
calendarItemId | 1 | The id of the calendar event

#### Parameters
Parameter | Default value | Action name | Description
--- | --- | --- | ---
calendarItemId | *none* | `setCalendarItemId` | Set the id of the calendar event
--- | --- | --- | ---
template | 'globalitems/calendaritem' | `setTemplate` | Set the template file to use for the calendar event
padding | 0 | `setPadding` | Set the padding of the ease overlay on the calendar event
ignorePadding | false | `setIgnorePadding` | Set the ease overlay to ignore the padding of the element
buttonPosition | 'outside' | `setButtonPosition` | Set the button position of the ease overlay on the calendar event

#### Examples
```twig
Ease_calendaritem(1)
{# Generates a calendar event with the `Id` 1, and sets the size of the slides to be 800x300  #}

Ease_calendaritem(2)|setTemplate('some_folder/calendaritem')
{# Generates a calendar event with the `Id` 2, and sets the template to use something other than default (the extension .ease is optional) #}
```


&nbsp;
## Menulists
### Ease_menulist
```twig
{% Ease_menulist(int menuId) %}
```
The method `Ease_menulist` generates a list of menu items. (Mostly used in global content areas).<br>
The initial constructor method takes one argument, the id of the menu.

#### Constructor arguments
Argument | Default value | Description
--- | --- | ---
menuId | *none* | The id of the menu.

#### Parameters
Parameter | Default value | Action name | Description
--- | --- | --- | ---
menuId | *none* | `setMenuId` | Set the id of the menu.
excludeMenuitemId | *none* | `setExcludeMenuitemId` | Set the id of a menuitem to exclude (This is helpful if show a menu list on the same page as a menu item, but don't want the menu item to show up in the menu list).
offset | 0 | `setOffset` | Set the offset of the menu list. (E.g. if 10, then the first 10 menu items will be skipped.)
limit | 20 | `setLimit` | Set the limit of the menu list. (How many menu should be shown initially).
imageWidth | 300 | `setImageWidth` | Set the width of the image of the menu items.
imageHeight | 150 | `setImageHeight` | Set the height of the image of the menu items.
--- | --- | --- | ---
template | 'globalitems/menulist' | `setTemplate` | Set the template file to use for the menu list
padding | 4 | `setPadding` | Set the padding of the ease overlay on the menu list
ignorePadding | false | `setIgnorePadding` | Set the ease overlay to ignore the padding of the elements
buttonPosition | 'inside' | `setButtonPosition` | Set the button position of the ease overlay on the menu list

#### Examples
```twig
Ease_menulist(1)
{# Generates a menu list, where the menu with id 1 #}

Ease_menulist(2)|setTemplate('some_folder/newsgroup')
{# Generates a menu list, with menu id 2, and sets the template to use something other than default (the extension .ease is optional) #}

Ease_menulist(2)|setLimit(40)
{# Generates a menu list, with menu id 2, and sets the limit to 40, so 40 menu items will be shown #}
```


&nbsp;
## Newsgroups
### Ease_newsgroup
```twig
{% Ease_newsgroup(int newsgroupId) %}
```
The method `Ease_newsgroup` generates a list of Ease newsarticles (newsgroup).<br>
The initial constructor method takes one argument, the id of the newsgroup.

#### Constructor arguments
Argument | Default value | Description
--- | --- | ---
newsgroupId | *none* | The id of the newsgroup.

#### Parameters
Parameter | Default value | Action name | Description
--- | --- | --- | ---
newsgroupId | *none* | `setNewsgroupId` | Set the id of the newsgroup.
excludeNewsArticleId | *none* | `setExcludeNewsArticleId` | Set the id of a product to exclude (This is helpful if show a product list on the same page as a single product, but don't want the single product to show up in the list).
offset | 0 | `setOffset` | Set the offset of the newsarticles list. (E.g. if 10, then the first 10 newsarticles will be skipped.)
limit | 20 | `setLimit` | Set the limit of the newsarticles list. (How many newsarticles should be shown initially).
interval | 20 | `setInterval` | Set the interval of the newsarticles list more function. (This controls how many new newsarticles will be added to the list every time a user presses the more newsarticles button)
imageWidth | 200 | `setImageWidth` | Set the width of the image of the newsarticles.
imageHeight | 150 | `setImageHeight` | Set the height of the image of the newsarticles.
truncateLength | 250 | `setImageHeight` | Set the truncatelength of the article description text.
disableGroupEdit | false | `setDisableGroupEdit` | If true, then Ease overlays for the newsgroup is disabled 
disableItemEdit | `false | setDisableItemEdit` | If true, then Ease overlays for the newsarticles are disabled 
--- | --- | --- | ---
template | 'globalitems/newsgroup' | `setTemplate` | Set the template file to use for the newsarticles list
padding | 4 | `setPadding` | Set the padding of the ease overlay on the newsarticles list
ignorePadding | false | `setIgnorePadding` | Set the ease overlay to ignore the padding of the elements

#### Examples
```twig
Ease_newsgroup
{# Generates a newsarticles list of all items  #}

Ease_newsgroup('2,10')|setTemplate('some_folder/newsgroup')
{# Generates a newsarticles list, where the newsarticles have the filter 2 or 10, and sets the template to use something other than default (the extension .ease is optional) #}

Ease_newsgroup('2')|setLimit(40)
{# Generates a newsarticles list, where the newsarticles have the filter 2, and sets the limit to 40, so 40 newsarticles will be shown #}
```


&nbsp;
### Ease_newsarticle
```twig
{% Ease_newsarticle(int newsArticleId) %}
```
The method `Ease_newsarticle` generates a single Ease newsarticle.<br>
The initial constructor method takes one argument, the id of the newsarticle.<br>

#### Constructor arguments
Argument | Default value | Description
--- | --- | ---
newsArticleId | 1 | The id of the newsarticle

#### Parameters
Parameter | Default value | Action name | Description
--- | --- | --- | ---
newsArticleId | *none* | `setNewsArticleId` | Set the id of the newsarticle
--- | --- | --- | ---
template | 'globalitems/newsarticle' | `setTemplate` | Set the template file to use for the newsarticle
padding | 0 | `setPadding` | Set the padding of the ease overlay on the newsarticle
ignorePadding | false | `setIgnorePadding` | Set the ease overlay to ignore the padding of the element
buttonPosition | 'outside' | `setButtonPosition` | Set the button position of the ease overlay on the newsarticle

#### Examples
```twig
Ease_newsarticle(1)
{# Generates a newsarticle with the `Id` 1  #}

Ease_newsarticle(2)|setTemplate('some_folder/newsarticle')
{# Generates a newsarticle with the `Id` 2, and sets the template to use something other than default (the extension .ease is optional) #}
```


&nbsp;
## Products
### Ease_products_filtergroup
```twig
{% Ease_products_filtergroup(int productFiltergroupId) %}
```
The method `Ease_products_filtergroup` generates an Ease product filtergroup hierarchical list.<br>
The initial constructor method takes one argument, the id of the filtergroup (this id is the same id which is used in the table in the database, and therefor must exist in the database beforehand).<br>

#### Constructor arguments
Argument | Default value | Description
--- | --- | ---
productFiltergroupId | 1 | The id of the filtergroup

#### Parameters
Parameter | Default value | Action name | Description
--- | --- | --- | ---
productFiltergroupId | 1 | `setProductFiltergroupId` | Set the id of the filtergroup
productFilterId | *none* | `setProductFilterId` | Optionally set the id of the active filter (not really used)
startDepth | 1 | `setStartDepth` | Set the menu start depth of the filtergroup.
endDepth | *none* | `setEndDepth` | Set the menu end depth of the filtergroup.
class | *none* | `setClass` | Add a class to the generated filtergroup element
hideAdd | false | `hideAdd` | Hide/disable the Ease add filter button.
imageWidth | 64 | `setImageWidth` | Set the width of the image of the filtergroup.
imageHeight | 64 | `setImageHeight` | Set the height of the image of the filtergroup.
featuredOnly | false | `setFeaturedOnly` | Set the filtergroup only to show featured filters.
accumulateFilters | false | `setAccumulateFilters` | Set the filtergroup links to be accumulative (if true, then whenever a filter is chosen it will be added to the currently chosen filters).
--- | --- | --- | ---
padding | 0 | `setPadding` | Set the padding of the ease overlay on the filtergroup
ignorePadding | false | `setIgnorePadding` | Set the ease overlay to ignore the padding of the element
buttonPosition | 'outside' | `setButtonPosition` | Set the button position of the ease overlay on the filtergroup

#### Examples
```twig
Ease_products_filtergroup(1)
{# Generates a filtergroup with the `Id` 1  #}

Ease_products_filtergroup(2)|setAccumulateFilters(true)
{# Generates a filtergroup with the `Id` 2, and sets the chosen filters to be accumulative  #}
```


&nbsp;
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


&nbsp;
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
{# Generates a products list, where the products have the filter 2 or 10, and sets the template to use something other than default (the extension .ease is optional) #}

Ease_products('2')|setLimit(40)
{# Generates a products list, where the products have the filter 2, and sets the limit to 40, so 40 products will be shown #}
```


&nbsp;
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
Ease_product(1)
{# Generates a product with the `Id` 1, and sets the size of the slides to be 800x300  #}

Ease_product(2)|setTemplate('some_folder/product')
{# Generates a product with the `Id` 2, and sets the template to use something other than default (the extension .ease is optional) #}
```


&nbsp;
## Simpleitems
### Ease_simpleitem
```twig
{% Ease_simpleitem(int simpleitemId) %}
```
The method `Ease_simpleitem` generates an Ease simple item.<br>
A simpleitem can be a text, richtext or an image (IMAGE NOT YET SUPPORTED). The type of the simple item is controlled from the database. E.g. text, richtext or image.<br>
The initial constructor method takes one argument, the id of the simple item (this id is the same id which is used in the table in the database, and therefor must exist in the database beforehand).<br>

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
{# Generates a slideshow with the `Id` 1, and sets the template to use something other than default  #}
```
