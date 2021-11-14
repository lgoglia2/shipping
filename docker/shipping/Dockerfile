FROM maven:3.5.2-jdk-8-alpine
WORKDIR /root/tmp/repo
RUN apk add git && \
	git clone https://github.com/lgoglia2/shipping.git && \
	mvn -DskipTests package && \
	cd orders/target
ENTRYPOINT ["java","-jar","./shipping.jar", "--port=80"]