---
title: size
description: 문자열의 문자 갯수 또는 배열의 아이템 갯수를 리턴하는 Liquid 필터.
---

문자열의 문자 갯수 또는 배열의 아이템 갯수를 리턴합니다. `size`는 점 표기법(`{% raw %}{{ my_string.size }}{% endraw %}`과 같이)과 함께 사용할 수 있습니다. 따라서, 조건식 태그 내에서 `size`를 사용할 수 있습니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "Ground control to Major Tom." | size }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ "Ground control to Major Tom." | size }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign my_array = "apples, oranges, peaches, plums" | split: ", " %}

{{ my_array | size }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{% assign my_array = "apples, oranges, peaches, plums" | split: ", " %}

{{ my_array | size }}
```

점 표기법 사용:

```liquid
{% raw %}
{% if site.pages.size > 10 %}
  This is a big website!
{% endif %}
{% endraw %}
```
