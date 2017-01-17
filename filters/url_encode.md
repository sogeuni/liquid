---
title: url_encode
description: URL에서 사용할 수 없는 문자열을 인코딩하는 Liquid 필터.
---

문자열 내의 URL에서 사용할 수 없는 문자를 %형태의 문자로 인코딩합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "john@liquid.com" | url_encode }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ "john@liquid.com" | url_encode }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "Tetsuro Takara" | url_encode }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ "Tetsuro Takara" | url_encode }}
```
