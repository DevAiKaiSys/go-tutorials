# Go Commands Reference

## Project Initialization
```bash
go mod init <module-path>
```

## Module Maintenance
Add missing and remove unused modules:
```bash
go mod tidy
```

## Local Development

[go mod edit command](https://go.dev/ref/mod#go-mod-edit)

Redirect module path to local directory:
```bash
go mod edit -replace example.com/module@v1.0.0=./local-path
```

## Running & Building
Run the current package:
```bash
go run .
```

Build the binary:
```bash
go build
```

## Testing
Run all tests in current directory:
```bash
go test ./...
```