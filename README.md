# protoc-gen-entity

Generate Go structs + `ToProto()`/`FromProto()` + unit tests from
Protobuf messages.

## Usage

```bash
go install github.com/remitano/protoc-gen-entity@latest

protoc --entity_out=paths=source_relative:. proto/order.proto
