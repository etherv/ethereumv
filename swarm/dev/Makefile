.PHONY: build cluster test

default: build

build:
	go build -o bin/swarm    github.com/ethereumv/ethereumv/cmd/swarm
	go build -o bin/geth     github.com/ethereumv/ethereumv/cmd/geth
	go build -o bin/bootnode github.com/ethereumv/ethereumv/cmd/bootnode

cluster: build
	scripts/boot-cluster.sh

test:
	go test -v github.com/ethereumv/ethereumv/swarm/...
