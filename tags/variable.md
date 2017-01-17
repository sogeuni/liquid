---
title: 변수
description: Liquid 템플릿 언어에서 변수를 생성하기 위한 태그에 대한 개요
---

변수 태그는 새로운 Liquid 변수를 생성합니다.

## assign

새로운 변수를 생성합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign my_variable = false %}
{% if my_variable != true %}
  This statement is valid.
{% endif %}
{% endraw %}
```

<p class="code-label">결과</p>
```text
  This statement is valid.
```

변수 값을 따옴표`"`로 감싸면 문자열로 저장됩니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign foo = "bar" %}
{{ foo }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
bar
```

## capture

여는 태그과 닫는 태그 사이의 문자열을 캡쳐하여 그 값을 변수에 할당합니다. `{% raw %}{% capture %}{% endraw %}`를 통해 생성된 변수는 문자열입니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% capture my_variable %}I am being captured.{% endcapture %}
{{ my_variable }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
I am being captured.
```

## increment

새로운 숫자 변수를 생성하며, 매번 호출시 이 값은 1씩 증가합니다. 초기값은 0입니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% increment my_counter %}
{% increment my_counter %}
{% increment my_counter %}
{% endraw %}
```

<p class="code-label">결과</p>
```text
0
1
2
```

`increment` 태그를 통해 생성된 변수는 `assign` 또는 `capture`를 통해 생성된 변수와는 독립적입니다.

아래의 예제에서 `assign`을 통해 생성된 "var"라는 이름의 변수가 있습니다. 그리고 동일한 이름으로 `increment` 태그를 여러번 사용하였습니다. `increment` 태그는 `assign`으로 생성한 "var"의 값에는 영향을 미치지 않음에 유의하세요.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% assign var = 10 %}
{% increment var %}
{% increment var %}
{% increment var %}
{{ var }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
0
1
2
10
```

## decrement

새로운 숫자 변수를 생성하며, 매번 호출시 이 값은 1씩 감소합니다. 초기값은 -1입니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% decrement variable %}
{% decrement variable %}
{% decrement variable %}
{% endraw %}
```

<p class="code-label">결과</p>
```text
-1
-2
-3
```

[increment](#increment)와 같이, `decrement`로 선언된 변수는 `assign` 또는 `capture`를 통행 생성된 변수와는 독립적입니다.