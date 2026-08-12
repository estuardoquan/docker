AUTHOR=estuardoquan
IMAGE=step-renew

TAG=${AUTHOR}/${IMAGE}

all: docker-build

docker-build: docker-build-step-renew

docker-build-step-renew:
	docker build -t ${TAG}:alpine ./
