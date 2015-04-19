#Ease Templates Refernece - Statments

##if

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


## set

Inside code blocks you can also assign values to variables. Assignments use the set tag and can have multiple targets.

Here is how you can assign the bar value to the foo variable:

```twig
{% set foo = 'bar' %}
```

After the set call, the foo variable is available in the template like any other ones:

```twig
{# displays bar #}
{{ foo }}
```

The assigned value can be any valid Twig expressions:

```twig
{% set foo = [1, 2] %}
{% set foo = {'foo': 'bar'} %}
{% set foo = 'foo' ~ 'bar' %}
```

> Note that loops are scoped in Twig; therefore a variable declared inside a for loop is not accessible outside the loop itself:

```twig
{% for item in list %}
    {% set foo = item %}
{% endfor %}

{# foo is NOT available #}
```

