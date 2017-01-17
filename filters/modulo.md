---
title: modulo
description: 나누기 연산에서 나머지를 반환하는 Liquid 필터.
---

나누기 연산의 나머지를 리턴합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 3 | modulo: 2 }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ 3 | modulo: 2 }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 24 | modulo: 7 }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ 24 | modulo: 7 }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 183.357 | modulo: 12 }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ 183.357 | modulo: 12 }}
```
