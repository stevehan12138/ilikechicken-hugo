---
title: "How to strip html tags in Django"
draft: false
---

Many times, you would want to strip the html tags away from a string and only leave plain text. This can be accomplished by using libraries such as BeautifulSoup, but it can also be accomplished using regex:

```
String target = someString.replaceAll("<[^>]*>", "");
Syntax can be different depending on the language, but it should look something like that.
```

Django already has a built-in function for this. It uses regex as well for less hassle.

```
from django.utils.html import strip_tags
strip_tags(string)
```