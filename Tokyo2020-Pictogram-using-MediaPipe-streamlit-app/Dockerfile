FROM python:3.9.6-buster

WORKDIR /ws
COPY ./requirements.txt /ws/requirements.txt
RUN pip install -U pip && \
    pip install -r requirements.txt
RUN rm -rf /var/lib/apt/lists/*
RUN apt-get update && apt-get install libgl1 && apt-get install -y python3-opencv
RUN pip install opencv-python
RUN apt-get install libgl1-mesa-glx
COPY . /ws
