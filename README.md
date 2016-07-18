# CubeSpawn-VizStack-DKR
Rviz Simulator for CubeSpawn

This is a docker-compose file and 2 docker files to build and deploy 2 containers:

A rosmaster container with python added;

And, an Rviz container for visualization.

Initially, there will be a few ROS packages, one for each CubeSpawn machine,
but in keeping with docker "best practices" these will likely be broken out into
thier own containers as they become more complete.
