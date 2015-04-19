# Filters<br>Ease Templates Reference

Filters
* [abs](#abs)
* [capitalize](#capitalize)
* [ceil](#ceil)
* [convert_encoding](#convert_encoding)
* [date](#date)
* [date_old](#date_old)
* [date_modify](#date_modify)
* [default](#default)
* [dump](#dump)
* [empty](#empty)
* [escape (or e)](#escape)
* [false](#false)
* [first](#first)
* [floor](#floor)
* [format](#format)
* [if (or ifelse)](#if)
* [isset](#isset)
* [join](#join)
* [json_encode](#json_encode)
* [keys](#keys)
* [last](#last)
* [length](#length)
* [lower](#lower)
* [merge](#merge)
* [nl2br](#nl2br)
* [not_empty](#not_empty)
* [number_format](#number_format)
* [print_r](#print_r)
* [replace](#replace)
* [resize](#resize)
* [reverse](#reverse)
* [round](#round)
* [slice](#slice)
* [sort](#sort)
* [split](#split)
* [striptags](#striptags)
* [substr (or substring)](#substr)
* [title](#title)
* [trim](#trim)
* [true](#true)
* [equals](#equals)
* [truncate](#truncate)
* [truncate_html](#truncate_html)
* [upper](#upper)
* [url_encode](#url_encode)


# Filters


## abs

The `abs` filter returns the absolute value.

```twig
{# number = -5 #}

{{ number|abs }}

{# outputs 5 #}
```

## capitalize

The `capitalize` filter capitalizes a value. The first character will be uppercase, all others lowercase:

```twig
{{ 'my first car'|capitalize }}

{# outputs 'My first car' #}
```


## ceil

The `ceil` filter rounds a number up to the next highest integer value:

```twig
{{ 10.64|ceil }}
{# returns 11 #}
```


## convert_encoding

The `convert_encoding` filter converts a string from one encoding to another. The first argument is the expected output charset and the second one is the input charset:

```twig
{{ data|convert_encoding('UTF-8', 'iso-2022-jp') }}
```


## date

The `date` filter formats a date to a given format:

```twig
{{ post.published_at|date("%d/%m/%Y") }}
```

The `date` filter accepts strings (it must be in a format supported by the [strtotime](http://www.php.net/strtotime) function). For instance, to display the current date, filter the word "now":

```twig
{{ "now"|date("%B %e, %Y %H:%M") }}
```

If no format is provided, Ease Template will use the default one: "%Y-%m-%d %H:%M:%S". 

The `date` filter uses PHP's [strftime](http://www.php.net/strftime) internally, here is list of possible formatting characters

&nbsp; | Day | &nbsp;
--- | --- | ---
%a | An abbreviated textual representation of the day	| Sun through Sat
%A | A full textual representation of the day | Sunday through Saturday
%d | Two-digit day of the month (with leading zeros) | 01 to 31
%e | Day of the month, with a space preceding single digits. Not implemented as described on Windows. See below for more information. | 1 to 31
%j | Day of the year, 3 digits with leading zeros | 001 to 366
%u | ISO-8601 numeric representation of the day of the week | 1 (for Monday) though 7 (for Sunday)
%w | Numeric representation of the day of the week | 0 (for Sunday) through 6 (for Saturday)

&nbsp; | Week | &nbsp;
--- | --- | ---
%U | Week number of the given year, starting with the first Sunday as the first week | 13 (for the 13th full week of the year)
%V | ISO-8601:1988 week number of the given year, starting with the first week of the year with at least 4 weekdays, with Monday being the start of the week | 01 through 53 (where 53 accounts for an overlapping week)
%W | A numeric representation of the week of the year, starting with the first Monday as the first week | 46 (for the 46th week of the year beginning with a Monday)

&nbsp; | Month | &nbsp;
--- | --- | ---
%b | Abbreviated month name, based on the locale | Jan through Dec
%B | Full month name, based on the locale | January through December
%h | Abbreviated month name, based on the locale (an alias of %b) | Jan through Dec
%m | Two digit representation of the month | 01 (for January) through 12 (for December)

&nbsp; | Year | &nbsp;
--- | --- | ---
%C | Two digit representation of the century (year divided by 100, truncated to an integer) | 19 for the 20th Century
%g | Two digit representation of the year going by ISO-8601:1988 standards (see %V) | Example: 09 for the week of January 6, 2009
%G | The full four-digit version of %g | Example: 2008 for the week of January 3, 2009
%y | Two digit representation of the year | Example: 09 for 2009, 79 for 1979
%Y | Four digit representation for the year | Example: 2038

&nbsp; | Time | &nbsp;
--- | --- | ---
%H | Two digit representation of the hour in 24-hour format | 00 through 23
%k | Two digit representation of the hour in 24-hour format, with a space preceding single digits | 0 through 23
%I | Two digit representation of the hour in 12-hour format | 01 through 12
%l | (lower-case 'L')	Hour in 12-hour format, with a space preceding single digits | 1 through 12
%M | Two digit representation of the minute | 00 through 59
%p | UPPER-CASE 'AM' or 'PM' based on the given time | Example: AM for 00:31, PM for 22:23
%P | lower-case 'am' or 'pm' based on the given time | Example: am for 00:31, pm for 22:23
%r | Same as "%I:%M:%S %p" | Example: 09:34:17 PM for 21:34:17
%R | Same as "%H:%M" | Example: 00:35 for 12:35 AM, 16:44 for 4:44 PM
%S | Two digit representation of the second | 00 through 59
%T | Same as "%H:%M:%S" | Example: 21:34:17 for 09:34:17 PM
%X | Preferred time representation based on locale, without the date | Example: 03:59:16 or 15:59:16
%z | The time zone offset. Not implemented as described on Windows. See below for more information. | Example: -0500 for US Eastern Time
%Z | The time zone abbreviation. Not implemented as described on Windows. See below for more information. | Example: EST for Eastern Time

&nbsp; | Time and Date Stamps | &nbsp;
--- | --- | ---
%c | Preferred date and time stamp based on locale | Example: Tue Feb 5 00:45:10 2009 for February 5, 2009 at 12:45:10 AM
%D | Same as "%m/%d/%y" | Example: 02/05/09 for February 5, 2009
%F | Same as "%Y-%m-%d" (commonly used in database datestamps) | Example: 2009-02-05 for February 5, 2009
%s | Unix Epoch Time timestamp (same as the time() function) | Example: 305815200 for September 10, 1979 08:40:00 AM
%x | Preferred date representation based on locale, without the time | Example: 02/05/09 for February 5, 2009

&nbsp; | Miscellaneous | &nbsp;
--- | --- | ---
%n | A newline character ("\n") | ---
%t | A Tab character ("\t") | ---
%% | A literal percentage character ("%") | ---


## date_old

The `date_old` filter functions much like `date` filter, but uses PHP's [date](http://www.php.net/date) function internally.

> The `date_old` filter does not support locales


## date_modify

The `date_modify` filter modifies a date with a given modifier string:

```twig
{{ post.published_at|date_modify("+1 day")|date("%m/%d/%Y") }}
```

The `date_modify` filter accepts strings (it must be in a format supported by the [strtotime](http://www.php.net/strtotime) function). You can easily combine it with the `date` filter for formatting.


## default

The default filter returns the passed default value if the value is undefined or empty, otherwise the value of the variable:

```twig
{{ var|default('var is not defined') }}

{{ var.foo|default('foo item on var is not defined') }}

{{ var['foo']|default('foo item on var is not defined') }}

{{ ''|default('passed var is empty')  }}
```

When using the default filter on an expression that uses variables in some method calls, be sure to use the default filter whenever a variable can be undefined:

```twig
{{ var.method(foo|default('foo'))|default('foo') }}
```


## dump

The `dump` filter dumps information about a variable to the screen. It also has an optional parameter to disable escaping of html content.

```twig
{{ some_var|dump }}
{{ some_var|dump(false) }}
```


## empty

The `empty` filter checks if a variable is empty, and returns true of false:

```twig
{{ some_var|empty|true('it is empty') }}
```

> PHP's [empty](http://www.php.net/empty) is used internally


## escape (e)

The `escape` filter escapes a string for safe insertion into the final output. It supports different escaping strategies depending on the template context.

By default, it uses the HTML escaping strategy:

```twig
{{ user.username|escape }}
```

For convenience, the `e` filter is defined as an alias:

```twig
{{ user.username|e }}
```

The `escape` filter can also be used in other contexts than HTML thanks to an optional argument which defines the escaping strategy to use:

```twig
{{ user.username|e }}
{# is equivalent to #}
{{ user.username|e('html') }}
```

And here is how to escape variables included in JavaScript code (NOT SUPPORTED YET):

```twig
{{ user.username|escape('js') }}
{{ user.username|e('js') }}
```

The escape filter supports the following escaping strategies:

* `html`: escapes a string for the *HTML body* context.
* `js`: NOT SUPPORTED YET: escapes a string for the *JavaScript context*.
* `url`: escapes a string for the *URI or parameter contexts*. This should not be used to escape an entire URI; only a subcomponent being inserted.
* `html_attr`: escapes a string for the *HTML attribute* context (NOT SUPPORTED YET).


## false

The `false` filter, returns first parameter if variable is *false*, and the second parameter if *true*

```twig
{{ some_var|false('yup, it is false', 'nope, it is not false') }}
```


## first

The `first` filter returns the first "element" of a sequence, a mapping, or a string:

```twig
{{ [1, 2, 3, 4]|first }}
{# outputs 1 #}

{{ { a: 1, b: 2, c: 3, d: 4 }|first }}
{# outputs 1 #}

{{ '1234'|first }}
{# outputs 1 #}
```


## floor

The `floor` filter rounds a number down to the next lowest integer value:

```twig
{{ 10.64|floor }}
{# returns 10 #}
```


## format

The `format` filter formats a given string by replacing the placeholders (placeholders follows the [sprintf](http://www.php.net/sprintf) notation):


```twig
{{ "I like %s and %s."|format(foo, "bar") }}

{# outputs: "I like foo and bar"
   if the foo parameter contains the "foo" string. #}
```


## if (ifelse)

The `if` filter, returns first parameter if variable is *true*, and the second parameter if *false*

```twig
{{ some_var|if('true', 'false') }}
{{ some_var|ifelse('true', 'false') }}
```

> The `if` filter works differently from the `true` and `false` filters internally, by using PHP's shorthand comparison statement.


## isset

The `isset` filter checks if a variable is set, and returns true of false:

```twig
{{ some_var|isset|true('it is not set') }}
```

> PHP's [isset](http://www.php.net/isset) is used internally


## join

The `join` filter returns a string which is the concatenation of the items of a sequence:

```twig
{{ [1, 2, 3]|join }}
{# returns 123 #}
```

The separator between elements is an empty string per default, but you can define it with the optional first parameter:

```twig
{{ [1, 2, 3]|join('|') }}
{# outputs 1|2|3 #}
```


## json_encode

The `json_encode` filter returns the JSON representation of a value:

```twig
{{ data|json_encode() }}
```


## keys

The `keys` filter returns the keys of an array. It is useful when you want to iterate over the keys of an array:

```twig
{% for key in array|keys %}
    ...
{% endfor %}
```


## last

The `last` filter returns the last "element" of a sequence, a mapping, or a string:

```twig
{{ [1, 2, 3, 4]|last }}
{# outputs 4 #}

{{ { a: 1, b: 2, c: 3, d: 4 }|last }}
{# outputs 4 #}

{{ '1234'|last }}
{# outputs 4 #}
```


## length

The `length` filter returns the number of items of a sequence or mapping, or the length of a string:

```twig
{% if users|length > 10 %}
    ...
{% endif %}
```


## lower

The `lower` filter converts a value to lowercase:

```twig
{{ 'WELCOME'|lower }}

{# outputs 'welcome' #}
```


## merge

The `merge` filter merges an array with another array:

```twig
{% set values = [1, 2] %}

{% set values = values|merge(['apple', 'orange']) %}

{# values now contains [1, 2, 'apple', 'orange'] #}
```

New values are added at the end of the existing ones.

The `merge` filter also works on hashes:

```twig
{% set items = { 'apple': 'fruit', 'orange': 'fruit', 'peugeot': 'unknown' } %}

{% set items = items|merge({ 'peugeot': 'car', 'renault': 'car' }) %}

{# items now contains { 'apple': 'fruit', 'orange': 'fruit', 'peugeot': 'car', 'renault': 'car' } #}
```

For hashes, the merging process occurs on the keys: if the key does not already exist, it is added but if the key already exists, its value is overridden.


## nl2br

The `nl2br` filter inserts HTML line breaks before all newlines in a string:

```twig
{{ "I like Ease.\nYou will like it too."|nl2br }}
{# outputs

    I like Ease.<br />
    You will like it too.

#}
```


## not_empty

The `not_empty` filter checks if a variable is NOT empty, and returns true of false:

```twig
{{ some_var|not_empty|true('it is NOT empty') }}
```

> PHP's [empty](http://www.php.net/empty) is used internally


## number_format

The `number_format` filter formats numbers. It is a wrapper around PHP's [number_format](http://php.net/number_format) function:

```twig
{{ 200.35|number_format }}
```

You can control the number of decimal places, decimal point, and thousands separator using the additional arguments:

```twig
{{ 9800.333|number_format(2, '.', ',') }}
```

If no formatting options are provided then `number_format` will use the default formatting options of:

* 0 decimal places.
* , as the decimal point.
* . as the thousands separator.


## print_r

The `print_r` filter prints human-readable information about a variable:

```twig
{{ some_var|print_r }}
```


## replace

The `replace` filter formats a given string by replacing a string with another:

```twig
{{ "I like %this% and %that%."|replace('%this%', foo)|replace('%that%', "bar") }}

{# outputs I like foo and bar
   if the foo parameter equals to the foo string. #}
```


## resize

The `resize` filter, resizes and caches and image. The image 

These are the parameters the filter uses:

* `width`: The width of the image, if no width or 0 is given, then it sets the width to auto
* `height`: The height of the image, if no height or 0 is given, then it sets the height to auto
* `fit`: Sets the fitting of the image: `inside`, `outside`, `stretch` or `crop` (you can also use `i`, `o`, `s` or `c`)
⋅⋅⋅ This is *optional*, default is 'crop'
* `fallback`: *Optional*: The fallback image to use, if no image is found
⋅⋅⋅ This is *optional*

```twig
{{ article.image|resize(200, 150, 'crop') }}
{{ '/images/logo.png'|resize(200, 150, 'crop') }}
```


## reverse

The `reverse` filter reverses a sequence, a mapping, or a string:

```twig
{% for user in users|reverse %}
    ...
{% endfor %}

{{ '1234'|reverse }}

{# outputs 4321 #}
```

For sequences and mappings, numeric keys are not preserved. To reverse them as well, pass *true* as an argument to the `reverse` filter:

```twig
{% for key, value in {1: "a", 2: "b", 3: "c"}|reverse %}
    {{ key }}: {{ value }}
{%- endfor %}

{# output: 0: c    1: b    2: a #}

{% for key, value in {1: "a", 2: "b", 3: "c"}|reverse(true) %}
    {{ key }}: {{ value }}
{%- endfor %}

{# output: 3: c    2: b    1: a #}
```


## round

The `round` filter rounds a number to a given precision:

```twig
{{ 42.55|round }}
{# outputs 43 #}

{{ 42.55|round(1, 'floor') }}
{# outputs 42.5 #}
```
The round filter takes two optional arguments; the first one specifies the precision (default is 0) and the second the rounding method (default is *common*):

* `common` rounds either up or down (rounds the value up to precision decimal places away from zero, when it is half way there -- making 1.5 into 2 and -1.5 into -2);
* `ceil` (or `up`) always rounds up;
* `floor` (or `down`) always rounds down.


## slice

The `slice` filter extracts a slice of a sequence, a mapping, or a string:

```twig
{% for i in [1, 2, 3, 4, 5]|slice(1, 2) %}
    {# will iterate over 2 and 3 #}
{% endfor %}

{{ '12345'|slice(1, 2) }}
{# outputs 23 #}
```

You can use any valid expression for both the start and the length:

```twig
{% for i in [1, 2, 3, 4, 5]|slice(start, length) %}
    {# ... #}
{% endfor %}
```

If the start is non-negative, the sequence will start at that start in the variable. If start is negative, the sequence will start that far from the end of the variable.

If length is given and is positive, then the sequence will have up to that many elements in it. If the variable is shorter than the length, then only the available variable elements will be present. If length is given and is negative then the sequence will stop that many elements from the end of the variable. If it is omitted, then the sequence will have everything from offset up until the end of the variable.

You can also use a third parameter if you want to preserve keys of an array

```twig
{% for i in {1: 'one', 2: 'two', 3: 'three', 4: 'four', 5: 'five'}|slice(start, length) %}
    {# will iterate over and return 0: 'two' and 1: 'three' #}
{% endfor %}

{% for i in {1: 'one', 2: 'two', 3: 'three', 4: 'four', 5: 'five'}|slice(start, length, true) %}
    {# will iterate over and return 2: 'two' and 3: 'three' #}
{% endfor %}
```


## sort

The `sort` filter sorts an array:

```twig
{% for user in users|sort %}
    ...
{% endfor %}
```

#### arguments

* `preserve_keys`: Whether to preserve key or not (default *true*)
* `case_sensitive`: Sorting is case sensitive or not (default *false*)
* `natural`: Sorting in natural or not (default *true*)


## split

The `split` filter splits a string by the given delimiter and returns a list of strings:

```twig
{% set foo = "one,two,three"|split(',') %}
{# foo contains ['one', 'two', 'three'] #}
```
You can also pass a limit argument:

* If limit is positive, the returned array will contain a maximum of limit elements with the last element containing the rest of string;
* If limit is negative, all components except the last -limit are returned;
* If limit is zero, then this is treated as 1.

```twig
{% set foo = "one,two,three,four,five"|split(',', 3) %}
{# foo contains ['one', 'two', 'three,four,five'] #}
```


## striptags

The `striptags` filter strips HTML and PHP tags from a string:

```twig
{{ some_html|striptags }}
```

You can use the optional parameter to specify tags which should not be stripped.

```twig
{{ some_html|striptags('<br><a><img>') }}
{% br, a and img tags will be preserved %}
```


## substr (or substring)

The 'substr' or 'substring' filter returns part of a string

#### Arguments

* `start`: Which number character to start from.
* `length`: The number of characters to return. (Optinal)

```twig
```


## title

The `title` filter returns a titlecased version of the value. Words will start with uppercase letters, all remaining characters are lowercase:

```twig
{{ 'my first car'|title }}

{# outputs 'My First Car' #}
```


## trim

The `trim` filter strips whitespace (or other characters) from the beginning and end of a string:

```twig
{{ '  I like Ease.  '|trim }}

{# outputs 'I like Ease.' #}

{{ '  I like Ease.'|trim('.') }}

{# outputs '  I like Ease' #}
```


## true

The `true` filter, returns first parameter if variable is *true*, and the second parameter if *false*

```twig
{{ some_var|true('yup, it is true', 'nope, it is not true') }}
```


## equals

The equals filter, returns second parameter if variable equals first parameter, and the third parameter if it doesn't.

```twig
{{ some_var|equals('john', 'it is john', 'it is not john') }}
```


## truncate

The truncate filter truncates a string to given length

```twig
{{ some_var|truncate(100) }}
{{ some_var|truncate(100, '...') }}
```


## truncate_html

The `truncate_html` filter truncates a html string to given length (length is characters, including html tags).
> Consider using `truncate` filter together with `striptags` filter instead.

```twig
{{ some_var|truncate_html(100) }}
{{ some_var|truncate_html(100, '...') }}
```


## upper

The `upper` filter converts a value to uppercase:

```twig
{{ 'welcome'|upper }}

{# outputs 'WELCOME' #}
```


## url_encode

The `url_encode` filter encodes a given string as URL segment or an array as query string:

```twig
{{ "path-seg*ment"|url_encode }}
{# outputs "path-seg%2Ament" #}

{{ "string with spaces"|url_encode }}
{# outputs "string%20with%20spaces" #}

{{ {'param': 'value', 'foo': 'bar'}|url_encode }}
{# outputs "param=value&foo=bar" #}
```
