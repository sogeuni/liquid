---
title: times
description: 숫자에 다른 숫자를 곱하는 Liquid 필터.
---

숫자에 다른 숫자를 곱합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 3 | times: 2 }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ 3 | times: 2 }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 24 | times: 7 }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ 24 | times: 7 }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 183.357 | times: 12 }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ 183.357 | times: 12 }}
```
