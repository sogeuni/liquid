---
title: date
description: 날짜의 서식을 지정하고 출력할 수 있는 Liquid 필터
---

타임스탬프를 다른 날짜 포맷으로 변환합니다. 이 구문의 형식은 [`strftime`](http://strftime.net)과 동일합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ article.published_at | date: "%a, %b %d, %y" }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
Fri, Jul 17, 15
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ article.published_at | date: "%Y" }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
2015
```

`date`는 제대로 된 날짜형식을 가지는 문자열에서도 동작합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "March 14, 2016" | date: "%b %d, %y" }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ "March 14, 2016" | date: "%b %d, %y" }}
```

현재 시간을 얻으려면 `date`에 특수 단어인 `"now"` (또는 `"today"`)를 넘깁니다:

<p class="code-label">입력</p>
```liquid
{% raw %}
This page was last updated at {{ "now" | date: "%Y-%m-%d %H:%M" }}.
{% endraw %}
```

<p class="code-label">결과</p>
```text
This page was last updated at {{ "now" | date: "%Y-%m-%d %H:%M" }}.
```

현재 시간은 사용자에게 페이지가 표시되는 시점이 아니라 템플릿으로 부터 마지막으로 페이지가 생성된 시간임에 유의하세요.
