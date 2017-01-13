---
title: 데이터 타입
description: Liquid 템플릿 언어의 데이터 타입에 대한 개요
---

Liquid 객체는 다음 5가지 타입 중 하나를 가질 수 있습니다.

- [String](#string)
- [Number](#number)
- [Boolean](#boolean)
- [Nil](#nil)
- [Array](#array)

Liquid 변수는 [assign]({{ "/tags/variable/#assign" | prepend: site.baseurl }})이나 [capture]({{ "/tags/variable/#capture" | prepend: site.baseurl }}) 태그를 이용하여 초기화 할 수 있습니다.

## 문자열(String)

변수의 값을 작은 따옴표나 큰 따옴표로 묶어 문자열을 선언합니다:

```liquid
{% raw %}
{% assign my_string = "Hello World!" %}
{% endraw %}
```

## 숫자(Number)

숫자는 정수형과 실수형을 포함합니다:

```liquid
{% raw %}
{% assign my_int = 25 %}
{% assign my_float = 39.756 %}
{% endraw %}
```

## Boolean

불리언은 `true` 혹은 `false` 입니다. 불리언 값을 선언할 때는 따옴표가 필요없습니다:

```liquid
{% raw %}
{% assign foo = true %}
{% assign bar = false %}
{% endraw %}
```

## Nil

Nil은 Liquid 코드의 결과가 없을 때 리턴하는 특수한 빈 값입니다. 이것은 문자열 "nil"이 **아닙니다**.

Nil은 `if` 블록의 조건문과 다른 체크 구문의 태그에서 [false로 간주]({{ "/basics/truthy-and-falsy" | prepend: site.baseurl }})합니다.

다음 예제에서 user가 존재하지 않으면(`user`가 `nil`을 리턴하면), Liquid는 인사말을 출력하지 않습니다.

```liquid
{% raw %}
{% if user %}
  Hello {{ user.name }}!
{% endif %}
{% endraw %}
```

`nil`을 리턴하는 태그 또는 결과는 페이지에 어떤 것도 출력하지 않습니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
The current user is {{ user.name }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
The current user is
```

## 배열(Array)

배열은 특정 타입의 변수의 리스트를 가집니다.

### 배열의 아이템에 접근하기

[반복 태그]({{ "/tags/iteration" | prepend: site.baseurl }})를 사용하여 배열의 각 항목들에 대해 반복해서 모두 접근이 가능합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
<!-- if site.users = "Tobi", "Laura", "Tetsuro", "Adam" -->
{% for user in site.users %}
  {{ user }}
{% endfor %}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{% raw %}
Tobi Laura Tetsuro Adam
{% endraw %}
```

### 배열의 특정 아이템에 접근하기

대괄호 `[` `]` 표기를 사용해서 배열의 특정 아이템에 접근할 수 있습니다. 배열의 인덱스는 0부터 시작합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
<!-- if site.users = "Tobi", "Laura", "Tetsuro", "Adam" -->
{{ site.users[0] }}
{{ site.users[1] }}
{{ site.users[3] }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
Tobi
Laura
Adam
```

### 배열의 초기화

Liquid만 사용해서 배열을 초기화 할 수는 없습니다.

하지만, [split]({{ "/filters/split" | prepend: site.baseurl }}) 필터를 사용하여 문자열을 서브스트링의 배열로 만들 수 있습니다.