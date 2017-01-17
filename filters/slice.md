---
title: slice
description: 문자열에서 주어진 위치의 하위문자열을 리턴하는 Liquid 필터.
---

문자열에서 지정된 위치의 한문자를 리턴합니다. 옵션으로 두 번째 인자는 리턴할 하위 문자의 갯수를 지정합니다.

문자열의 인덱스는 0부터 시작합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "Liquid" | slice: 0 }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ "Liquid" | slice: 0 }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "Liquid" | slice: 2 }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ "Liquid" | slice: 2 }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "Liquid" | slice: 2, 5 }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ "Liquid" | slice: 2, 5 }}
```

첫번째 인자가 음수라면 인덱스는 문자열의 끝부터 계산됩니다:

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "Liquid" | slice: -3, 2 }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ "Liquid" | slice: -3, 2 }}
```
