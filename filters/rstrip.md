---
title: rstrip
description: 문자열의 오른쪽 공백을 제거하는 Liquid 필터.
---

문자열의 오른쪽의 모든 whitespace(탭, 공백 및 줄바꿈)를 제거합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "          So much room for activities!          " | rstrip }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ "          So much room for activities!          " | rstrip }}
```
