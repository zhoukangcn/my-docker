FROM python:2.7-alpine

RUN echo 'http://mirrors.aliyun.com/alpine/v3.7/main' > /etc/apk/repositories \
    && echo 'http://mirrors.aliyun.com/alpine/v3.7/community' >> /etc/apk/repositories \
    && pip install -i https://mirrors.aliyun.com/pypi/simple/ shadowsocks \
    && rm -rf /var/cache/apk/* \
    && rm -rf /tmp/* /var/tmp/*
