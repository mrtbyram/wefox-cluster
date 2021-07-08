# wefox-cluster

This cluster includes the containers given by assignment delivery folder and new Payment Controller container which checks the payments.

### How to execute

<code>
  git clone git@github.com:mrtbyram/wefox-cluster.git
  
  docker-compose up
</code>

Payment Controller container gets the application from https://github.com/mrtbyram/wefox.

### Notes

* Payment Controller is Java Spring Boot application. 
* Spring Kafka library is used to read kafka topics. 
* Spring Data library is used to connect to the postgresql.
* WebFlux library is used to call rest endpoints in order to support non-blocking flows.

### Things to improve

* Deployment lifecycle should be improved. Static file from a repository is used for creating the application containter right now. Docker image should be read from a docker registry which is updated by the push on the project repository.
* Application logs could be collected by a third party container.
