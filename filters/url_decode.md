---
title: url_decode
description: 퍼센트 인코딩된 문자열을 디코딩하는 Liquid 필터.
---

URL 혹은 [`url_encode`]({{ '/filters/url_encode' | prepend: site.baseurl }})로 인코딩된 문자열을 디코딩합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "%27Stop%21%27+said+Fred" | url_decode }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
'Stop!' said Fred
```
