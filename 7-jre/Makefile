build:
	@docker build --tag=goodrainapps/openjre .

release: build
	@docker build --tag=goodrainapps/openjdk:$(shell cat VERSION)-jre-alpine .
