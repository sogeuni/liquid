---
title: strip_newlines
description: Liquid filter that removes newline characters from a string.
---

Removes any newline characters (line breaks) from a string.

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
