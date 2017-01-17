---
title: strip
description: Liquid filter that removes whitespace from the left and right sides of a string.
---

Removes all whitespace (tabs, spaces, and newlines) from both the left and right side of a string. It does not affect spaces between words.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "          So much room for activities!          " | strip }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ "          So much room for activities!          " | strip }}
```
