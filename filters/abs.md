---
title: abs
description: 절대값을 얻기 위한 Liquid 필터
---

숫자의 절대값을 리턴합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ -17 | abs }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
17
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ 4 | abs }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
4
```

`abs` will also work on a string if the string only contains a number.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "-19.86" | abs }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
19.86
```
