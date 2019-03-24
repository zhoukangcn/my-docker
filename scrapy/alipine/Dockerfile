FROM python:2.7-alpine

RUN echo 'http://mirrors.aliyun.com/alpine/v3.7/main' > /etc/apk/repositories \
    && echo 'http://mirrors.aliyun.com/alpine/v3.7/community' >> /etc/apk/repositories \
    && apk add --no-cache libxslt \
    && apk add --no-cache --virtual=build_dependencies gcc python-dev musl-dev libxml2-dev libxslt-dev libffi-dev openssl-dev \
    && cp -r /usr/include/libxml2/libxml/ /usr/include \
    && pip install -i https://mirrors.aliyun.com/pypi/simple/ --upgrade pip \
    && pip install -i https://mirrors.aliyun.com/pypi/simple/ scrapy \
    && apk del build_dependencies \
    && rm -rf /var/cache/apk/* \
    && rm -rf /tmp/* /var/tmp/*
