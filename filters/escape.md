---
title: escape
description: 문자열에서 URL에 안전하지 않은 문자을 이스케이프 처리하는 Liquid 필터.
---

문자열의 문자를 이스케이프 시퀀스로 변환합니다(따라서 URL에서 사용할 수 있게 됩니다). 이스케이프할 문자가 없으면 문자열을 변환하지 않습니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "Have you read 'James & the Giant Peach'?" | escape }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ "Have you read 'James & the Giant Peach'?" | escape }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "Tetsuro Takara" | escape }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ "Tetsuro Takara" | escape }}
```
