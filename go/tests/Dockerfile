FROM golang:1-alpine

ENV GIT_TERMINAL_PROMPT=0
RUN apk add --no-cache git
RUN go get golang.org/x/tools/cmd/goimports
RUN go get github.com/01-edu/z01
COPY entrypoint.sh /usr/local/bin
COPY . src
RUN go install rc prog/...
ENTRYPOINT ["/bin/sh", "/usr/local/bin/entrypoint.sh"]
