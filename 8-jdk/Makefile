build:
	@docker build --tag=goodrainapps/openjdk .

release: build
	@docker build --tag=goodrainapps/openjdk:$(shell cat VERSION)-jdk-alpine .
