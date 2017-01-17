---
title: lstrip
description: 문자열의 왼쪽 공백을 제거하는 Liquid 필터.
---

문자열의 시작 부분의 모든 whitespace(탭, 공백 및 줄바꿈)을 제거합니다. 단어 사이의 공백에는 적용되지 않습니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "          So much room for activities!          " | lstrip }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ "          So much room for activities!          " | lstrip }}
```
