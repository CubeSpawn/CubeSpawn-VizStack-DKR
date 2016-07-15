FROM ros:indigo-ros-core
ENV PYTHONUNBUFFERED 1

# add pip

RUN apt-get update && apt-get install -y \
    python-pip \

&& rm -rf /var/lib/apt/lists/* \

# Add code folder

mkdir /cubespawn/
WORKDIR /cubespawn/
COPY requirements.txt /cubespawn/requirements.txt
RUN pip install -r requirements.txt
COPY . /cubespawn/
