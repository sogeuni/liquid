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

문자열 내에 숫자만 있다면 `abs`는 문자열에서도 동작합니다.

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
