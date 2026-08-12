AUTHOR=estuardoquan
IMAGE=node

TAG=${AUTHOR}/${IMAGE}

all: docker-build

docker-build: docker-build-node

docker-build-node:
	docker build -t ${TAG}:alpine ./
