#Ease Templates Refernece - Statments

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

