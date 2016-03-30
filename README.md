##Description

Sample project to demonstrate using docker compose to get a dockerized simple web app talking with a dockerized database

##Usage

To just run the application:
```
> gradle bootRun
> curl localhost:8080/helloWorld  | less
```

To run everything in a container 
```
> gradle startEnvironment
```

The url will depend on your docker setup 

If going through docker-machine:
```
http://192.168.99.100:8080/helloWorld  
```
otherwise: 
```
http://localhost:8080/helloWorld
```
##Technologies Used

Gradle
Docker
Spring boot

##Outstanding Questions

