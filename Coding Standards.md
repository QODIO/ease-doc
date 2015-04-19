#Coding Standards<br>Ease Templates

When writing Ease templates, we recommend you to follow these coding standards:

* Put one (and only one) space after the start of a delimiter ({{, {%, and {#) and before the end of a delimiter (}}, %}, and #}):
```twig
{{ foo }}
{# comment #}
{% if foo %}{% endif %}
```

* Put one (and only one) space before and after the following operators: comparison operators (==, !=, <, >, >=, <=), math operators (+, -, /, *, %, //, **), logic operators (not, and, or), ~, is, in, and the ternary operator (?:):
```twig
{{ 1 + 2 }}
{{ foo ~ bar }}
{{ true ? true : false }}
```

* Put one (and only one) space after the : sign in hashes and , in arrays and hashes:
```twig
{{ [1, 2, 3] }}
{{ {'foo': 'bar'} }}
```

* Do not put any spaces after an opening parenthesis and before a closing parenthesis in expressions:
```twig
{{ 1 + (2 * 3) }} // NOT SUPPORTED YET
```

* Do not put any spaces before and after string delimiters:
```twig
{{ 'foo' }}
{{ "foo" }}
```

* Do not put any spaces before and after the following operators: `|`, `.`, `[]`:

```twig
{{ foo|upper|lower }}
{{ user.name }}
{{ user[name] }}
{% for i in [1, 2, 3, 4] %}{% endfor %}
```

* Do not put any spaces before and after the parenthesis used for filter and function calls:
```twig
{{ foo|default('foo') }}
```

* Do not put any spaces before and after the opening and the closing of arrays and hashes:
```twig
{{ [1, 2, 3] }}
{{ {'foo': 'bar'} }}
```

* Use lower cased and underscored variable names:
```twig
{% set foo = 'foo' %}
{% set foo_bar = 'foo' %}
```

* Indent your code inside tags (use the same indentation as the one used for the target language of the rendered template):
```twig
{% if true %}
    true
{% endif %}
```
