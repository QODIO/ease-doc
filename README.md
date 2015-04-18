#Ease Templates for Template Designers

This document describes the syntax and semantics of the template engine and will be most useful as reference to those creating Ease templates. 


##Synopsis

A template is simply a text file. It can generate any text-based format (HTML, XML, CSV, LaTeX, etc.). It has the extension, .ease.

A template contains *variables* or *expressions*, which get replaced with values when the template is evaluated, and *tags*, which control the logic of the template.

Below is a minimal template that illustrates a few basics. We will cover further details later on:

```html
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

IDEs Integration
The Ease template engine is based on the syntax of the Twig template engine. Therefor many IDEs support syntax highlighting and auto-completion for Ease (as long as they support Twig):

Textmate via the Twig bundle
Vim via the Jinja syntax plugin or the vim-twig plugin
Netbeans via the Twig syntax plugin (until 7.1, native as of 7.2)
PhpStorm (native as of 2.1)
Eclipse via the Twig plugin
Sublime Text via the Twig bundle
GtkSourceView via the Twig language definition (used by gedit and other projects)
Coda and SubEthaEdit via the Twig syntax mode
Coda 2 via the other Twig syntax mode
Komodo and Komodo Edit via the Twig highlight/syntax check mode
Notepad++ via the Notepad++ Twig Highlighter
Emacs via web-mode.el
Atom via the PHP-twig for atom
