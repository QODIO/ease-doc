# Ease Templates Refernece - Statments

Statements
* [for (endfor)](#for)
* [if  (elseif, else, endif)](#if)
* [include](#include)
* [set](#set)

Methods
* [dump_template_vars](#dump_template_vars)
* [dump_translate_vars](#dump_translate_vars)
* [dump_vars](#dump_vars)
* [displayMedia](#displaymedia)
* [getQuery](#getquery)


# Statements

## for

Loop over each item in a sequence. For example, to display a list of users provided in a variable called *users*:

```twig
<h1>Members</h1>
<ul>
    {% for user in users %}
        <li>{{ user.username|e }}</li>
    {% endfor %}
</ul>
```

> A sequence can be either an array or an object.

If you do need to iterate over a sequence of numbers, you can use the [] operators:

```twig
{% for i in [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10] %}
    * {{ i }}
{% endfor %}
```

The above snippet of code would print all numbers from 0 to 10.


## if

The `if` statement in Ease Templates is comparable with the *if* statements of PHP.

In the simplest form you can use it to test if an expression evaluates to *true*:

```twig
{% if online == false %}
    <p>Our website is in maintenance mode. Please, come back later.</p>
{% endif %}
```

You can also test if an array is not empty:
```twig
{% if users %}
    <ul>
        {% for user in users %}
            <li>{{ user.username|e }}</li>
        {% endfor %}
    </ul>
{% endif %}
```

You can also use `not` or `!` to check for values that evaluate to false:

```twig
{% if not user.subscribed %}
    <p>You are not subscribed to our mailing list.</p>
{% endif %}

{% if !user.subscribed %}
    <p>You are not subscribed to our mailing list.</p>
{% endif %}
```

For multiple branches `elseif` and `else` can be used like in PHP. You can use more complex expressions there too:

```twig
{% if kenny.sick %}
    Kenny is sick.
{% elseif kenny.dead %}
    You killed Kenny! You bastard!!!
{% else %}
    Kenny looks okay --- so far
{% endif %}
```

> The rules to determine if an expression is *true* or *false* are the same as in PHP; here are the edge cases rules:

Value | Boolean evaluation
--- | ---
empty string | false
numeric zero | false
whitespace-only string | true
empty array | false
null | false
non-empty array | true
object | true


## include

The `include` statement includes a template and returns the rendered content of that file into the current namespace:

```twig
{% include 'header.ease' %}
    Body
{% include 'footer.ease' %}
```

Included templates have access to the variables of the active context.


## set

Inside code blocks you can also assign values to variables. Assignments use the `set` tag.

Here is how you can assign the *bar* value to the *foo* variable:

```twig
{% set foo = 'bar' %}
```

After the set call, the *foo* variable is available in the template like any other ones:

```twig
{# displays bar #}
{{ foo }}
```

The assigned value can be any valid Ease Template expressions:

```twig
{% set foo = [1, 2] %}
{% set foo = {'foo': 'bar'} %}
{% set foo = 'foo' ~ 'bar' %}
```

> Note that loops are, for security reasons, scoped in Ease Template; therefore a variable declared inside a for loop is not accessible outside the loop itself:

```twig
{% for item in list %}
    {% set foo = item %}
{% endfor %}

{# foo is NOT available #}
```


# Methods

## displayMedia

The `displayMedia` method is used to display images, video, flash. The method takes 4 parameters.

* filepage: The path to the media file you want to display
* width: The width of the media element
* height: The height of the media element
* class: An optional paramenter, defining a class to be added to the media element

```twig
{% displayMedia('/images/logo.png', 300, 200, 'logo_image') %}
```


## dump_template_vars

Display all the defined template variables and their content.
This method is very useful for debugging purposes.


## dump_translate_vars

Display all the defined translate variables and their content.
This method is very useful for debugging purposes.


## dump_vars

Display all the defined variables and their content.
This method is very useful for debugging purposes.


## getQuery

The `getQuery` method is used to fetch the current querystring (*GET*), with an optional parameter; which contains a comma separated string of keys of querystring parameters that should not be included. This is useful for generating url strings.

This example is useful for language urls, where you want to keep all the other querystring parameters.

```twig
<a href="?{% getQuery('language') %}&language=en">EN</a>
<a href="?{% getQuery('language') %}&language=da">DA</a>
```

