---
title: upcase
description: 문자열을 모두 대문자로 변환하는 Liquid 필터.
---

문자열의 모든 문자를 대문자로 변환합니다. 이미 모두 대문자일 경우에는 문자열은 변경되지 않습니다.

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
