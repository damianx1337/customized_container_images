VTAG=$(shell date +"%y%m%d")
MAINTAINER=dnsobc
APP_NAME=yt-dlp


build:
	podman build -f Containerfile -t ${MAINTAINER}/${APP_NAME}:${VTAG}
	podman image prune
	podman builder prune
	podman system prune

run:
	podman run --rm -it --name ${APP_NAME}_ct ${MAINTAINER}/${APP_NAME}:${VTAG}
