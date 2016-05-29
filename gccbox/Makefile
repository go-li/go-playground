docker: Dockerfile
	docker build -t mygobox1 .

test: docker
	go test
	docker run --rm mygobox1 test

run:
	docker run -d -p 8078:8079 -t mygobox1
