
GOPATH:=$(shell go env GOPATH)
.PHONY: proto
proto:
	protoc --proto_path=. --micro_out=. --go_out=:. proto/helloworld.proto
	
.PHONY: build
build:
	go build -o helloworld *.go

.PHONY: test
test:
	go test -v ./... -cover

.PHONY: docker
docker:
	docker build . -t helloworld:latest
