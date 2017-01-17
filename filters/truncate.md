---
title: truncate
description: 문자열에서 주어진 갯수의 문자를 잘라내는 Liquid 필터.
---

`truncate`는 인자로 넘어온 문자 갯수만큼 문자열을 줄입니다. 지정된 문자 갯수가 문자열의 길이보다 작다면 문자열에 말줄임표(...)가 추가되고 이것은 문자 갯수에 포함됩니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "Ground control to Major Tom." | truncate: 20 }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ "Ground control to Major Tom." | truncate: 20 }}
```

### 말줄임표 사용자정의

`truncate`에 두 번째 인자는 옵션으로 생략된 문자열에 덧붙이는 말줄임표 문자열을 지정합니다. 기본값은 ... 이지만 다른 문자열로 변경할 수 있습니다.

두 번째 인자의 길이는 첫 번째 인자에 지정된 문자수에 포함됩니다. 예를 들어 문자열을 정확히 10자로 자르기를 원하고 말줄임표를 3자를 사용한다면 `truncate`의 첫 번째 인자는 말줄임표 3자를 포함하여 **13**으로 지정하여야 합니다.

<p class="code-label">입력</p>
{% raw %}
``` liquid
{{ "Ground control to Major Tom." | truncate: 25, ", and so on" }}
```
{% endraw %}

<p class="code-label">결과</p>
``` text
{{ "Ground control to Major Tom." | truncate: 25, ", and so on" }}
```

### 말줄임표 없애기

두 번째 인자에 빈 문자열을 넣어 첫 번째 인자에 넣은 갯수만큼 문자열을 정확히 자를 수 있습니다:

<p class="code-label">입력</p>
{% raw %}
``` liquid
{{ "Ground control to Major Tom." | truncate: 20, "" }}
```
{% endraw %}

<p class="code-label">결과</p>
``` text
{{ "Ground control to Major Tom." | truncate: 20, "" }}
```
