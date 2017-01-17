---
title: ceil
description: 가장 가까운 정수로 올림하는 Liquid 필터
---

입력을 가장 가까운 정수로 올림합니다. Liquid는 필터를 적용하기 전에 입력 값을 숫자로 변환하려고 시도합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 1.2 | ceil }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ 1.2 | ceil }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 2.0 | ceil }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ 2.0 | ceil }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 183.357 | ceil }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ 183.357 | ceil }}
```

여기서 입력값은 문자열입니다:

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "3.5" | ceil }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ "3.5" | ceil }}
```
