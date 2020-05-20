FROM python:alpine

RUN apk update &&\
    apk add python3-dev musl-dev jpeg-dev zlib-dev gcc g++ git

RUN apk add opus opus-tools ffmpeg libmagic libjpeg

RUN git clone https://github.com/azlux/botamusique.git &&\
    cd botamusique &&\
    pip install wheel &&\
    pip install -r requirements.txt

COPY entrypoint.sh /
CMD ["/entrypoint.sh"]
