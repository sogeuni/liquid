---
title: capitalize
description: Liquid filter that capitalizes the first character in a string.
---

Makes the first character of a string capitalized.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "title" | capitalize }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
Title
```

`capitalize` only capitalizes the first character of the string, so later words are not affected:

 <p class="code-label">입력</p>
```liquid
{% raw %}
{{ "my great title" | capitalize }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
My great title
```
