FROM        --platform=$TARGETOS/$TARGETARCH python:3.13-alpine

LABEL       author="Brijesh Poojary" maintainer="bxd@reviactyl.app"

LABEL       org.opencontainers.image.source="https://github.com/reviactyl/images"
LABEL       org.opencontainers.image.licenses=MIT

RUN         apk add --update --no-cache cmake make ca-certificates curl ffmpeg g++ gcc git openssl sqlite tar tzdata \
	&& adduser -D -h /home/container container

USER        container
ENV         USER=container HOME=/home/container
WORKDIR     /home/container

COPY        ./../entrypoint.sh /entrypoint.sh
CMD         [ "/bin/ash", "/entrypoint.sh" ]
