## Routing Service API Contract

### References

-   [Data Types](https://developers.google.com/protocol-buffers/docs/proto3#scalar)
-   [Working with null values](https://itnext.io/protobuf-and-null-support-1908a15311b6)

### Pre-requisite for code generation

In the `/rpc` directory, for each package, all the `*.go` files are generated from the `*.proto` file.  
**Important:** The generated `*.go` files must NOT be manually edited. To make changes, update the `*.proto` file and re-run the command below. This will re-generate and update the `*.go` files

Follow the installation steps linked [here](https://twitchtv.github.io/twirp/docs/install.html) before running the code generation commands below

### Command to generate code

```
// generate the Go files from the proto files
protoc --twirp_out=. --go_out=. <path-to-the-proto-file>
```

Example:

```
protoc --twirp_out=. --go_out=. rpc/helloworld/service.proto
```
