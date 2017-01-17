---
title: replace_first
description: 문자열에서 주어진 하위 문자열과 일치하는 첫 번째 부분을 변경하는 Liquid 필터
---

문자열에서 첫 번째 파라미터와 처음으로 일치하는 부분을 두 번째 파라미터로 변환합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign my_string = "Take my protein pills and put my helmet on" %}
{{ my_string | replace_first: "my", "your" }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{% assign my_string = "Take my protein pills and put my helmet on" %}
{{ my_string | replace_first: "my", "your" }}
```
