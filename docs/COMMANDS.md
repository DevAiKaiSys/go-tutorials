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

Download and update dependencies:
```bash
go get .
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

[go build command](https://go.dev/cmd/go/#hdr-Compile_packages_and_dependencies)
```bash
go build
```

## Testing
Run tests in current directory:
```bash
go test
```

Run tests with verbose output:
```bash
go test -v
```

Run all tests in project:
```bash
go test ./...
```
## Environment & Installation

[go list command](https://go.dev/cmd/go/#hdr-List_packages_or_modules)
```bash
go list -f '{{.Target}}'
```

### Update PATH
On Linux or Mac:
```bash
export PATH=$PATH:/path/to/your/install/directory
```

On Windows:
```cmd
set PATH=%PATH%;C:\path\to\your\install\directory
```

### Set GOBIN
```bash
go env -w GOBIN=/path/to/your/bin
# or
go env -w GOBIN=C:\path\to\your\bin
```

[go install command](https://go.dev/ref/mod#go-install)
```bash
go install
```
