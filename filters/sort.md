---
title: sort
description: 대/소문자를 구분하여 배열을 정렬하는 Liquid 필터.
---

배열의 아이템을 속성 값에 따라 정렬합니다. 정렬 순서는 대/소문자를 구분합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign my_array = "zebra, octopus, giraffe, Sally Snake" | split: ", " %}

{{ my_array | sort | join: ", " }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{% assign my_array = "zebra, octopus, giraffe, Sally Snake" | split: ", " %}

{{ my_array | sort | join: ", " }}
```
