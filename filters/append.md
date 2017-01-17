---
title: append
description: 문자열에 다른 문자열을 추가하는 Liquid 필터
---

두 개의 문자열을 연결하고 연결된 값을 리턴합니다. 

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "/my/fancy/url" | append: ".html" }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ "/my/fancy/url" | append: ".html" }}
```

`append`는 변수에도 사용할 수 있습니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign filename = "/index.html" %}
{{ "website.com" | append: filename }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{% assign filename = "/index.html" %}
{{ "website.com" | append: filename }}
```
