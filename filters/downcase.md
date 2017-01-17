---
title: downcase
description: Liquid filter that coverts a string to lowercase.
---

Makes each character in a string lowercase. It has no effect on strings which are already all lowercase.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "Parker Moore" | downcase }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ "Parker Moore" | downcase }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "apple" | downcase }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ "apple" | downcase }}
```
