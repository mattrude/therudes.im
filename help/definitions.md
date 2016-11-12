---
layout: default
title: XMPP Definitions
permalink: /help/definitions/
---

## BOSH
<b>B</b>idirectional-streams <b>O</b>ver <b>S</b>ynchronous <b>H</b>TTP (BOSH) used to transport XMPP [stanzas](#stanza).  The result is an HTTP binding for XMPP communications that is useful in situations where a device or client is unable to maintain a long-lived [TCP](#tcp) connection to an XMPP server.

## Dialback

## Domain

## DNS

## Federation

<b>Federation</b> is the method used by XMPP servers to connect to other XMPP server to allow users from one server to chat with users on other server.

The following diagram provides a high-level overview of this architecture (where `-` represents communications that use XMPP and `=` represents communications that use any other protocol).

<pre><code>        C1
        |
   C2---S1---C3
        |
   C4---S2---G1===FN1===FC1
        |
        C5
</code></pre>

The symbols are as follows:

* C1, C2, C3, C4, C5 = XMPP clients
* S1, S2 = XMPP servers
* G1 = A gateway that translates between XMPP and the protocol(s) used on a foreign (non-XMPP) messaging network
* FN1 = A foreign messaging network
* FC1 = A client on a foreign messaging network

## Gateway

## IP Address

## Jabber

## JID
A users unique [XMPP](#xmpp-server) address, is called a JID (or for historical reasons, sometimes called a Jabber ID). The JID is structured like an email address with a username and a domain name (or [IP address](#ip-address)) for the server where that user resides, separated by an at sign `@`, such as username@example.com.

## LAN

## Presence

## Prosody

## SRV Records

## Stanza
A group of lines forming the basic recurring metrical unit in [XML](#xml); like a verse in a poem.

## TCP

## TLS

## Transports
One of the original design goals of the early Jabber open-source community was enabling users to connect to multiple non-XMPP messaging systems. This was done through *transports* or *gateways*.

## XEP

## XMPP Server
An XMPP server provides basic messaging, [presence](#presence), and XML routing features. This page lists Jabber/XMPP server software that you can use to run your own XMPP service, either over the Internet or on a [local area network](#lan).

## XML
