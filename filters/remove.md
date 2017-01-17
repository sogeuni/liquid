---
title: remove
description: Liquid filter that removes all occurences of a given substring from a string.
---

Removes every occurrence of the specified substring from a string.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "I strained to see the train through the rain" | remove: "rain" }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ "I strained to see the train through the rain" | remove: "rain" }}
```
