BASE_IMG_NAME=debian
BASE_IMG_VERSION=bullseye
BASE_IMG_REPO=docker.io/library

IMG_NAME=jenkins
IMG_VERSION=lts-2.346.2
CT_NAME=${IMG_NAME}_ct
MAINTAINER=to_be_set
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
	podman run -d -p 8080:8080 --name ${CT_NAME} ${MAINTAINER}/${IMG_NAME}:${IMG_VERSION}

update-base-img:
	podman pull ${BASE_IMG_REPO}/${BASE_IMG_NAME}:${BASE_IMG_VERSION}
