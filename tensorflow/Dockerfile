FROM tensorflow/tensorflow:latest-gpu-jupyter

WORKDIR /tf

COPY requirements.txt /tf
COPY test.py /tf

RUN pip install -q -r requirements.txt
RUN pip3 install matplotlib
RUN apt-get install libgl1 -y --fix-missing
RUN apt-get install ffmpeg -y --fix-missing
RUN apt-get libsm6 -y --fix-missing
RUN apt-get libxext6 -y --fix-missing

RUN python test.py

EXPOSE 8080