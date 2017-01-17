---
title: append
description: Liquid filter that appends a string to another string.
---

Concatenates two strings and returns the concatenated value.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "/my/fancy/url" | append: ".html" }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ "/my/fancy/url" | append: ".html" }}
```

`append` can also be used with variables:

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign filename = "/index.html" %}
{{ "website.com" | append: filename }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{% assign filename = "/index.html" %}
{{ "website.com" | append: filename }}
```
