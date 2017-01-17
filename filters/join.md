---
title: join
description: Liquid filter that joins an array of strings into a single string.
---

Combines the items in an array into a single string using the argument as a separator.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign beatles = "John, Paul, George, Ringo" | split: ", " %}

{{ beatles | join: " and " }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{% assign beatles = "John, Paul, George, Ringo" | split: ", " %}

{{ beatles | join: " and " }}
```
