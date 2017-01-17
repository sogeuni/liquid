---
title: replace
description: 문자열에서 주어진 하위 문자열과 일치하는 모든 부분을 변경하는 Liquid 필터.
---

문자열에서 첫 번째 파라미터와 일치하는 모든 부분을 두 번째 파라미터로 변환합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "Take my protein pills and put my helmet on" | replace: "my", "your" }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ "Take my protein pills and put my helmet on" | replace: "my", "your" }}
```
