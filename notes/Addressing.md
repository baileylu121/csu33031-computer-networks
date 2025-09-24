_Addressing_ is the process of determining the next network hop to jump to.

This can be visualised by running `traceroute`:
```
traceroute google.com
traceroute to google.com (142.251.211.238), 64 hops max
  1   XXX.XXX.XXX.XXX  1.774ms  104.766ms  3.077ms 
  2   XXX.XXX.XXX.XXX  6.823ms  3.086ms  7.370ms 
  3   XXX.XXX.XXX.XXX  5.812ms  5.779ms  5.409ms 
  4   XXX.XXX.XXX.XXX  9.143ms  8.665ms  8.401ms 
  5   XXX.XXX.XXX.XXX  11.137ms  10.538ms  10.456ms 
  6   XXX.XXX.XXX.XXX  14.092ms  15.286ms  13.024ms 
  7   XXX.XXX.XXX.XXX  15.759ms  16.233ms  12.949ms 
  8   XXX.XXX.XXX.XXX  13.007ms  13.036ms  13.611ms 
  9   142.251.211.238  13.677ms  12.065ms  11.839ms 
```