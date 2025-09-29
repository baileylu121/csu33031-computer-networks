_Selective Repeat [[ARQ]]_  is a type of [[Flow Control|flow control]] which includes [[Error Control|error handling]] such that it can be used on [[Noise|noisy]] channels.

Similar to [[Go-Back-N ARQ]], it also uses **sliding-windows** to increase the amount of data sent at once. Here, $2$ are used, one for the **sender** and one for the **receiver**.

Windows will be sent in full, and then advance by their full size after acknowledgement, unless a special **negative acknowledgement** is sent, which request re-sending the whole window at once.

![[Selective Repeat ARQ.png]]