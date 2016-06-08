docker: Dockerfile
	docker build -t mygccbox80 .

test: docker
	go test
	docker run --rm mygccbox80 test

run:
	docker run -d -p 80:80 -t mygccbox80
