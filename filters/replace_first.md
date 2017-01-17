---
title: replace_first
description: Liquid filter that replaces the first occurrence of a given substring in a string.
---

Replaces only the first occurrence of the first argument in a string with the second argument.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign my_string = "Take my protein pills and put my helmet on" %}
{{ my_string | replace_first: "my", "your" }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{% assign my_string = "Take my protein pills and put my helmet on" %}
{{ my_string | replace_first: "my", "your" }}
```
