all: build

.PHONY: clean
clean:
	rm -rf torb

deps:
	gb vendor restore

.PHONY: build
build:
	GOPATH=`pwd`:`pwd`/vendor go build -v torb

.PHONY: run
run:
	DB_DATABASE=torb DB_HOST=127.0.0.1 DB_PORT=3306 DB_USER=isucon DB_PASS=isucon ./torb
