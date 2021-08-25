# protoc-issue
A repo to house an issue I'm running into with protoc

## Generate Go code

The following command generate Go code from the Protobuf schema files:

```
protoc \
    --go_out=pb \
    --go_opt=paths=source_relative \
    --go-grpc_out=pb \
    --go-grpc_opt=paths=source_relative \
    protoc-issue-registry/messages/util/*.proto \
    protoc-issue-registry/services/hello/*.proto
```

## Issue observed

When generating Go code using the above command, the `util "github.com/codingconcepts/protoc-issue-registry/messages/util"` import in the pb/protoc-issue-registry/services/hello/hello.pb.go file cannot be resolved.