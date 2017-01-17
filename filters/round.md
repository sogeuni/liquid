---
title: round
description: 정수를 가장 가까운 정수로 반올림하는 Liquid 필터.
---

정수를 가장 가까운 정수로 반올림하거나, 인자가 숫자로 지정된 경우 반올림 할 소숫점 자리를 지정하여 반올림합니다.

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
