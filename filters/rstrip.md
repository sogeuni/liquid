---
title: rstrip
description: Liquid filter that removes all whitespace from the right side of a string.
---

Removes all whitespace (tabs, spaces, and newlines) from the right side of a string.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "          So much room for activities!          " | rstrip }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ "          So much room for activities!          " | rstrip }}
```
