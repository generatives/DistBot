# DistBot

This is code for a mobile robot running on a RaspberryPi. The it is a two wheeled robot with a omnidirectional whel for stability. It is equipped with a colour camera and an ultrasonic distance sensor.

The camera is used to find a red (configurable) ball. The robot will follow the red ball until it reaches it or looses sight of the ball. If the ball is lost it will drive in a random direction until reaching a wall, then pick a new random direction and drive. It will do this until it find the ball again.

The robot uses a simple state machine to manage the behaviours. ZMQ is used to separate the image processing from the robot behaviour.