AUTHOR=estuardoquan
IMAGE=dante

TAG=${AUTHOR}/${IMAGE}

all: docker-build

docker-build: docker-build-dante

docker-build-dante:
	docker build -t ${TAG}:alpine ./


