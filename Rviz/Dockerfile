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

ENV uid 1000
ENV gid 1000

RUN export uid=${uid} gid=${gid} && \
    mkdir -p /home/ros && \
    echo "ros:x:${uid}:${gid}:ros,,,:/home/ros:/bin/bash" >> /etc/passwd && \
    echo "ros:x:${uid}:" >> /etc/group && \
    echo "ros ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/ros && \
    chmod 0440 /etc/sudoers.d/ros && \
    chown ${uid}:${gid} -R /home/ros

USER ros
ENV HOME /home/ros

RUN printf "export QT_GRAPHICSSYSTEM=native\nsource /opt/ros/indigo/setup.bash" >> /home/ros/.bashrc