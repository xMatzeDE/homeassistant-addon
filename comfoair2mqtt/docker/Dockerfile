ARG BUILD_FROM
FROM $BUILD_FROM

RUN apk add git bash \
 && cd /opt \
 && git clone https://github.com/adorobis/hacomfoairmqtt.git \
 && python3 -m venv /opt/hacomfoairmqtt \
 && cd /opt/hacomfoairmqtt \
 && pip3 install paho-mqtt pyserial pyyaml \
 && source /opt/hacomfoairmqtt/bin/activate \
 && rm /var/cache/apk/* \
 && rm -rf /root/.cache /root/.npm \
 && cp /opt/hacomfoairmqtt/src/ca350 /opt/hacomfoairmqtt/src/ca350.original \
 && sed -i 's|/usr/local/share/ca350/bin/python3.8|/opt/hacomfoairmqtt/bin/python3|g' /opt/hacomfoairmqtt/src/ca350

WORKDIR /opt/hacomfoairmqtt

COPY rootfs /
RUN chmod +x /*.sh
ENTRYPOINT ["/docker-entrypoint.sh"]
