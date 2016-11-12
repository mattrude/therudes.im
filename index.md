---
layout: default
title: Home
permalink: /
---

This is the **{{ site.name }}** communication service website.  This site is here to provide basic infromation on using this service.  A [XMPP]({{ site.url }}/help/definitions/#xmpp-server) service provides messaging ability via a local client.  By using this service, security in increased due to the settings and the fact this service is owned and ran by the users.{% if site.xep-0375 == 1%}  This service is in complete compliance with [XEP-0375](https://xmpp.org/extensions/xep-0375.html). The XEP-0375 document specifies the 2016 compliance levels for XMPP clients and servers.{% endif %}

## How to use the service

This service requires the use of a client to connect to the server with.  Please see the [client list]({{ site.url }}/help/client-list/) for a small list of available clients that may be used.  My personal preferred clients is [Swift](http://swift.im/) for desktop/laptops and [ChatSecure](https://guardianproject.info/apps/chatsecure/) for mobile.

## Connecting

* Hostname: <b>{{ site.xmpp-url }}</b>
* Port: <b>5222</b>{% if site.xmpp-conference-url and site.xep-0045 == 1 %}
* Conference Rooms: <b>{{ site.xmpp-conference-url }}</b>{% endif %}{% if site.xmpp-proxy-url %}
* Socks 5 Proxy: <b>{{ site.xmpp-proxy-url }}</b>{% endif %}

## Services Provided

{% if site.xmpp-conference-url and site.xep-0045 == 1 %}
### Conference Rooms

This service provides conference rooms via the mulit-user chats (MUC) interface documented in [XEP-0045](http://xmpp.org/extensions/xep-0045.html).  The conference room service allows multiple users to join the same chat room or session at once and enabling all users in that room to comunicate freely.  Users may connect to these chat rooms via other [federated]({{ site.url }}/help/definitions/#federation) XMPP servers, but only members of this server may create new rooms.

The conference services URL is `{{ site.xmpp-conference-url }}`, the fingerprints are [listed below]({{ site.url }}/#certificates-fingerprints).

Please see the page [Using Conferences]({{ site.url }}/help/using-conferences/) for more infromation on how to connect and use the conferencing service.
{% endif %}

{% if site.xep-0191 == 1 %}
### Privacy Lists

Privacy Lists provide a method for a user to block the receipt of messages (and packets), from a specific user or group of users.  Using the protocal layed out in [XEP-0191](https://xmpp.org/extensions/xep-0191.html) and [XEP-0016](https://xmpp.org/extensions/xep-0016.html), and depending on the client used, a user may block a [JID]({{ site.url }}/help/definitions/#jid) or a [domain]({{ site.url }}/help/definitions/#domain).
{% endif %}

### Offline Storage

Offline Storage allows for the storage of offline messages to disk, ready to be delivered to users when the next log in.  This is implement using [XEP-0160](http://xmpp.org/extensions/xep-0160.html), [XEP-0203](http://xmpp.org/extensions/xep-0203.html) and [XEP-0091](http://xmpp.org/extensions/xep-0091.html) for backwards compatibility with older clients.

{% if site.xep-0313 == 1 %}
### Message Archive Management

It is a common desire for users of XMPP to want to store their messages in a central archive on their server. This feature allows them to record conversations that take place on clients that do not support local history storage, to synchronise conversation history seamlessly between multiple clients, to read the history of a MUC room, or to view old items in a pubsub node.

{% endif %}

### vCards

vCards are a online version of a business card, as implemented in [XEP-0054](http://xmpp.org/extensions/xep-0054.html). Users are not required to fill in a vCard and can supply as much or as little as they like.

### Compression

While the bandwidth usage of XMPP isn't great, compressing the data sent to/from your server can give significant benefits to those on slow connections, such as dial-up or mobile networks.

Compression is enabled via [mod_compression](https://prosody.im/doc/modules/mod_compression) that implements [XEP-0138](http://xmpp.org/extensions/xep-0138.html), and supports the zlib compression algorithm.

{% if site.xep-0357 == 1 %}
### Push Notifications

The purpose of push notifications ([XEP-0357](https://xmpp.org/extensions/xep-0357.html)) is to inform users of new messages or other pertinent information even when they have no XMPP clients online.

Typically, these notifications are delivered to a user's mobile device, displaying a notice that can trigger opening an XMPP client to continue a conversation or answer a Jingle session request.

{% endif %}

{% if site.xep-0065 == 1 %}
### File Transfer

File Transfer ([XEP-0065](https://xmpp.org/extensions/xep-0065.html)) allows the server to proxy file transfers between 2 clients that are behind NAT routers or firewalls, and otherwise wouldn't be able to transfer files.

{% endif %}

### Web Presence

Web Presence provides the status of a user via a image URL.  Please see the page [Web Presence]({{ site.url }}/help/web-presence/) for more infromation on how to use the web presence service.

## Security

* SSL/TLS encryption is [required](https://github.com/stpeter/manifesto/blob/master/manifesto.txt) between clients and servers (C2S) and server to server (S2S) connections
* The backend is configured to store hashed and salted authentication data
* Use Off-the-Record (OTR) in your chat client to have fully encrypted chats

{% if site.fingerprints == 1 %}
### Certificates Fingerprints

One of the benefits of communicating via XMPP is the level of security involved.  To allow users to validate the servers they are connecting to, below is the current fingerprints for each domain name.

<div id="cert-table">
{% if site.fingerprint-sha1 %}
  <div class="cert-title">
    <b>{{ site.xmpp-url }}<small> - SHA1 Fingerprint</small></b>
  </div>
  <div class="cert-content">
    <pre>{{ site.fingerprint-sha1 }}</pre>
  </div>
{% endif %}
{% if site.fingerprint-sha256 %}
  <div class="cert-title">
    <b>{{ site.xmpp-url }}<small> - SHA256 Fingerprint</small></b>
  </div>
  <div class="cert-content">
    <pre>{{ site.fingerprint-sha256 }}</pre>
  </div>
{% endif %}
{% if site.fingerprint-conference-sha1 %}
  <div class="cert-title">
    <b>{{ site.xmpp-conference-url }}<small> - SHA1 Fingerprint</small></b>
  </div>
  <div class="cert-content">
    <pre>{{ site.fingerprint-conference-sha1 }}</pre>
  </div>
{% endif %}
{% if site.fingerprint-conference-sha256 %}
  <div class="cert-title">
    <b>{{ site.xmpp-conference-url }}<small> - SHA256 Fingerprint</small></b>
  </div>
  <div class="cert-content">
    <pre>{{ site.fingerprint-conference-sha256 }}</pre>
  </div>
{% endif %}
</div> <!-- Closing cert-table id div -->
{% endif %}

<p style='text-align:right;'><a href="https://xmpp.net/result.php?domain={{ site.xmpp-url }}&amp;type=server"><img src="https://xmpp.net/badge.php?domain={{ site.xmpp-url }}" alt="xmpp.net score" /></a></p>

## Policies

No more information is collected and stored than what is absolutely necessary. This includes rosters, vCards, offline messages, etc.

Spam and abuse including advertisements of any kind will not be tolerated on this network. For spam or abuse please contact us with the full details.
