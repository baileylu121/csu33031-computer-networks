---
tags:
  - Transmission_Mode
---
In _simplex mode_, the sender is able to send data but cannot receive data, making it a **mono-directional** connection.

![[Simplex.png]]

# Advantages

| Advantage                       | Description                                                                                  |
| ------------------------------- | -------------------------------------------------------------------------------------------- |
| Simplicity                      | Data flowing only one way is far more simple than multidirectional                           |
| Cost-Effective                  | If data only needs to go one way, hardware can be simplified                                 |
| No Collision                    | There is no risk of collision on a _simplex_ route as it only travels one way                |
| Efficient for some applications | Some setups (i.e. transporting keyboard input) only require single directional communication |
# Disadvantages

| Advantage                           | Description                                                                                  |
| ----------------------------------- | -------------------------------------------------------------------------------------------- |
| Lack of bidirectional communication | Some applications are not possible (i.e. video calls)                                        |
| Inefficient at complex tasks        | Unable to receive acknowledgements in return hence error checking is impossible              |

