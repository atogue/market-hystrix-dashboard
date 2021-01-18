# market-hystrix-dashboard
This Spring Boot application is a microservice dashboard to handle circuit breaker and manage services workload into a registry platform.

## Note:
requirements:
- spring boot version >= 2.3.x and < 2.4.0
- java 15
- Maven 3.6.3
- Dependency: Hystrix Dashboard

Remember to enable Hystrix into Gateway API service by adding the following annotation into main class:
```
@EnableHystrix
```

Allow the actuator endpoint into dashboard proxy list by adding the following configuration into application.yml
```
hystrix:
  dashboard:
    proxy-stream-allow-list: "*"
```
or into application.properties:
````
hystrix.dashboard.proxy-stream-allow-list=*
```