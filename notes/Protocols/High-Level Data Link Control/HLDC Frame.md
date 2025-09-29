A _[[High-Level Data Link Control|HLDC]] Frame_ is an individual packet of data and some metadata about the packet.

![[HLDC Frame.png]]

| Component            | Purpose                                                                         |
| -------------------- | ------------------------------------------------------------------------------- |
| Flag                 | The beginning and end of a frame                                                |
| Address              | The source [[HLDC Station#Secondary Station\|secondary]] device                 |
| Control              | The [[HLDC Frame#Types\|type]] of the frame and it's acknowledgement identifier |
| Frame Check Sequence | A $16$ or $32$ bit [[Cyclic Redundancy Check]]                                  |
# Types
There are a number of _[[High-Level Data Link Control|HLDC]] frame_ types with different purposes.

## I-Frame 
The _I-Frame_ is a type of frame containing information for transfer.

> [!info] Control Sequence
> It's control sequence looks like:
> ![[I-Frame.png]]
> **Where**:
> - $N(S)$ = Sequence number of sender
> - $N(R)$ = Sequence number of receiver
> - $P/F$ = Poll/Final Bit
## S-Frame 
The _S-Frame_ is a type of frame containing supervisory information for communication between devices. These may pertain to [[Flow Control|flow control]] or [[Error Control|error control]].

> [!info] Control Sequence
> It's control sequence looks like:
> ![[S-Frame.png]]
> **Where**:
> - $Code$ can be any of:
>   - $00$ = Receive Ready (RR)
>   - $10$ = Receive Not Ready (RNR)
>   - $01$ = Reject (REJ)
>   - $11$ = [[Selective Repeat ARQ|Selective Reject]] (SREJ)
>  - $N(R)$ = Sequence number of reciever
## U-Frame 
The _U-Frame_ is a type of frame used for miscellaneous other purposes.

> [!info] Control Sequence
> It's control sequence looks like:
> ![[U-Frame.png]]
> **Code may be any of**:
> ![[U-Frame Codes.png]]