# protoc-gen-entity

Generate Go structs + `ToProto()`/`FromProto()` + unit tests from
Protobuf messages.

## Usage

```bash
go install github.com/remitano/protoc-gen-entity@latest

protoc --entity_out=paths=source_relative:. proto/order.proto
```

## Versioning

We follow [go
guide](https://www.compilenrun.com/docs/language/go/go-project-structure/go-versioning/)
on versioning.

TL;DR:

```
./bin/bump_version
```

## Testing in local env
- Sửa code ở main.go
- Build executable file: `go build -o ./bin/protoc-gen-entity .`
- Chạy pwd lấy {protoc-gen-entity_repo_location}
- Update bin/convert-proto file ở trading-engine repo phần "# 2) Generate với protoc-gen-entity" như sau:
```
protoc \
  --proto_path=./protos \
  --plugin=protoc-gen-entity="{protoc-gen-entity_repo_location}/bin/protoc-gen-entity" \
  --entity_out=paths=source_relative:./tmp \
  ./protos/events/*.proto
```