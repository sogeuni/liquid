---
title: 연산자
description: Liquid 템플릿 언어에서 연산자를 사용하여 계산을 수행합니다.
---

Liquid는 다양한 논리 연산자와 비교 연산자를 가지고 있습니다.

## 기본 연산자

<table>
  <tbody>
    <tr>
      <td><code>==</code></td>
      <td>일치함</td>
    </tr>
    <tr>
      <td><code>!=</code></td>
      <td>일치하지 않음</td>
    </tr>
    <tr>
      <td><code>&gt;</code></td>
      <td>초과</td>
    </tr>
    <tr>
      <td><code>&lt;</code></td>
      <td>미만</td>
    </tr>
    <tr>
      <td><code>&gt;=</code></td>
      <td>이상</td>
    </tr>
    <tr>
      <td><code>&lt;=</code></td>
      <td>이하</td>
    </tr>
    <tr>
      <td><code>or</code></td>
      <td>논리합</td>
    </tr>
    <tr>
      <td><code>and</code></td>
      <td>논리곱</td>
    </tr>
  </tbody>
</table>

예제:

```liquid
{% raw %}
{% if product.title == "Awesome Shoes" %}
  These shoes are awesome!
{% endif %}
{% endraw %}
```

태그 내에서 여러개의 연산자를 사용할 수 있습니다:

```liquid
{% raw %}
{% if product.type == "Shirt" or product.type == "Shoes" %}
  This is a shirt or a pair of shoes.
{% endif %}
{% endraw %}
```

## contains

`contains`는 문자열 안에 서브스트링이 있는지 검사합니다.

```liquid
{% raw %}
{% if product.title contains 'Pack' %}
  This product's title contains the word Pack.
{% endif %}
{% endraw %}
```

또한, `contains'는 문자열들을 가지는 배열에서 특정 문자열이 있는지를 검사할 수 있습니다.

```liquid
{% raw %}
{% if product.tags contains 'Hello' %}
  This product has been tagged with 'Hello'.
{% endif %}
{% endraw %}
```

`contains`는 문자열만 검색할 수 있습니다. 객체들을 가진 배열에서 객체를 찾는데 사용할 수는 없습니다.
