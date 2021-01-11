# Go Style Guide

## Project Setup

1. Go modules should be used; enable with `go mod init`.
1. Make should be used; suggested Makefile:

```make
# default make target.
.PHONY: release
release: fmt vet test build

.PHONY: build
build:
	go build -v ./...

.PHONY: fmt
fmt:
	go fmt ./...

.PHONY: test
test:
	go test -v ./...

.PHONY: vet
vet:
	go vet -v ./...
```

## Development

1. Code should be formatted with `make fmt`.
1. Code should be vetted with `make vet`.
1. `%q` is preferred over `%s` when printing strings.
1. Imports should be sorted into two groups:
   1. standard library.
   1. everything else.
1. When logging an error use `.WithError(err)` and a helpful error message. Ex:
   `log.WithError(err).Error("failed to foo the bars")`.
1. Error messages should start with a lowercase letter. Ex: `failed to foo` not
   `Failed to foo`.
1. Use PascalCase or camelCase over other casings such as snake_case or
   kebab-case.
