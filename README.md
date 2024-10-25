# faruqi-protos

Welcome to Faruqi Protos! This repository houses the Protocol Buffer definitions for my personal projects, providing a solid foundation for efficient and scalable gRPC communication.

## 🚀 Installation
```shell
$ go get -u github.com/faruqi/faruqi-protos
```

## 📦 Usage
Integrate this repository into your project seamlessly! To generate Go files from the <b>.proto</b> definitions, add the following target to your <b>Makefile</b>:

```makefile
PROTO_REPO_PATH=$(shell go list -m -f '{{ .Dir }}' github.com/faruqii/faruqi-protos)
PROTO_OUT_DIR=.

.PHONY: proto

proto-products:
	protoc -I="$(PROTO_REPO_PATH)" \
		--go_out=$(PROTO_OUT_DIR) \
		--go-grpc_out=$(PROTO_OUT_DIR) \
		"$(PROTO_REPO_PATH)/proto/products/*.proto"
```

### 📂 Output
The above command will generate the Go Protocol files into the <b>./proto</b> directory, ready for you to use in your application.




