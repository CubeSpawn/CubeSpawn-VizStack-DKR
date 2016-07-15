FROM ros:indigo
# install ros tutorials packages
RUN apt-get update && apt-get install -y \
    python-pip \
    ros-indigo-common-tutorials \
    && rm -rf /var/lib/apt/lists
ENV PYTHONUNBUFFERED 1
RUN mkdir /cubespawn
WORKDIR /cubespawn
ADD requirements.txt /cubespawn/
RUN pip install -r requirements.txt
ADD . /cubespawn/