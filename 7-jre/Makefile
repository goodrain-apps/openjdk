build:
	@docker build --tag=goodrainapps/openjre .

release: build
	@docker build --tag=goodrainapps/openjre:$(shell cat VERSION)-jre-alpine .
