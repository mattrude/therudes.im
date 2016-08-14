---
layout: default
title: Using Conferences
permalink: /help/using-conferences/
---

{% if site.xmpp-conference-url and site.xep-0045 == 1 %}
## Connecting from a federated XMPP server

By default the server will try to use [TLS]({{ site.url }}/help/definitions/#tls) if the other side supports it, and fall back to [dialback]({{ site.url }}/help/definitions/#dialback) if it does not or if the certificate is incorrect or not trusted.

{% if site.fingerprints == 1 %}
## Certificate Fingerprints

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
{% else %}
This server dose not support conferences, sorry.
{% endif %}
