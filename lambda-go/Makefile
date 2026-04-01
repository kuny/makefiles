#--------------------------------------------------
# for AWS Lambda go
#--------------------------------------------------

OS=linux
ARCH=amd64
BINARY_NAME=bootstrap
BUILD_DIR=build
ZIP_NAME=awsLambda.zip

.PHONY: all init tidy graph test build clean

all: clean build

init:
	go mod init

tidy:
	go mod tidy

list:
	go list -m all

graph:
	go mod graph

test:
	go test -v ./...

cover:
	go test -cover ./...

build:
	GOOS=$(OS) GOARCH=$(ARCH) go build -o $(BUILD_DIR)/$(BINARY_NAME) main.go
	chmod +x $(BUILD_DIR)/$(BINARY_NAME)
	zip -j $(BUILD_DIR)/$(ZIP_NAME) $(BUILD_DIR)/$(BINARY_NAME)

clean:
	rm -rf $(BUILD_DIR)

