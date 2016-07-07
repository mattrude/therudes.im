---
layout: default
title: Using Conferences
permalink: /help/using-conferences/
---

## Connecting from a federated XMPP server

By default the server will try to use [TLS]({{ site.url }}/help/definitions/#tls) if the other side supports it, and fall back to [dialback]({{ site.url }}/help/definitions/#dialback) if it does not or if the certificate is incorrect or not trusted.

## Certificate Fingerprints

One of the benefits of communicating via XMPP is the level of security involved.  To allow users to validate the servers they are connecting to, below is the current fingerprints for each domain name.

<table style="width:100%;">
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
