## Proglog

# To test API

`echo "test 1" | base64`

`curl -X POST localhost:8080 -d '{"record": {"value": "dGVzdCAxCg=="}}'`

`curl -X GET localhost:8080 -d '{"offset": 0}'`

# To install the Protocol Buffer Compiler

`brew install protobuf`

`brew install protoc-gen-go`

To test the installation, run `protoc --version`

# To compile protobuf into Go code

`go get google.golang.org/protobuf`

```
protoc api/v1/*.proto \
    --go_out=. \
    --go_opt=paths=source_relative \
    --proto_path=.
```