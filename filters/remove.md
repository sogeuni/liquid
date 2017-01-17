---
title: remove
description: 문자열에서 주어진 하위 문자열과 일치하는 모든 항목을 제거하는 Liquid 필터.
---

문자열에서 지정된 하위 문자열과 일치하는 모든 부분을 제거합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "I strained to see the train through the rain" | remove: "rain" }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ "I strained to see the train through the rain" | remove: "rain" }}
```
