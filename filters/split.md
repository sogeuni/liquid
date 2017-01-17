---
title: split
description: 구분자를 사용하여 문자열을 분할하여 배열로 만드는 Liquid 필터.
---

인자를 구분자로 사용하여 입력 문자열을 배열로 분할합니다. 일반적으로 `split`은 문자열에서 쉼표로 구분된 항목을 배열로 변환하는 데 사용합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign beatles = "John, Paul, George, Ringo" | split: ", " %}

{% for member in beatles %}
  {{ member }}
{% endfor %}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{% assign beatles = "John, Paul, George, Ringo" | split: ", " %}

{% for member in beatles %}
  {{ member }}
{% endfor %}
```
