---
title: downcase
description: 문자열을 소문자로 변환하는 Liquid 필터.
---

문자열의 모든 문자를 소문자로 변환합니다. 문자열이 이미 모두 소문자라면 아무런 변화가 없습니다.

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
