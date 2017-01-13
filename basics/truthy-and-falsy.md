---
title: 참과 거짓
description: Liquid 템플릿 언어에서 불리인 로직에 대한 개요
---

프로그래밍에서는 **참**인 조건에서 항상 `true`를 리턴합니다. 반대로 **거짓**인 조건에서는 항상 `false`를 리턴합니다. 모든 객체의 타입은 참이나 거짓으로 설명이 가능합니다.

- [참](#truthy)
- [거짓](#falsy)
- [요약](#summary)

<div id="truthy"></div>

## 참

Liquid에서 `nil`과 `false`를 제외한 모든 값은 참입니다.

아래 예제에서 "Tobi"라는 문자열은 boolean이 아니지만 조건식에서는 참인 조건이 됩니다:

```liquid
{% raw %}
{% assign tobi = "Tobi" %}

{% if tobi %}
  This condition will always be true.
{% endif %}
{% endraw %}
```

[문자열]({{ "/basics/types/#string" | prepend: site.baseurl }})이 비어 있어도 참입니다. 아래 예제는 `settings.fp_heading`이 비어있울 경우에 내용이 빈 HTML 태그가 됩니다:

<p class="code-label">입력</p>
```liquid
{% raw %}
{% if settings.fp_heading %}
  <h1>{{ settings.fp_heading }}</h1>
{% endif %}
{% endraw %}
```

<p class="code-label">결과</p>
```html
<h1></h1>
```
<div id="falsy"></div>

## 거짓

Liquid에서의 거짓값은 [`nil`]({{ "/basics/types/#nil" | prepend: site.baseurl }})과 [`false`]({{ "/basics/types/#boolean" | prepend: site.baseurl }}) 입니다.

<div id="summary"></div>

## 요약

다음 표는 Liquid에서의 참과 거짓에 대해 정리하고 있습니다.

|               | 참            | 거짓           |
| ------------- |:-------------:|:-------------:|
| true          | •             |               |
| false         |               | •             |
| nil           |               | •             |
| string        | •             |               |
| empty string  | •             |               |
| 0             | •             |               |
| integer       | •             |               |
| float         | •             |               |
| array         | •             |               |
| empty array   | •             |               |
| page          | •             |               |
| EmptyDrop     | •             |               |
