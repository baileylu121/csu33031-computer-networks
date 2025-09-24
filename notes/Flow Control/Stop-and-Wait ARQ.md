_[[Stop-and-Wait]] [[ARQ]]_ is a variant of [[Stop-and-Wait|stop-and-wait]] which includes [[Error Control|error handling]] such that it can be used on [[Noise|noisy]] channels.

Here, an acknowledgement is only sent if two things have occurred:
- A packet has been received correctly
- The receiver is ready to receive another packet

> [!note]
> Frames are usually numbered to ensure the correct one will be resent if an acknowledgement is not received

![[Stop-and-Wait ARQ Image.png]]