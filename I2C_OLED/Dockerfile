ARG BUILD_FROM
FROM $BUILD_FROM

# Install requirements for add-on
RUN \
  apk add --no-cache \
    git \
    python3 \
    py3-pip \
    py3-requests \
    py3-pillow \
    py3-smbus

RUN git clone -b v1.0.5a --single-branch --depth 1 https://github.com/mkagawa/rpi_i2c_oled.git /I2C_OLED

COPY run.sh /
WORKDIR /data
RUN chmod a+x /run.sh
CMD [ "/run.sh" ]
