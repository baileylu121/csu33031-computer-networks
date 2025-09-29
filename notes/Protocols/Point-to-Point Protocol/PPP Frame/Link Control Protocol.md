---
aliases:
  - LCP
---
A _Link Control Protocol_ packet is a variant of a [[PPP Frame]] which controls the function of the link between two devices, issuing commands like disconnection requests.

> [!note]
> A _Link Control Protocol_ packet looks like:
> ![[Link Control Protocol.png]]

# Codes
The codes that may be sent in a _Link Control Protocol_ packet are:

| Code   | Packet Type         | Description                                  |
| ------ | ------------------- | -------------------------------------------- |
| `0x01` | `Configure-request` | Returns the list of available config options |
| `0x02` | `Configure-ack`     | Accepts the proposed options list            |
| `0x03` | `Configure-nak`     | Does not accept some config options          |
| `0x04` | `Configure-reject`  | Does not recognize some config options       |
| `0x05` | `Terminate-request` | Requests a shutdown                          |
| `0x06` | `Terminate-ack`     | Accepts a shutdown                           |

# Options
Some of the configuration options available are:

| Option                                | Default |
| ------------------------------------- | ------- |
| Maximum Receive Unit                  | 1500    |
| Authentication Protocol               | None    |
| Protocol Field Compression            | Off     |
| Address and Control Field Compression | Off     |
