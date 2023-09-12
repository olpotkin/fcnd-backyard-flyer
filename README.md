# fcnd-backyard-flyer
How to control a drone with code in simulated environment.

[image_01]: ./docs/img-01.png "Simulator (backyard flyer scenario) window"

## Simulator
- Drone simulator is [available on GitHub](https://github.com/udacity/FCND-Simulator-Releases/releases).
![alt text][image_01]

## Main goals of the Project
1. **Setting the drone's target position (for the autopilot to follow)** by using the `cmd_position` method from the `Drone` class.
2. **Responding to messages from the autopilot**

`BackyardFlyer` class will be sent messages from the autopilot to let it know when something about the drone has changed.
For example, the autopilot will send a `LOCAL_POSITION` message whenever the drone's local position changes. 

The code is responsible for registering certain functions (called "callback functions") to respond to these messages.
For example, if we need to call some function named `local_position_callback` whenever we receive a `LOCAL_POSITION` update,
we need to write code that says:

`self.register_callback(MsgID.LOCAL_POSITION, self.local_position_callback)`







