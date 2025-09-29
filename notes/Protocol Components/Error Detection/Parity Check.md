A _Parity Check_ involves expecting a certain property to be true about the **oddness** or **evenness** of the number of bits received.

# Even Check
An even _parity check_ involves sending an **optional extra** bit with every chunk of data so that the total number of $1$'s is always **even**.

![[Even Check.png]]

This is a fairly low overhead operation to perform (see the `popcnt` x86 ASM instruction), but is likely to miss a lot of errors during it's operation.

# Simple _Parity Check_
This _parity check_ is an expanded version of the [[Parity Check#Even Check|even check]] where both the $1$'s and $0$'s are checked, which allows all [[Single-Bit Error|single-bit errors]] to be detected.

Unfortunately, this introduces a decent sized amount of overhead, as, for example, for every $7000$ bits sent $1000$ bits of redundant information is also sent just to run the parity check.

# Two Dimensional _Parity Check_
For a _2D Parity Check_, a block of bits is subdivided into a grid, then an extra row and column of parity bits is added.

Then, every single row and column gets an [[Parity Check#Even Check|even parity check]] ran on it individually.

![[2D Parity Check.png]]