---
title: minus
description: Liquid filter that subtracts one number from another.
---

Subtracts a number from another number.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 4 | minus: 2 }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ 4 | minus: 2 }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 16 | minus: 4 }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ 16 | minus: 4 }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 183.357 | minus: 12 }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ 183.357 | minus: 12 }}
```
