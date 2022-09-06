REGISTRY_PREFIX		?= localhost:5001
IMAGE_NAME		?= test-image
IMAGE_TAG		?= 1.0.0

build-and-push: build push

build:
	docker build --no-cache -f test-image/Dockerfile -t $(REGISTRY_PREFIX)/$(IMAGE_NAME):$(IMAGE_TAG) test-image

push:
	docker push $(REGISTRY_PREFIX)/$(IMAGE_NAME):$(IMAGE_TAG)

.PHONY: build-and-push
.PHONY: build
.PHONY: push
