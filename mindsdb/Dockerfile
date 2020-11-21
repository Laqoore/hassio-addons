ARG BUILD_FROM
FROM $BUILD_FROM

RUN     apk add --no-cache \
        py3-pip \
        python3 \
        && pip install --no-cache-dir mindsdb
WORKDIR /
# Use cmd entry point to start the server
# Copy data
COPY rootfs /
CMD ["python", "-m", "mindsdb", "--api=mysql", "--config=config.json"]


