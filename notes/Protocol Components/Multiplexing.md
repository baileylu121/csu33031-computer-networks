_Multiplexing_ is the process of transmitting multiple data streams, along with a of control segment and selecting one out many of those streams based on that control segment.

An example of a _multiplexer_ may be implemented with this pseudo-code:
```elixir
a = [
	010010
	110110
	000100
	110110
]

def mux(a, 0001), do: a[0] # 010010
def mux(a, 0010), do: a[1] # 110110
def mux(a, 0100), do: a[2] # 000100
def mux(a, 1000), do: a[3] # 110110
```