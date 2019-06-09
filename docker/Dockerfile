FROM tensorflow/tensorflow:1.9.0-gpu

ADD docker/requirements_os.txt .
RUN apt update -y && apt install -y $(cat requirements_os.txt|grep -v '#')

ADD docker/requirements.txt .
RUN pip install -r requirements.txt

RUN mkdir /weights
RUN wget -P /weights http://www.vlfeat.org/matconvnet/models/imagenet-vgg-verydeep-19.mat