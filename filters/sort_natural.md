---
title: sort_natural
description: 대소문자를 구분하지 않는 순서로 배열을 정렬하는 Liquid 필터.
---

배열의 아이템을 속성 값에 따라 정렬합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign my_array = "zebra, octopus, giraffe, Sally Snake" | split: ", " %}

{{ my_array | sort_natural | join: ", " }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
giraffe, octopus, Sally Snake, zebra
```
