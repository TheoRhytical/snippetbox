# Snippetbox

Web app for sharing of text snippets

This project was built solely to learn Go web development patterns including
- File structure
- Seperation of Concerns
- Dependency Injection
- Logging
- Error handling
- Database actions
- Go templating and embedded FS
- Middleware
- Authentication and Security
- Testing


### Dependencies

Requirements for the software and other tools to build, test and push
- Go >= 1.22
- MySQL Database or Docker
- [air](https://github.com/air-verse/air) [Optional]

### Setting up self signed TLS Cert

```
mkdir tls
cd tls
```
`go run <Go standard library source code path>/crypto/tls/generate_cert.go --rsa-bits=2048 --host=localhost`
Example (running in Debian):
`go run /usr/local/go/src/crypto/tls/generate_cert.go --rsa-bits=2048 --host=localhost`


### Running in Dev

Download dependencies
```
go mod tidy

```
Setup MySQL or `cp .env.example .env` and configure `.env`, then run `docker compose up`

Running the web app
```
go build -o bin/snippetbox ./cmd/snippetbox
./bin/snippetbox
```
or
```
air
```

## Running the tests

`go test ./cmd/snippetbox`



Project taken from the book: "Let's Go!" by Alex Edwards
