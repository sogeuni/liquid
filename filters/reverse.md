---
title: reverse
description: 배열이나 문자열을 뒤집어서 배열로 변환하는 Liquid 필터.
---

배열의 아이템의 순서를 반대로 바꿉니다. `reverse`는 문자열을 뒤집지는 못합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign my_array = "apples, oranges, peaches, plums" | split: ", " %}

{{ my_array | reverse | join: ", " }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{% assign my_array = "apples, oranges, peaches, plums" | split: ", " %}

{{ my_array | reverse | join: ", " }}
```

`reverse`는 문자열에 직접 사용할 수 없지만 문자열을 배열로 나누어 배열을 뒤집은 다음, 필터를 연결하여 다시 결합할 수 있습니다:

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "Ground control to Major Tom." | split: "" | reverse | join: "" }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ "Ground control to Major Tom." | split: "" | reverse | join: "" }}
```
