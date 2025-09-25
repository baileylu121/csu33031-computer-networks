---
tags:
  - Transmission_Mode
---
In _half-duplex mode_, **both** the sender and receiver can transmit, however they can only do so **one at a time**.

![[Half-Duplex Mode Image.png]]
# Advantages

| Advantage                           | Description                                                                          |
| ----------------------------------- | ------------------------------------------------------------------------------------ |
| Efficient use of channel            | Allows for bi-directional communication over a single channel                        |
| Cost-Effective                      | If we only need one channel, hardware can be simplified                              |
| Simple Collision Handling           | Since only one device can transmit at once, we do not have to worry about collisions |
| Suitable for periodic communication | Some setups (i.e. walkie-talkies) only require communication every now and then      |
# Disadvantages

| Advantage                     | Description                                                                                  |
| ----------------------------- | -------------------------------------------------------------------------------------------- |
| Slower transmissions          | As data can only go one way at once, it is very difficult to create real-time communications |
| Poor in high traffic networks | In a congested network, the limitation of only one device transmitting becomes a bottleneck  |
