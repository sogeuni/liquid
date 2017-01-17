---
title: divided_by
description: 숫자를 다른 숫자로 나누는 Liquid 필터
---

숫자를 특정 숫자로 나눕니다.

정수로 나눈다면 결과는 가까운 정수로 내림합니다. (즉, [floor]({{ site.baseurl }}/filters/floor)) 

<p class="code-label">입력</p>
{% raw %}
``` liquid
{{ 16 | divided_by: 4 }}
```
{% endraw %}

<p class="code-label">결과</p>
``` text
{{ 16 | divided_by: 4 }}
```

<p class="code-label">입력</p>
{% raw %}
``` liquid
{{ 5 | divided_by: 3 }}
```
{% endraw %}

<p class="code-label">결과</p>
``` text
{{ 5 | divided_by: 3 }}
```

### 반올림 제어

`divided_by` 는 나누는 값과 동일한 타입의 결과를 생성합니다. — 즉, 정수로 나누면 결과는 정수가 되고, 실수로 나누면 결과는 실수가 됩니다.

예를 들어 나누는 수가 정수라면:

<p class="code-label">입력</p>
{% raw %}
``` liquid
{{ 20 | divided_by: 7 }}
```
{% endraw %}

<p class="code-label">결과</p>
``` text
{{ 20 | divided_by: 7 }}
```

실수일 경우에는:

<p class="code-label">입력</p>
{% raw %}
``` liquid
{{ 20 | divided_by: 7.0 }}
```
{% endraw %}

<p class="code-label">결과</p>
``` text
{{ 20 | divided_by: 7.0 }}
```

### 변수의 형 변환

변수를 나누는 수로 사용할 수도 있습니다. 이 경우 간단히 `.0`을 추가하여 부동소수점으로 변환할 수 있습니다. 이 경우 `times` 필터를 사용하여 변수을 부동소수점으로 변경한 값을 다른 변수에 `assign`할 수 있습니다.

이 예제에서는 정수값을 가지는 변수로 나누기 때문에 결과는 정수가 됩니다.

<p class="code-label">입력</p>
{% raw %}
``` liquid
{% assign my_integer = 7 %}
{{ 20 | divided_by: my_integer }}
```
{% endraw %}

<p class="code-label">결과</p>
``` text
{% assign my_integer = 7 %}
{{ 20 | divided_by: my_integer }}
```

이제 변수의 float 값을 얻기 위해 `1.0`을 [곱 한]({{ site.baseurl}}/filters/times)다음 float로 나눕니다:

<p class="code-label">입력</p>
{% raw %}
``` liquid
{% assign my_integer = 7 %}
{% assign my_float = my_integer | times: 1.0 %}
{{ 20 | divided_by: my_float }}
```
{% endraw %}

<p class="code-label">결과</p>
``` text
{% assign my_integer = 7 %}
{% assign my_float = my_integer | times: 1.0 %}
{{ 20 | divided_by: my_float }}
```
