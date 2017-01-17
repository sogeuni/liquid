---
title: default
description: 값이 존재하지 않는 경우 특정값으로 대체하기 위한 Liquid 필터
---

값이 존재하지 않는 경우 대체할 특정값을 지정할 수 있습니다. `default`는 좌변이 `nil`, `false` 또는 빈 값일 경우에 표시됩니다.

예를 들어 `product_price`가 정의되지 않았다면 기본값이 사용됩니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ product_price | default: 2.99 }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
2.99
```

다음 예제에서 `product_price` 값은 정의되었으므로 기본값은 사용되지 않습니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign product_price = 4.99 %}
{{ product_price | default: 2.99 }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
4.99
```

다음 예제에서 `product_price` 값은 빈 값이므로 기본값이 사용됩니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign product_price = "" %}
{{ product_price | default: 2.99 }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
2.99
```
