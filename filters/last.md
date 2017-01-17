---
title: last
description: 배열의 마지막 값을 리턴하는 Liquid 필터.
---

배열의 마지막 아이템을 리턴합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign my_array = "apples, oranges, peaches, plums" | split: ", " %}

{{ my_array.last }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{% assign my_array = "apples, oranges, peaches, plums" | split: ", " %}

{{ my_array.last }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign my_array = "zebra, octopus, giraffe, tiger" | split: ", " %}

{{ my_array.last }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{% assign my_array = "zebra, octopus, giraffe, tiger" | split: ", " %}

{{ my_array.last }}
```
