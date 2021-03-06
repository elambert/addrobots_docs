## Robotic Cart Reference Application

The project comes with a reference application that converts a wire cart or z-rack into autonomous, remote-drive vehicle. The cloud application encodes high-level, application-specific commands (e.g. "drive", "stop", "orbit", etc.) into protobuf messages that it sends to an Android application. The Android application is a fairly typical high-level vehicle control system with a PID loop fed by phone's sensor array: camera/optical-flow, compass heading, acceleration/tilt and so on. The PID control code converts these high-level application commands into low-level motor commands that it sends to a central background service that gets them onto the USB bus. This Android application only as as a fun project to get you familiar with how the stack works.

