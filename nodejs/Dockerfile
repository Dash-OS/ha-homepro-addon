ARG BUILD_FROM
FROM $BUILD_FROM



WORKDIR /opt

# Set shell
SHELL ["/bin/bash", "-o", "pipefail", "-c"]

RUN \ 
     apk add --no-cache \
        curl \
        git=2.40.1-r0 \
        nodejs=20.8.0

WORKDIR /data

# Copy data for add-on
COPY package.json /
COPY run.sh /
COPY index.js /
RUN chmod a+x /run.sh

CMD [ "/run.sh" ]