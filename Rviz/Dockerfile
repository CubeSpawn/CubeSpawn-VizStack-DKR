FROM ros:indigo-ros-core
# add pip

RUN apt-get update && apt-get install -y \
    python-pip \
    && rm -rf /var/lib/apt/lists

ENV PYTHONUNBUFFERED 1

# Add code folder

RUN mkdir /cubespawn
WORKDIR /cubespawn

ADD requirements.txt /cubespawn/

RUN pip install -r requirements.txt

ADD . /cubespawn/