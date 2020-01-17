# pet-monitoring

Pet project to learn monitoring tools such as: grafana, prometheus , ELK

## Idea:
The idea behind this project is to architecture a project, where it can be monitored. Moreover, I will aim to create this project by steps, using ADR's to keep design decisions&tooling. Stack that I'm willing to learn and apply : Prometheus, Docker, Docker-compose, Micrometer, SpringBoot. I will create a basic API, just to feed monitoring data.

## How to run it:
```
./gradlew build
docker build -t pet-monitoring
docker tag pet-monitoring [yourdockeruserexample:'laullobet']/pet-monitoring:[versionyoulikeexample:'0.1']
docker-compose up
```
## How to test it 
```curl http://localhost:8080/orders```
Should trigger the follwing log:
```web_1              | 2020-01-17 12:48:22.521  INFO 1 --- [nio-8080-exec-3] c.p.o.interfaces.web.GetOrderController  : Responding orders...
   web_1              | 2020-01-17 12:48:53.834  INFO 1 --- [nio-8080-exec-5] c.p.o.interfaces.web.GetOrderController  : Responding orders latency [544]
```

## How to use it 
Keep curling http://localhost:8080/orders 
Visit http://localhost:9090
