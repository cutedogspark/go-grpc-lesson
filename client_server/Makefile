
all: protoc-go protoc-js


protoc-go:
	@protoc -I helloworld/ helloworld/helloworld.proto --go_out=plugins=grpc:./helloworld
	@echo "generate golang success"

protoc-js:
	@protoc -I helloworld/ helloworld/helloworld.proto \
     --js_out=import_style=commonjs,binary:./client-node/static-client \
     --grpc_out=./client-node/static-client  \
     --plugin=protoc-gen-grpc=$(shell which grpc_node_plugin)
	@echo "generate node(js) success"
