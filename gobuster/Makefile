VTAG=v3.6.0-$(shell date +"%y%m%d")
MAINTAINER=dnsobc
APP_NAME=gobuster


build:
	podman build -f Containerfile -t ${MAINTAINER}/${APP_NAME}:${VTAG}
	podman image prune -f
	podman builder prune -f
	podman system prune -f

run:
	podman run --rm -it --name ${APP_NAME}_ct ${MAINTAINER}/${APP_NAME}:${VTAG}
