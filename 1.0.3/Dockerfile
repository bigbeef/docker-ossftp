FROM python:2-alpine

WORKDIR /srv

RUN set -xe && \
    apk add --no-cache unzip curl bash && \
    curl -fsSLO --compressed "http://docs-aliyun.cn-hangzhou.oss.aliyun-inc.com/assets/attach/32190/cn_zh/1523340041580/ossftp-1.0.3-linux-mac.zip" && \
    unzip -o "ossftp-1.0.3-linux-mac.zip" -d /srv && \
    rm -rf "ossftp-1.0.3-linux-mac.zip" && \
    mv ossftp-1.0.3-linux-mac ossftp && \
    apk del unzip curl

EXPOSE 2048 8192

CMD [ "bash", "/srv/ossftp/start.sh" ]
