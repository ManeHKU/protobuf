# protobuf
Common repo for generating gRPC stub

Add the following lines to every repo's Makefile to generate
Go:
```
gen_proto:
	echo "Building Proto"
	protoc --proto_path=./../protobuf --go_out=./protos --go_opt=paths=source_relative --go-grpc_out=./protos --go-grpc_opt=paths=source_relative service.proto
```
Swift:
```
gen_proto = protoc --proto_path=./../protobuf --go_out=. --go_opt=paths=source_relative \
--go-grpc_out=. --go-grpc_opt=paths=source_relative \
protos/service.proto
```