## GraphQL: application implemented in GOLang

Courses GraphQL applications example implemented in GOLang.
- using tool [gqlgen](https://github.com/99designs/gqlgen)

### Initializing mod in GOLang
```bash
go mod init github.com/leticiapillar/courses-go-graphql
```

## Tool: gqlgen
### Getting Started
- Building GraphQL servers in golang
- [Set up project](https://gqlgen.com/getting-started/#set-up-project)
- [Building the server](https://gqlgen.com/getting-started/#building-the-server)
- This lib generates a todo list example, using this command: `go run github.com/99designs/gqlgen init`

### Courses schema
- Update file `graph/schema.graphqls` with Courses schema
- Delete files:
    - `grpah/generated/*`
    - `grpah/model/*`
    - `graph/schema.resolvers.go`
- Execute command: `go run github.com/99designs/gqlgen generate` to generate structute files of schema.

