---
title: first
description: 배열의 첫 번째 아이템을 리턴하는 Liquid 필터.
---

배열의 첫 번째 아이템을 리턴합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign my_array = "apples, oranges, peaches, plums" | split: ", " %}

{{ my_array.first }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{% assign my_array = "apples, oranges, peaches, plums" | split: ", " %}

{{ my_array.first }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign my_array = "zebra, octopus, giraffe, tiger" | split: ", " %}

{{ my_array.first }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{% assign my_array = "zebra, octopus, giraffe, tiger" | split: ", " %}

{{ my_array.first }}
```
