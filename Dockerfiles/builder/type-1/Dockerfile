# portalmc/builder:type-1

FROM openjdk:8-jdk-alpine

LABEL maintainer "Ralph(Tamaki Hidetsugu) <me@ralph.ms>"

RUN apk --update --no-cache add bash \
 && mkdir /portal \
 && cd /portal \
 && touch build.sh \
 && chmod +x build.sh \
 && echo '#!/bin/bash' >> build.sh \
 && echo set -eu >> build.sh \
 && echo cp -r /portal/src /portal/work >> build.sh \
 && echo cd /portal/work >> build.sh \
 && echo chmod +x ./gradlew >> build.sh \
 && echo ./gradlew setupCIWorkspace build >> build.sh \
 && echo cp -r /portal/work/build/libs /portal/build >> build.sh \
 && echo 'find /portal/build/ -type f -exec chmod 644 \{\} \;' >> build.sh \
 && echo 'find /portal/build/ -type d -exec chmod 755 \{\} \;' >> build.sh

CMD /portal/build.sh
