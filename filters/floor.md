---
title: floor
description: Liquid filter that gets the floor of a number by rounding down to the nearest integer.
---

Rounds a number down to the nearest whole number. Liquid tries to convert the input to a number before the filter is applied.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 1.2 | floor }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ 1.2 | floor }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 2.0 | floor }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ 2.0 | floor }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 183.357 | floor }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ 183.357 | floor }}
```

Here the input value is a string:

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "3.5" | floor }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ "3.5" | floor }}
```
