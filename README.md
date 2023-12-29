# protobuf
Common repo for generating gRPC stub

Add the following lines to every repo's Makefile to generate
Go:
```
gen_proto:
	echo "Building Proto"
	protoc --proto_path=./../protobuf --go_out=./pb --go_opt=paths=source_relative --go-grpc_out=./pb --go-grpc_opt=paths=source_relative main_service.proto
```
Swift:
```
gen_proto:
    protoc --proto_path=./../protobuf --swift_opt=Visibility=Public --swift_out=./"Mane HKU"/"Mane HKU"/pb --grpc-swift_opt=Visibility=Public --grpc-swift_out=./"Mane HKU"/"Mane HKU"/pb main_service.proto
```