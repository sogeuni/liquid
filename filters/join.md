---
title: join
description: 배열의 문자열을 하나의 문자열로 합치는 Liquid 필터.
---

파라미터를 구분 기호로 배열의 아이템을 하나의 문자열로 합칩니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign beatles = "John, Paul, George, Ringo" | split: ", " %}

{{ beatles | join: " and " }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{% assign beatles = "John, Paul, George, Ringo" | split: ", " %}

{{ beatles | join: " and " }}
```
