VTAG=$(shell date +"%y%m%d")
MAINTAINER=dnsobc
APP_NAME=jekyll-site


build:
	podman build -f Containerfile -t ${MAINTAINER}/${APP_NAME}:${VTAG}
	podman image prune -f
	podman builder prune -f
	podman system prune -f

run-it:
	podman run --rm -it -p 4000:4000 --name ${APP_NAME}_ct ${MAINTAINER}/${APP_NAME}:${VTAG}
run-d:
	podman run -d -p 4000:4000 --name ${APP_NAME}_ct ${MAINTAINER}/${APP_NAME}:${VTAG}
shell:
	podman exec -it ${APP_NAME}_ct /bin/bash
