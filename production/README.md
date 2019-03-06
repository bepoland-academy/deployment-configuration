##### Run all Docker images:
* first build all necessary docker images
* run ``docker-compose up``
* validate if service are running:
  * [Configuration service for users-service](http://localhost:8888/users-service/default)
  * [Registry (Eureka) service](http://localhost:8761)
  * [Users service under gateway](http://localhost:8080/users/hello)