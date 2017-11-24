# portalmc/builder:mc-1.12.2-1-alpine

FROM openjdk:8-jdk-alpine

LABEL maintainer "Ralph(Tamaki Hidetsugu) <me@ralph.ms>"

RUN apk update && \
    apk add bash

RUN ["/bin/bash", "-c", " \
        set -x && \
        mkdir /portal && \
        cd /portal && \
        touch build.sh && \
        chmod +x build.sh && \
        echo '#!/bin/bash' >> build.sh && \
        echo cp -r /portal/src /portal/work >> build.sh && \
        echo cd /portal/work >> build.sh && \
        echo chmod +x ./gradlew >> build.sh && \
        echo ./gradlew setupCIWorkspace build >> build.sh && \
        echo cp -r /portal/work/build/libs /portal/build >> build.sh \
    "]

CMD /portal/build.sh
