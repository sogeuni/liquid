---
title: newline_to_br
description: 입력 문자열에서 줄바꿈을 HTML <br> 태그로 변환하는 Liquid 필터.
---

모든 줄바꿈(`\n`)을 HTML 줄바꿈(`<br>`)으로 변경합니다.

<p class="code-label">입력</p>
```liquid
{% raw %}
{% capture string_with_newlines %}
Hello
there
{% endcapture %}

{{ string_with_newlines | newline_to_br }}
{% endraw %}
```

<p class="code-label">결과</p>
```html
{% capture string_with_newlines %}
Hello
there
{% endcapture %}

{{ string_with_newlines | newline_to_br }}
```
