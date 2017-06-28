# springcloud-eureka-feign
Example of using Spring Cloud : 

eureka (service registration) and feign (a declarative HTTP client) 


## eureka-server

run `java -jar eureka-server/target/eureka-server-0.0.1-SNAPSHOT.jar`

http://localhost:8761

## hello-server

run `java -jar server/target/hello-server-0.0.1-SNAPSHOT.jar`

verify it is functioning at [http://localhost:7111](http://localhost:7111)

You should see `Hello World: HelloServer:myhostname:7111`

## hello-client

run `java -jar client/target/hello-client-0.0.1-SNAPSHOT.jar`

verify it is functioning at [http://localhost:7211](http://localhost:7211)

You should see `Hello World: HelloServer:myhostname:7111`


## See round robin load balancing in action 

default built in feign

run `java -jar server/target/hello-server-0.0.1-SNAPSHOT.jar --server.port=7112`

Go back to [http://localhost:7211](http://localhost:7211) and you should see both ports `7111` and `7112` in the output after a minute or two as you keep refreshing.
