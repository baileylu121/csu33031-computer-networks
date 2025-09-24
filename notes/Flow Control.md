_Flow Control_ is a **group of procedures** used to control the **amount of data** a sender is able to send **without acknowledgement**.

# Protocols
There are a number of given protocols under the banner of _Flow Control_, depending on the quality of the channel.
## [[Noise|Noiseless]] Channel
There are a number of protocols for transmitting on channels where [[Noise]] is not an issue:
- [[Simplest]]
- [[Stop-and-Wait]]
## [[Noise|Noisy]] Channel
There is a number of protocols for transmitting on channels where [[Error Control|errors]] may occur:
- [[Stop-and-Wait ARQ]]
- [[Go-Back-N ARQ]]
- [[Selective Repeat ARQ]]