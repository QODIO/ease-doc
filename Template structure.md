# Ease Template Structure<br>Ease Templates Reference

### File and Folder Structure
* `[assets]`: This folder contains all the assets (css, javascript, images, fonts, etc.)
  * `[css]`: This folder contains all the css files of the template
    * `[gridator]`: This folder contains Gridator
    * `_all.html`: This is a "kitchen sink" file with most of the CSS elements in Gridator (for testing purposes)
    * `_grid.html`: This is a testing file for the grid elements in Gridator (for testing purposes)
    * `fontface.css`: Normally used for fontfaces for embedded fonts
    * `gridator.styl`: Gridator's main .styl file, this file includes all other Gridator modules
      * `gridator.css`: A compiled stylus file (don't edit this file directly)
    * `stylesheet.styl`: The template's main .styl file, where every style for the template goes.
      * `stylesheet.css`: A compiled stylus file (don't edit this file directly)
    * `variables.styl`: This file is both used by gridator.styl and stylesheet.styl. It contains all the variables the stylesheets use.
  * `[fonts]`: Normally used for embedded fonts
  * `[images]`: Normally used for images
  * `[js]`: Normally used for javascript
* `[contentitems]`: This folder contains all the contentitem templates 
  * `album.ease`: Template file for the album contentitems
  * `albumcollection_album.ease`: Template file for the albumcollection contentitem (after you open a albumcollection)
  * `albumcollection_layout1.ease`: Template file for the albumcollection contentitem with layout 1 (Grid)
  * `albumcollection_layout1.ease`: Template file for the albumcollection contentitem with layout 1 (List)
  * `filescollection.ease`: Template file for the filescollection contentitem
  * `glossary.ease`: Template file for the glossary contentitem
  * `htmlitem.ease`: Template file for the htmlitem contentitem
  * `placescollection_layout1.ease`: Template file for the placescollection contentitem (Grid)
  * `placescollection_layout2.ease`: Template file for the placescollection contentitem (List)
  * `placescollection_place.ease`: Template file for the placescollectin contentitem (after you open a place)
  * `schedule.ease`: Template file for the schedule contentitem
  * `textitem_layout1.ease`: Template file for the textitem contentitem with layout 1
  * `textitem_layout2.ease`: Template file for the textitem contentitem with layout 2
  * `textitem_layout3.ease`: Template file for the textitem contentitem with layout 3
  * `textitem_layout4.ease`: Template file for the textitem contentitem with layout 4
  * `textitem_layout5.ease`: Template file for the textitem contentitem with layout 5
  * `textitem_layout6.ease`: Template file for the textitem contentitem with layout 6
  * `textitem_layout7.ease`: Template file for the textitem contentitem with layout 7
* `[globalitems]`: This folder contains all the globalitems templates
  * `adgroup.ease`: Template file for the adgroup globalitem
  * `calendar.ease`: Template file for the calendar globalitem
  * `calendaritem.ease`: Template file for the calendaritem globalitem
  * `menulist.ease`: Template file for the menulist globalitem
  * `newsarticle.ease`: Template file for the newsarticle globalitem
  * `newsgroup.ease`: Template file for the newsgroup globalitem
  * `newsgroup_grid.ease`: Template file for the newsgroup globalitem (this is an optional variant with a grid setup)
  * `newsgroup_list.ease`: Template file for the newsgroup globalitem (this is an optional variant with a list setup)
  * `product.ease`: Template file for the product globalitem (single product)
  * `products.ease`: Template file for the products globalitem (product list)
  * `products_active_filters.ease`: Template file for the products_active_filters globalitem
  * `simpleitem.ease`: Template file for the simpleitem globalitem
  * `slideshow.ease`: Template file for the slideshow globalitem
* `[pages]`: This folder contains all the main pages of the site
  * `page_calendar.ease`: Template file for the calendar events list page
  * `page_calendaritem.ease`: Template file for the calendar event page
  * `page_contentitems.ease`: Template file for the contentitems pages (These are the dynamic pages)
  * `page_frontpage.ease`: Template file for the frontpage (this is the first page users land on)
  * `page_newsarticle.ease`: Template file for the news article page
  * `page_newsgroup.ease`: Template file for the newsgroup page (newsarticle list)
  * `page_newsletter_unsubscribe_success.ease`: Template file for the newsletter successful unsubscribe landing page 
  * `page_product.ease`: Template file for the product page (single product)
  * `page_products.ease`: Template file for the products list page
* `masterpage.ease`: The main template file, which all others are nested to. This template contains the main structure (<head>, <body,> etc...)
* `page_newsletter_email.html`: Html template file for the newsletter
