A _Cyclic Redundancy Check_ involves expecting a certain property to be true about the **divisibility** of number of bits received.

Before the data is sent, a certain number of bits are appended onto the message to ensure that it is **perfectly divisible** by a given **polynomial**. When the data is received, it is then divided by that **polynomial** again, and if it does not equal $0$ then an error has been found.

![[Cyclic Redundancy Check Image.png]]

It generally detects [[Burst Error|burst errors]] with a much higher quality than a [[Parity Check|parity check]], however, it also requires sending more bits too to ensure divisibility. Additionally, integer division is a fairly slow operation for computers to execute compared to others.