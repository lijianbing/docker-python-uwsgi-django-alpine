# python 3.6, uwsgi, django-1.11.15
FROM python:3.6-alpine
RUN sed -i 's/dl-cdn.alpinelinux.org/mirror.tuna.tsinghua.edu.cn/g' /etc/apk/repositories \
    && apk add --no-cache tzdata \
    && apk add --no-cache --virtual mypacks linux-headers libc-dev gcc \
    && pip install -i https://mirrors.aliyun.com/pypi/simple/ uwsgi django==1.11.15 mysql-connector-python \
    && apk del mypacks \
    && rm -rf /root/.cache




