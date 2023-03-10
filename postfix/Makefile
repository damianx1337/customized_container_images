BASE_IMG_NAME=debian
BASE_IMG_VERSION=bullseye
BASE_IMG_REPO=docker.io/library

IMG_NAME=postfix
IMG_VERSION=debian-bullseye-pkg-repo-version
CT_NAME=${IMG_NAME}_ct
MAINTAINER=to_be_set
CT_FILE=Containerfile
CT_PORT=25
HOST_PORT=2525

test:
	echo ${IMG_NAME}
	echo ${IMG_VERSION}
	echo ${CT_NAME}
	echo ${MAINTAINER}
	echo ${CT_FILE}

build:
	podman build -f ${CT_FILE} -t ${MAINTAINER}/${IMG_NAME}:${IMG_VERSION}

run:
	podman run -d -p ${HOST_PORT}:${CT_PORT} --name ${CT_NAME} ${MAINTAINER}/${IMG_NAME}:${IMG_VERSION}

shell-connect:
	podman exec -it ${CT_NAME} sh

view-logs:
	podman logs ${CT_NAME}

update-base-img:
	podman pull ${BASE_IMG_REPO}/${BASE_IMG_NAME}:${BASE_IMG_VERSION}
