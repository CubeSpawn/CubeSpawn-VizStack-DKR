FROM ros:indigo-ros-core
# add pip

RUN apt-get update && apt-get install -y \
    ros-indigo-rviz \
    && rm -rf /var/lib/apt/lists

# Add code folder

RUN mkdir /cubespawn
WORKDIR /cubespawn

ADD dummy.txt /cubespawn/

ADD . /cubespawn/