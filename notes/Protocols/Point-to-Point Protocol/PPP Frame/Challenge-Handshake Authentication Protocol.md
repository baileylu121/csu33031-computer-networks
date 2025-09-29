---
aliases:
  - CHAP
---
_Challenge-Handshake Authentication Protocol_ is a variation of [[Authentication Protocol]] which handles authentication by attaching a **challenge**.

When a connection request is made, system `A` will create a challenge value (i.e. a hash) based on a **password** which is stored locally and **never transmitted**.

It will then send that challenge to system `B`. If system `B` generates a **matching challenge** for it's own local password, connection is allowed.

![[Challenge-Handshake Authentication Protocol.png]]

> [!note]
> This method is generally much more secure than [[Password Authentication Protocol|PAP]], as it **does not** transmit the password in **plain text**.

# Packet
A _Challenge-Handshake Authentication Protocol_ might look like:
![[Challenge-Handshake Authentication Protocol Packet.png]]