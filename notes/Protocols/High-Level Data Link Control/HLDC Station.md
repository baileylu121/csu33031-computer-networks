A _[[High-Level Data Link Control|HLDC]] Station_ is a given point of transmission along a route implementing [[High-Level Data Link Control|HLDC]].

![[HLDC Station Image.png]]
# Primary Station
The _Primary Station_ controls the operation of the link.

> [!note]
> Any frames issued are known as **commands**.
# Secondary Station
The _Secondary Station_ exists under control of the [[HLDC Station#Primary Station|primary station]].

> [!note]
> Any frames issued are known as **responses**.
# Combined Station
The _Combined Station_ is an instance of a [[HLDC Station#Primary Station|primary station]] and [[HLDC Station#Secondary Station|secondary station]] sharing an implementation.

> [!note]
> The _Combined Station_ may issue **commands** or **responses**.

![[HLDC Combined Station Image.png]]