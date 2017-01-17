---
title: 반복
description: Liquid 템플릿 언어의 'loop' 태그나 반복에 대한 개요
---

반복 태그는 코드 블록을 반복적으로 실행합니다.

## for

코드 블록을 반복 실행합니다. `for` 루프 내에서 사용 가능한 전체 속성 목록은 [forloop (object)](https://docs.shopify.com/themes/liquid/objects/for-loops)를 참고하세요.

<p class="code-label">입력</p>
```liquid
{% raw %}
  {% for product in collection.products %}
    {{ product.title }}
  {% endfor %}
{% endraw %}
```

<p class="code-label">결과</p>
```text
hat shirt pants
```

### break

`break` 태그를 만나면 루프 반복을 중단합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% for i in (1..5) %}
  {% if i == 4 %}
    {% break %}
  {% else %}
    {{ i }}
  {% endif %}
{% endfor %}
{% endraw %}
```

<p class="code-label">결과</p>
```text
1 2 3
```

### continue

`continue` 태그를 만나면 현재 반복 중이던 구문을 건너뜁니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% for i in (1..5) %}
  {% if i == 4 %}
    {% continue %}
  {% else %}
    {{ i }}
  {% endif %}
{% endfor %}
{% endraw %}
```

<p class="code-label">결과</p>
```text
1 2 3   5
```

## for (파라미터)

### limit

지정된 반복횟수로 제한하여 루프를 실행합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
<!-- if array = [1,2,3,4,5,6] -->
{% for item in array limit:2 %}
  {{ item }}
{% endfor %}
{% endraw %}
```

<p class="code-label">결과</p>
```text
1 2
```

### offset

지정한 인덱스에서 루프를 시작합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
<!-- if array = [1,2,3,4,5,6] -->
{% for item in array offset:2 %}
  {{ item }}
{% endfor %}
{% endraw %}
```

<p class="code-label">결과</p>
```text
3 4 5 6
```

### range

반복할 숫자 범위를 지정합니다. 범위는 리터럴 및 변수로 정의할 수 있습니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% for i in (3..5) %}
  {{ i }}
{% endfor %}

{% assign num = 4 %}
{% for i in (1..num) %}
  {{ i }}
{% endfor %}
{% endraw %}
```

<p class="code-label">결과</p>
```text
3 4 5
1 2 3 4
```

### reversed

루프의 순서를 반대로 바꿉니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
<!-- if array = [1,2,3,4,5,6] -->
{% for item in array reversed %}
  {{ item }}
{% endfor %}
{% endraw %}
```

<p class="code-label">결과</p>
```text
6 5 4 3 2 1
```

## cycle

문자열 그룹을 순환하여 순서대로 파리미터로 전달합니다. `cycle`이 호출될 때 마다 다음 문자열이 파리미터로 전달되어 출력됩니다.

`cycle`은 [for](#for) 블록 내에서만 사용 가능 합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% cycle 'one', 'two', 'three' %}
{% cycle 'one', 'two', 'three' %}
{% cycle 'one', 'two', 'three' %}
{% cycle 'one', 'two', 'three' %}
{% endraw %}
```

<p class="code-label">결과</p>
```text
one
two
three
one
```

`cycle`은 다음과 같은 경우에 사용합니다:

-   테이블의 행에 짝/홀수 클래스를 적용할 때
-   행의 마지막 제품 썸네일에 유니크한 클래스를 적용할 때

## cycle (파라미터)

하나의 템플릿에 여러개의 `cycle` 블록이 필요한 경우 `cycle group`이라고 하는 파라미터를 사용합니다. cycle group에 이름이 없다면 동일한 파라미터가 있는 여러 호출을 하나의 그룹으로 간주합니다.

## tablerow

HTML 테이블을 생성합니다. 반드시 `<table>`과 `</table>` HTML 태그로 감싸야 합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
<table>
{% tablerow product in collection.products %}
  {{ product.title }}
{% endtablerow %}
</table>
{% endraw %}
```

<p class="code-label">결과</p>
```html
<table>
  <tr class="row1">
    <td class="col1">
      Cool Shirt
    </td>
    <td class="col2">
      Alien Poster
    </td>
    <td class="col3">
      Batman Poster
    </td>
    <td class="col4">
      Bullseye Shirt
    </td>
    <td class="col5">
      Another Classic Vinyl
    </td>
    <td class="col6">
      Awesome Jeans
    </td>
  </tr>
</table>
```

## tablerow (파라미터)

### cols

테이블의 column 수를 정의합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% tablerow product in collection.products cols:2 %}
  {{ product.title }}
{% endtablerow %}
{% endraw %}
```

<p class="code-label">결과</p>
```html
<table>
  <tr class="row1">
    <td class="col1">
      Cool Shirt
    </td>
    <td class="col2">
      Alien Poster
    </td>
  </tr>
  <tr class="row2">
    <td class="col1">
      Batman Poster
    </td>
    <td class="col2">
      Bullseye Shirt
    </td>
  </tr>
  <tr class="row3">
    <td class="col1">
      Another Classic Vinyl
    </td>
    <td class="col2">
      Awesome Jeans
    </td>
  </tr>
</table>
```

#### limit

특정 인덱스 이후에 tablerow를 종료합니다.

```liquid
{% raw %}
{% tablerow product in collection.products cols:2 limit:3 %}
  {{ product.title }}
{% endtablerow %}
{% endraw %}
```

### offset

특정 인덱스 이후에 tablerow를 시작합니다.

```liquid
{% raw %}
{% tablerow product in collection.products cols:2 offset:3 %}
  {{ product.title }}
{% endtablerow %}
{% endraw %}
```

### range

반복 할 숫자 범위를 정의합니다. 범위는 리터럴과 변수값이 가능합니다.

```liquid
{% raw %}
<!--variable number example-->

{% assign num = 4 %}
<table>
{% tablerow i in (1..num) %}
  {{ i }}
{% endtablerow %}
</table>

<!--literal number example-->

<table>
{% tablerow i in (3..5) %}
  {{ i }}
{% endtablerow %}
</table>
{% endraw %}
```
