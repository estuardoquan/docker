AUTHOR=estuardoquan
IMAGE=tor

TAG=${AUTHOR}/${IMAGE}

all: docker-build

docker-build: docker-build-tor

docker-build-tor:
	docker build -t ${TAG}:alpine ./


