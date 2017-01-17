---
title: round
description: Liquid filter that rounds a number to the nearest integer.
---

Rounds an input number to the nearest integer or, if a number is specified as an argument, to that number of decimal places.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 1.2 | round }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ 1.2 | round }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 2.7 | round }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ 2.7 | round }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 183.357 | round: 2 }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ 183.357 | round: 2 }}
```
