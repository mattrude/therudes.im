---
layout: default
title: Web Presence
permalink: /help/web-presence/
---

    <img src="{{ site.url }}/status/john.smith" />

Alternatively, it can be used to get status name as plaint text, status message as plain text or html-code for embedding on web-pages.

To get status name in plain text you can use something like that link: `{{ site.url }}/status/john.smith/text`

To get status message as plain text you can use something like following link: `{{ site.url }}/status/john.smith/message`

To get html code, containig status name, status image and status message (if set): `{{ site.url }}/status/john.smith/html`
