---
title: strip_newlines
description: 문자열에서 줄바꿈 문자를 제거하는 Liquid 필터.
---

문자열의 모든 줄바꿈 문자(line breaks)를 제거합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% capture string_with_newlines %}
Hello
there
{% endcapture %}

{{ string_with_newlines | strip_newlines }}
{% endraw %}
```

<p class="code-label">결과</p>
```html
{% capture string_with_newlines %}
Hello
there
{% endcapture %}

{{ string_with_newlines | strip_newlines }}
```
