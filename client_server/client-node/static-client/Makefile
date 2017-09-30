

protoc:
	@protoc -I ../../helloworld/ ../../helloworld/helloworld.proto \
     --js_out=import_style=commonjs,binary:./ \
     --grpc_out=./ \
     --plugin=protoc-gen-grpc=$(shell which grpc_node_plugin)
	@echo "generate success"
