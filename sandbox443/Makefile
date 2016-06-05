docker: Dockerfile
	docker build -t xiam/go-playground/sandbox .

test: docker
	go test
	docker run --rm xiam/go-playground/sandbox test

run:
	docker run -d -p 443:443 -t xiam/go-playground/sandbox
