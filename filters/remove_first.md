---
title: remove_first
description: Liquid filter that removes the first occurence of a given substring from a string.
---

Removes only the first occurrence of the specified substring from a string.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "I strained to see the train through the rain" | remove_first: "rain" }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ "I strained to see the train through the rain" | remove_first: "rain" }}
```
