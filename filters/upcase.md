---
title: upcase
description: Liquid filter that capitalizes every character in a string.
---

Makes each character in a string uppercase. It has no effect on strings which are already all uppercase.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "Parker Moore" | upcase }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ "Parker Moore" | upcase }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "APPLE" | upcase }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ "APPLE" | upcase }}
```
