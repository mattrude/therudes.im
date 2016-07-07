---
layout: default
title: Generic Configuration
permalink: /help/generic-configuration/
---

This article provides the general configuration instructions for the {{ site.xmpp-url }} instant messaging service.

Every Jabber client has a different method of configuration. Our recommended and supported IM client is Spark, which you can download. To configure a client on your own (perhaps to take advantage of a client that also supports AIM, such as GAIM or Adium), here is the generic information you'll need:

* Protocol: Jabber/XMPP. You must use a client which supports this standard. A fairly exhaustive list of such clients can be found on the Jabber.org home page.
* Servername: `{{ site.xmpp-url }}`
* Port: 5222
* SSL: On. If if offers "STARTTLS" support, choose that; otherwise, just make sure it's trying to connect securely.

Some clients hide the "SSL" option. Some automatically change the port to 5223 when you turn on SSL; others don't. Both of these are things to watch out for. (Some clients also handle SSL negatively -- there'll be a box for "allow plain-text transmission" or the like that must be unchecked.)

On first login, you will of course be asked for a login name. This will probably take the form of `username@{{ site.xmpp-url }}`, using your own username, of course.

Some clients may require you to specify a full IM address when you're adding someone to your Contact list. This will take the form of `username@{{ site.xmpp-url }}`. Most clients will also let you give a nickname to your contacts when you add them, so you don't have to see the whole address all the time.

If you want to access a chat room, you may need to specify the chat room server. It's `{{ site.xmpp-conference-url }}`. The generic address of a chat room is `chatroom-name@{{ site.xmpp-conference-url }}`. Note that the "real" name of a chat room cannot have spaces, but you can specify a nickname or description which some clients will display in lieu of the real name -- this can cause some confusion.

Please see the page [Using Conferences]({{ site.url }}/help/using-conferences/) for more infromation on how to connect and use the confrencing service.
