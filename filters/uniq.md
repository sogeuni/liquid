---
title: uniq
description: 배열에서 중복되는 아이템을 제거하는 Liquid 필터.
---

배열에서 중복되는 아이템을 제거합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign my_array = "ants, bugs, bees, bugs, ants" | split: ", " %}

{{ my_array | uniq | join: ", " }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{% assign my_array = "ants, bugs, bees, bugs, ants" | split: ", " %}

{{ my_array | uniq | join: ", " }}
```
