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

If you want to bump minor/path version:
- Run `git tag v#{current_ver}.x.y`
- Run `git push --tags`

If you want to bump major version:
- update the module version in go.mod (add /v2, /v3... to the module path)
- Run `git tag v2.0.0`
- Run `git push --tags`
