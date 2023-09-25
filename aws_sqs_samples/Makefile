BASE_IMG_NAME=debian
BASE_IMG_VERSION=bullseye-slim
BASE_IMG_REPO=docker.io/library

IMG_NAME=aws-sqs-tester
IMG_VERSION=latest
CT_NAME=${IMG_NAME}_ct
MAINTAINER=dnsobc
CT_FILE=Containerfile

test:
	echo ${IMG_NAME}
	echo ${IMG_VERSION}
	echo ${CT_NAME}
	echo ${MAINTAINER}
	echo ${CT_FILE}

build:
	podman build -f ${CT_FILE} -t ${MAINTAINER}/${IMG_NAME}:${IMG_VERSION}

run:
	podman run --rm -it --name ${CT_NAME} ${MAINTAINER}/${IMG_NAME}:${IMG_VERSION}
