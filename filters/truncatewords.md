---
title: truncatewords
description: 문자열에서 주어진 갯수의 단어를 잘라내는 Liquid 필터.
---

문자열을 인자로 전달된 단어 수만큼 줄입니다. 지정된 단어 갯수가 문장의 단어 갯수보다 작다면 문자열 뒤에 말줄임표(...)가 붙습니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "Ground control to Major Tom." | truncatewords: 3 }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ "Ground control to Major Tom." | truncatewords: 3 }}
```

### 말줄임표 사용자정의

`truncatewords`에 두 번째 인자는 옵션으로 생략된 문자열에 덧붙이는 말줄임표 문자열을 지정합니다. 기본값은 ... 이지만 다른 문자열로 변경할 수 있습니다.

<p class="code-label">입력</p>
{% raw %}
``` liquid
{{ "Ground control to Major Tom." | truncatewords: 3, "--" }}
```
{% endraw %}

<p class="code-label">결과</p>
``` text
{{ "Ground control to Major Tom." | truncatewords: 3, "--" }}
```

### 말줄임표 없애기

두 번째 인자로 빈문자열을 넘기면 뒤에 붙는 말줄임표를 없앨 수 있습니다:

<p class="code-label">입력</p>
{% raw %}
``` liquid
{{ "Ground control to Major Tom." | truncatewords: 3, "" }}
```
{% endraw %}

<p class="code-label">결과</p>
``` text
{{ "Ground control to Major Tom." | truncatewords: 3, "" }}
```
