---
title: escape_once
description: 문자열에서 URL에 안전하지 않은 문자을 이스케이프 처리하는 Liquid 필터.
---

이미 이스케이프 된 기존 엔터티를 변경하지 않고 문자열을 이스케이프 처리합니다. 이스케이프 할 것이 없는 문자열은 변경되지 않습니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "1 < 2 & 3" | escape_once }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ "1 < 2 & 3" | escape_once }}
```

<p class="code-label">입력</p>
```liquid
{% raw %}
{{ "1 &lt; 2 &amp; 3" | escape_once }}
{% endraw %}
```

<p class="code-label">결과</p>
```text
{{ "1 &lt; 2 &amp; 3" | escape_once }}
```
