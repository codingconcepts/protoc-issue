# protoc-issue
A repo to house an issue I'm running into with protoc

## Generate Go code

```
protoc \
    -I . \
    --go_out=./pb \
    --go-grpc_out=./pb \
    registry/messages/util/*.proto \
    registry/services/hello/*.proto
```

## Issue observed

When generating Go code using the above command, the `util "registry/messages/util"` import in the pb/registry/messages/hello/hello.pb.go file cannot be resolved.