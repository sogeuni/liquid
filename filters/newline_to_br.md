---
title: newline_to_br
description: Liquid filter that converts newlines in an input string to HTML <br> tags.
---

Replaces every newline (`\n`) with an HTML line break (`<br>`).

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
