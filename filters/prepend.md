---
title: prepend
description: 문자열의 시작 부분에 다른 문자열을 추가하는 Liquid 필터.
---

문자열의 시작에 다른 문자열을 추가합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "apples, oranges, and bananas" | prepend: "Some fruit: " }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ "apples, oranges, and bananas" | prepend: "Some fruit: " }}
```

`prepend`는 변수를 사용할 수도 있습니다:

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign url = "liquidmarkup.com" %}

{{ "/index.html" | prepend: url }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{% assign url = "liquidmarkup.com" %}

{{ "/index.html" | prepend: url }}
```
