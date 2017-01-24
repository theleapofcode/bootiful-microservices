# bootiful-microservices
Spring boot microservice example with Spring cloud components like

	* Spring cloud config - Centralized configuration
	* Spring cloud feign - Inter microservice communication
	* Spring cloud ribbon - Client side load balancing
	* Spring cloud eureka - Service discovery
	* Spring cloud zuul - API gateway
	* Spring cloud stream - Messaging
	* ELK - Centralized logging
	* Spring actuator - Metrics
	* Spring cloud hysterix - Monitoring
	
Inspired by [Spring microservices](https://www.packtpub.com/application-development/spring-microservices)


## Steps to run the application

	1. Open project home in terminal and run maven build. 
		`mvn clean install -DskipTests`

	2. Start Rabbit MQ. 
		`rabbitmq-server`
		
	3. Start Elasticsearch. 
		`${ELASTICSEARCH_HOME}/bin/elasticsearch`
		
	4. Start Logstash. 
		`${LOGSTASH_HOME}/bin/logstash`
		
	5. Start Kibana. 
		`${KIBANA_HOME}/bin/kibana`

	6. Start spring cloud config server
		`java -jar bootiful-config-server/target/bootiful-config-server-1.0.0.jar`
		
	7. Start spring cloud eureka server
		`java -jar bootiful-eureka-server/target/bootiful-eureka-server-1.0.0.jar`
		
	8. Start api gateway server
		`java -jar bootiful-api-gateway/target/bootiful-api-gateway-1.0.0.jar`
		
	9. Start hystrix server
		`java -jar bootiful-hystrix-server/target/bootiful-hystrix-server-1.0.0.jar`

	9.Run below commands in separate terminal windows.
	`java -jar bootiful-flight-fares-service/target/bootiful-flight-fares-service-1.0.0.jar`
	`java -jar bootiful-flight-search-service/target/bootiful-flight-search-service-1.0.0.jar`
	`java -jar bootiful-flight-checkin-service/target/bootiful-flight-checkin-service-1.0.0.jar`
	`java -jar bootiful-flight-book-service/target/bootiful-flight-book-service-1.0.0.jar`
	`java -jar bootiful-flight-management-website/target/bootiful-flight-management-website-1.0.0.jar`

	10. Open Browser Window at `http://localhost:8001`

	11. When asked for credentials use guest/guest123

	12. Click Search Menu for Search and Booking

	13. Click CheckIn Menu for Checkin


