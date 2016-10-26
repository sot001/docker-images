build:
	@docker build -t minecraft .
run:
	@docker run -p 25565:25565 --name=minecraft -d minecraft
stop:
	@docker stop minecraft
clean:  stop
	@docker rm minecraft

