---
title: compact
description: 배열에서 nil 값을 제거하는 Liquid 필터
---

배열에서 모든 `nil` 값을 제거합니다.

예를 들어 `site.pages`는 웹사이트 컨텐츠 페이지의 배열이고 이들 중 일부 페이지는 `category`라고 불리는 자신만의 특정 카테고리 속성을 가진다고 할 때, 카테고리들을 배열에 `map`한다면 `category` 속성을 가지지 않는 페이지 때문에 배열 항목의 일부에 `nil`이 추가될 수 있습니다.

<p class="code-label">입력</p>
{% raw %}
```liquid
{% assign site_categories = site.pages | map: 'category' %}

{% for category in site_categories %}
  {{ category }}
{% endfor %}
```
{% endraw %}

<p class="code-label">결과</p>
```text
  business
  celebrities

  lifestyle
  sports

  technology
```

`site_categories` 배열을 만들 때 `compact`를 사용하여 배열 내의 모든 `nil` 값을 제거할 수 있습니다.

<p class="code-label">입력</p>
{% raw %}
```liquid
{% assign site_categories = site.pages | map: 'category' | compact %}

{% for category in site_categories %}
  {{ category }}
{% endfor %}
```
{% endraw %}

<p class="code-label">결과</p>
```text
  business
  celebrities
  lifestyle
  sports
  technology
```
