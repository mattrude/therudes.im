---
layout: default
title: Home
permalink: /
---

This is the **{{ site.name }}** communication services website.  This site is here to provide basic infromation on using this service.  A [XMPP]({{ site.url }}/help/definitions/#xmpp-server) service provides messaging ability via a local client.  By using this service, security in increased due to the settings and the fact this service is owned and ran by the users.

## How to use the service

This service requires the use of a client to connect to the server with.  Please see the [client list]({{ site.url }}/help/client-list/) for a small list of available clients that may be used.  My personal preferred clients is [Swift](http://swift.im/) for desktop/laptops and [ChatSecure](https://guardianproject.info/apps/chatsecure/) for mobile.

## Connecting

* Hostname: <b>{{ site.xmpp-url }}</b>
* Port: <b>5222</b>

## Services Provided

{% if site.xmpp-conference-url %}
### Confrence Rooms

This service provides confrence rooms via the mulit-user chats (MUC) interface documented in [XEP-0045](http://xmpp.org/extensions/xep-0045.html).  The confrence room service allows multiple users to join the same chat room or session at once and enabling all users in that room to comunicate freely.  Users may connect to these chat rooms via other [federated]({{ site.url }}/help/definitions/#federation) XMPP servers, but only members of this server may create new rooms.

The confrence services URL is `{{ site.xmpp-conference-url }}`, the fingerprints are [listed below]({{ site.url }}/#certificates-fingerprints).

Please see the page [Using Conferences]({{ site.url }}/help/using-conferences/) for more infromation on how to connect and use the confrencing service.
{% endif %}

### Web Presence

Web Presence provides the status of a user via a image URL.  Please see the page [Web Presence]({{ site.url }}/help/web-presence/) for more infromation on how to use the web presence service.

## Security

* SSL/TLS encryption is [required](https://github.com/stpeter/manifesto/blob/master/manifesto.txt) between clients and servers (C2S) and server to server (S2S) connections
* The backend is configured to store hashed and salted authentication data
* Use Off-the-Record (OTR) in your chat client to have fully encrypted chats

{% if site.fingerprints %}
### Certificates Fingerprints

One of the benefits of communicating via XMPP is the level of security involved.  To allow users to validate the servers they are connecting to, below is the current fingerprints for each domain name.

<div id="cert-table">
{% if site.fingerprint-sha1 %}
  <div class="cert-title">
    <b>{{ site.baseurl }}<small> - SHA1 Fingerprint</small></b>
  </div>
  <div class="cert-content">
    <pre>{{ site.fingerprint-sha1 }}</pre>
  </div>
{% endif %}
{% if site.fingerprint-sha256 %}
  <div class="cert-title">
    <b>{{ site.baseurl }}<small> - SHA256 Fingerprint</small></b>
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
