---
layout: default
title: Web Presence
permalink: /help/web-presence/
---
Web Presence provides the status of a user via a image URL.  It is enabled by default for all users, but may be disabled.

### Using Web Presence Image

To use web presence, just add the below image url to a site or email.  The userid entry is your userid or the left part after the `@` sign of your [JID]({{ site.url }}/help/definitions/#jid).  So if your JID is `odin@{{ site.xmpp-url }}` then your userid will be `odin`.

    <img src="{{ site.url }}/status/userid" />

* ![online]({{ site.url }}/img/status_online.png) - User's current status is **online**
* ![status-chat]({{ site.url }}/img/status_chat.png) - User's current status is **free to chat**
* ![status-away]({{ site.url }}/img/status_away.png) - User's current status is **away**
* ![status-xa]({{ site.url }}/img/status_xa.png) - User's current status is **extended away**
* ![status-dnd]({{ site.url }}/img/status_dnd.png) - User's current status is **dnd** (do not disturb)
* ![offline]({{ site.url }}/img/status_offline.png) - User's current status is **offline**

### Web Presence Status text

Alternatively, it can be used to get status name as plaint text, status message as plain text or html-code for embedding on web-pages.

To get status name in plain text you can use something like the following link: `{{ site.url }}/status/userid/text`

To get status message as plain text you can use something like the following link: `{{ site.url }}/status/userid/message`

To get html code, containig status name, status image and status message (if set): `{{ site.url }}/status/userid/html`

To get json output, containig status name, status image and status message (if set): `{{ site.url }}/status/userid/json`
