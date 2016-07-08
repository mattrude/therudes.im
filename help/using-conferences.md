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
