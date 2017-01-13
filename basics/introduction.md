---
title: 소개
description: Liquid 템플릿 언어의 객체와 태그 및 필터에 대한 개요
---

Liquid 코드는 [**객체**](#objects), [**태그**](#tags), 및 [**필터**](#filters)로 분류할 수 있습니다.

## 객체(Objects)

**객체**는 Liquid가 컨텐츠를 페이지의 어느 위치에 보여줄 지를 알려줍니다. 객체와 변수의 이름은 `{% raw %}{{{% endraw %}`와 `{% raw %}}}{% endraw %}` 같이 이중 중괄호로 표시합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ page.title }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
Introduction
```

이 경우, Liquid는 `page.title`이라 불리는 객체의 내용을 `Introduction`이라는 문자열로 렌더링합니다.

## 태그(Tags)

**태그**는 템플릿의 로직 및 제어 흐름을 생성합니다. 태그는 `{% raw %}{%{% endraw %}`와 `{% raw %}%}{% endraw %}` 같이 중괄호와 퍼센트 기호로 표시합니다.

태그 내에 사용된 마크업은 화면에 보이는 텍스트를 생성하지 않습니다. 즉, 변수를 선언하고 페이지에 Liquid 로직을 표시하지 않으면서 조건과 반복문을 만들 수 있습니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% if user %}
  Hello {{ user.name }}!
{% endif %}
{% endraw %}
```

<p class="code-label">결과</p>
```text
Hello Adam!
```

태그는 세 가지 유형으로 분류 할 수 있습니다:

- [제어 흐름(Control flow)]({{ "/tags/control-flow" | prepend: site.baseurl }})
- [반복(Iteration)]({{ "/tags/iteration" | prepend: site.baseurl }})
- [변수 선언(Variable assignments)]({{ "/tags/variable" | prepend: site.baseurl }})

각각의 섹션에서 각 태그 유형에 대한 자세한 내용을 확인할 수 있습니다.


## 필터(Filters)

**필터**는 Liquid 객체의 결과물을 변환홥니다. 필터는 결과물 내에서 사용되며 `|`로 구분합니다.

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
