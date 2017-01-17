---
title: replace
description: Liquid filter that replaces all occurences of a given substring in a string.
---

Replaces every occurrence of an argument in a string with the second argument.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "Take my protein pills and put my helmet on" | replace: "my", "your" }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ "Take my protein pills and put my helmet on" | replace: "my", "your" }}
```
