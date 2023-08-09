VTAG=$(shell date +"%y%m%d")
MAINTAINER=dnsobc
APP_NAME=load-tester


test:
	echo ${VTAG}
	echo ${MAINTAINER}

build:
	podman build -f Containerfile -t ${MAINTAINER}/${APP_NAME}:${VTAG}

run:
	podman run --rm -it --name ${APP_NAME}_ct ${MAINTAINER}/${APP_NAME}:${VTAG}
