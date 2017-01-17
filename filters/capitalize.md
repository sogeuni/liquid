---
title: capitalize
description: 문자열의 첫번째 문자를 대문자화하는 Liquid 필터
---

문자열의 첫번째 문자를 대문자로 변환합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "title" | capitalize }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
Title
```

`capitalize`는 문자열의 첫 문자만 대문자로 변환하므로 다른 단어에는 영향을 미치지 않습니다:

 <p class="code-label">입력</p>
```liquid
{% raw %}
{{ "my great title" | capitalize }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
My great title
```
