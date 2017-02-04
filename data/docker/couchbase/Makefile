NAME = mychiara/hns_couchbase
TAG = 0.0.4

build:
	docker build -t $(NAME):$(TAG) --rm .

run:
	docker run --name hns_cb -d -p 8091-8093:8091-8093 -p 11207:11207 -p 11210-11211:11210-11211 -p 18091-18092:18091-18092 $(NAME):$(TAG)

rm:
	docker stop hns_cb && docker rm hns_cb

push:
	docker push $(NAME):$(TAG)