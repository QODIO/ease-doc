#Ease Templates for Template Designers

This document describes the syntax and semantics of the template engine and will be most useful as reference to those creating Ease templates. 


##Synopsis

A template is simply a text file. It can generate any text-based format (HTML, XML, CSV, LaTeX, etc.). It has the extension, .ease.

A template contains *variables* or *expressions*, which get replaced with values when the template is evaluated, and *tags*, which control the logic of the template.

Below is a minimal template that illustrates a few basics. We will cover further details later on:

```twig
<!DOCTYPE html>
<html>
    <head>
        <title>My Webpage</title>
    </head>
    <body>
        <ul id="navigation">
        {% for item in navigation %}
            <li><a href="{{ item.href }}">{{ item.caption }}</a></li>
        {% endfor %}
        </ul>

        <h1>My Webpage</h1>
        {{ a_variable }}
    </body>
</html>
```

There are two kinds of delimiters: `{% ... %}` and `{{ ... }}`. The first one is used to execute statements such as for-loops, the latter prints the result of an expression to the template.


##IDEs Integration

The Ease template engine is based on the syntax of the Twig template engine. Therefor many IDEs support syntax highlighting and auto-completion for Ease (as long as they support Twig):
* Textmate via the [Twig bundle](https://github.com/Anomareh/PHP-Twig.tmbundle)
* Vim via the [Jinja syntax plugin](http://jinja.pocoo.org/docs/integration/#vim) or the [vim-twig plugin](https://github.com/evidens/vim-twig)
* Netbeans via the Twig syntax plugin (until 7.1, native as of 7.2)
* PhpStorm (native as of 2.1)
* Eclipse via the [Twig plugin](https://github.com/pulse00/Twig-Eclipse-Plugin)
* Sublime Text via the [Twig bundle](https://github.com/Anomareh/PHP-Twig.tmbundle)
* GtkSourceView via the [Twig language definition](https://github.com/gabrielcorpse/gedit-twig-template-language) (used by gedit and other projects)
* Coda and SubEthaEdit via the [Twig syntax mode](https://github.com/bobthecow/Twig-HTML.mode)
* Coda 2 via the other [Twig syntax mode](https://github.com/muxx/Twig-HTML.mode)
* Komodo and Komodo Edit via the Twig highlight/syntax check mode
* Notepad++ via the [Notepad++ Twig Highlighter](https://github.com/Banane9/notepadplusplus-twig)
* Emacs via [web-mode.el](http://web-mode.org/)
* Atom via the [PHP-twig for atom](https://github.com/reesef/php-twig)


##Variables

Variables may have attributes or elements you can access, too. You can use a dot (.) or ([]) to access child attributes of a variable:

```twig
{{ foo.bar }}
{{ foo['bar'] }}
```

>It's important to know that the curly braces are not part of the variable but the print statement. When accessing variables inside tags, don't put the braces around them.


##Global Variables

The following variables are always available in templates:
chosen          | 
    ...         | Contains objects that are currently chosen. E.g. `menuitem`, `product`, `newsarticle` etc.
application     | 
    name        | The name of the site
    description | The description of the site
analytics
    id          | The Google Analytics ID
addthis
    id          | The AddThis ID
domain
    url         | Site domain name
language
    site        | The currently chosen site language
    ease        | The currently chosen Ease language
    url
        ...     | Contains the urls for language switching. E.g. `fo`, `da`, `en` etc.
        da      | => ?p=frontpage&l=da
        en      | => ?p=frontpage&l=en
ease
    languages   | A numeric array containing all the available languages
    pagemenus
        disabled    | True if page menus are disabled
        settings
            filescollections
                allowed_filetypes   | A numeric array containing all the allowed filetypes for filescollections
                products
                    currency        |  Currently chosen currency
                    locales
                        fo          | The string for faroese localization
                        da          | The string for danish localization
                        en          | The string for english localization
                    currency_patterns
                        fo          | The currency patterns string for faroese localization
                        da          | The currency patterns string for danish localization
                        en          | The currency patterns string for english localization
        loggedin    | True if user is logged in
        version     | The current version of Ease
GET     | An array containing all the provided GET variables
POST    | An array containing all the provided GET variables
