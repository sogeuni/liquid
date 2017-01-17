---
title: map
description: 객체에서 명명 된 속성을 추출하여 값 배열을 만드는 Liquid 필터.
---

다른 객체에서 명명 된 속성 값을 추출하여 값 배열을 만듭니다.

이 예제에서 'site.pages` 객체에는 웹 사이트의 모든 메타 데이터가 포함되어 있다고 가정합니다. `assign`에 `map` 필터를 사용하여 `site.pages` 객체에서 `category` 속성의 모든 값을 포함하는 변수를 생성합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign all_categories = site.pages | map: "category" %}

{% for item in all_categories %}
{{ item }}
{% endfor %}
{% endraw %}
```

<p class="code-label">결과</p>
```text
business
celebrities
lifestyle
sports
technology
```
