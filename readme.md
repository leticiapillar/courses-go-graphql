## GraphQL: application implemented in GOLang

- Course: Full Cycle 3.0
- Module: Comunicação entre sistemas
- "Courses" is an example of GraphQL Application implemented in GOLang.
- Using tool [gqlgen](https://github.com/99designs/gqlgen)

---
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

### Lazy loading
Implementing lazy loading to Courses and Chapters
- Refator on `graph/model/models_gen.go` file 
- Create one model file to category, chapter and course
- Move repectively type structute to model file
- Add models path to file `gqlgen.yml` in `:models` section
- Generate resolver with command: `go run github.com/99designs/gqlgen generate`
- Implementing Courses and Chpaters resolvers

### Run server
```bash
go run server.go 

# GraphQL playground
http://localhost:8080/
```

---
## References
- [Introduction to GraphQL](https://graphql.org/learn/)
- [How to GraphQL](https://www.howtographql.com/)
- [Go GraphQL tools](https://graphql.org/code/#go)
- [Course: Full Cycle 3.0](https://imersao.fullcycle.com.br/page/lancamento/)
