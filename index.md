---
layout: default
title: Home
permalink: /
---

This is the **Rude Family's** communication services website.  This site is here to provide basic infromation on using this service.  A [XMPP]({{ site.url }}/doc/definitions/#xmpp-server) service provides messaging ability via a local client.  By using this service, security in increased due to the settings and the fact this service is owned and ran by the users.

## How to use the service

This service requires the use of a client to connect to the server with.  Please see the [client list]({{ site.url }}/doc/client-list/) for a small list of available clients that may be used.  My personal preferred clients is [Swift](http://swift.im/) for desktop/laptops and [ChatSecure](https://guardianproject.info/apps/chatsecure/) for mobile.

## Services Provided

### Confrence Rooms

This service provides confrence rooms via the mulit-user chats (MUC) interface documented in [XEP-0045](http://xmpp.org/extensions/xep-0045.html).  The confrence room service allows multiple users to join the same chat room or session at once and enabling all users in that room to comunicate freely.  Users may connect to these chat rooms via other [federated]({{ site.url }}/doc/definitions/#federation) XMPP servers, but only members of this server may create new rooms.

The confrence services URL is `conference.therudes.com`, the fingerprints are listed below.

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
			<th>therudes.com <small> - SHA1 Fingerprint</small></th>
		</tr>
    </thead>
    <tr>
		<td><code>BD:32:61:05:5D:F2:1D:FC:9E:40:74:29:CC:37:98:60:B5:C6:7C:8B</code></td>
	</tr>
    <thead>
		<tr>
			<th>therudes.com <small> - SHA256 Fingerprint</small></th>
		</tr>
	</thead>
    <tr>
        <td><code>C3:0E:A2:BF:1E:C5:C4:DD:E9:BE:10:1D:A1:F6:79:34:7C:FD:4A:CF:7F:73:22:16:CA:DC:F5:4C:59:A7:F8:1D</code></td>
    </tr>
    <thead>
    	<tr>
        	<th>conference.therudes.com <small> - SHA1 Fingerprint</small></th>
    	</tr>
    </thead>
    <tr>
        <td><code>35:3E:7B:63:89:B3:C6:6D:D7:32:70:C6:8B:27:92:A6:74:1C:98:96</code></td>
    </tr>
    <thead>
    	<tr>
        	<th>conference.therudes.com <small> - SHA256 Fingerprint</small></th>
        </tr>
    </thead>
    <tr>
        <td><code>8F:54:F8:8B:C1:52:C3:40:E6:47:94:9D:DA:1E:1E:51:E5:92:FC:9F:79:A8:E3:2D:2E:84:1D:FC:F2:8B:7A:AD</code></td>
    </tr>
</table>

<a href='https://xmpp.net/result.php?domain=therudes.com&amp;type=client'><img src='https://xmpp.net/badge.php?domain=therudes.com' alt='xmpp.net score' /></a>
