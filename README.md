# Spring Cloud Bus
Spring Cloud Bus module can be used to link multiple applications
with a message broker and we can broadcast configuration changes.

https://sivalabs.in/2017/08/spring-cloud-tutorials-auto-refresh-config-changes-using-spring-cloud-bus/

Let us see how we can use RabbitMQ as message broker and connect multiple applications 
to receive the configuration change events and refresh the bounded property values.

* This project has 3 modules 2 client module and one server which is configured with git config location
* RabbitMQ dockerized image is started for brodcasting config change
* run docker-compose up to start rabbitmq container.
* http://localhost:8181/actuator/bus-refresh api for broadcasting config refresh.
All the Client who is configured with the below dependency:

		<dependency>
			<groupId>org.springframework.cloud</groupId>
			<artifactId>spring-cloud-starter-bus-amqp</artifactId>
		</dependency>
will listent to event and refresh.

