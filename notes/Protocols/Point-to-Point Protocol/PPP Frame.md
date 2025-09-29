A _[[Point-to-Point Protocol|PPP]] frame_ is a modified version of a [[HLDC Frame]] which carries extra data.

![[PPP Frame.png]]

They are differentiated as:
- There is a new `Protocol` section before `Data`
- Both `Flag` and `Address` have hard-coded values.

# Protocol and Data
The `Protocol` heading signifies the type of packet being sent - this may be a number of values:
- **[[Link Control Protocol|LCP]]**: `0xC021`
- **[[Authentication Protocol|AP]]**: `0xC023` or `0xC223`
- **[[Network Control Protocol|NCP]]**: `0x8021`
- **Data**: `0x0021`

![[PPP Frame Components.png]]