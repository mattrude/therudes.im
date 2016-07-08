---
layout: default
title: Home
permalink: /
---

This is the **Rude Family's** communication services website.  This site is here to provide basic infromation on using this service.  A [XMPP]({{ site.url }}/help/definitions/#xmpp-server) service provides messaging ability via a local client.  By using this service, security in increased due to the settings and the fact this service is owned and ran by the users.

## How to use the service

This service requires the use of a client to connect to the server with.  Please see the [client list]({{ site.url }}/help/client-list/) for a small list of available clients that may be used.  My personal preferred clients is [Swift](http://swift.im/) for desktop/laptops and [ChatSecure](https://guardianproject.info/apps/chatsecure/) for mobile.

## Services Provided

### Confrence Rooms

This service provides confrence rooms via the mulit-user chats (MUC) interface documented in [XEP-0045](http://xmpp.org/extensions/xep-0045.html).  The confrence room service allows multiple users to join the same chat room or session at once and enabling all users in that room to comunicate freely.  Users may connect to these chat rooms via other [federated]({{ site.url }}/help/definitions/#federation) XMPP servers, but only members of this server may create new rooms.

The confrence services URL is `{{ site.xmpp-conference-url }}`, the fingerprints are [listed below]({{ site.url }}/#certificates-fingerprints).

Please see the page [Using Conferences]({{ site.url }}/help/using-conferences/) for more infromation on how to connect and use the confrencing service.

### BOSH Service

[XEP-0124](http://xmpp.org/extensions/xep-0124.html)

### Web Presence

Web Presence provides the status of a user via a image URL.  Please see the page [Web Presence]({{ site.url }}/help/web-presence/) for more infromation on how to use the web presence service.

## Certificates Fingerprints

One of the benefits of communicating via XMPP is the level of security involved.  To allow users to validate the servers they are connecting to, below is the current fingerprints for each domain name.

<table style="width:100%;">
    <thead>
		<tr>
			<th>{{ site.xmpp-url }}<small> - SHA1 Fingerprint</small></th>
		</tr>
    </thead>
    <tr>
		<td><code>{{ site.fingerprint-sha1 }}</code></td>
	</tr>
    <thead>
		<tr>
			<th>{{ site.xmpp-url }}<small> - SHA256 Fingerprint</small></th>
		</tr>
	</thead>
    <tr>
        <td><code>{{ site.fingerprint-sha256 }}</code></td>
    </tr>
    <thead>
    	<tr>
        	<th>{{ site.xmpp-conference-url }}<small> - SHA1 Fingerprint</small></th>
    	</tr>
    </thead>
    <tr>
        <td><code>{{ site.fingerprint-conference-sha1 }}</code></td>
    </tr>
    <thead>
    	<tr>
        	<th>{{ site.xmpp-conference-url }}<small> - SHA256 Fingerprint</small></th>
        </tr>
    </thead>
    <tr>
        <td><code>{{ site.fingerprint-conference-sha256 }}</code></td>
    </tr>
</table>

<a href="https://xmpp.net/result.php?domain={{ site.xmpp-url }}&amp;type=client"><img src="https://xmpp.net/badge.php?domain={{ site.xmpp-url }}" alt="xmpp.net score" /></a>
