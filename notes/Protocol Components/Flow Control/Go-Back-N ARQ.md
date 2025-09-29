_Go-Back-N [[ARQ]]_  is a type of [[Flow Control|flow control]] which includes [[Error Control|error handling]] such that it can be used on [[Noise|noisy]] channels.

Here, data is sent in **sliding-windows**, and acknowledgements contain the amount of data actually received.

> [!example]
> If the window size is $3$ and we acknowledge that we have received $2$ chunks of data, the window is advanced by $2$, and the next $3$ pieces of data are sent. This way we can send multiple pieces of data to keep delay lower if a series of successes happen. 

![[Go-Back-N ARQ.png]]
