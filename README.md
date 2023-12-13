# spring-cloud-gateway-hystrix

Spring Boot Microservices Sample Project 

API-GateWay
-----------
```bash
URL : http://localhost:8989/order/bookOrder
HTTP Method : POST
```
Json Request :
```json
{
	"order":{
		"id":103,
		"name":"Mobile",
		"qty":1,
		"price":8000
		
	},
	"payment":{}
}
```
Json Response :
```json
{
    "order": {
        "id": 26,
        "name": "ear-phone",
        "qty": 5,
        "price": 4000
    },
    "amount": 4000,
    "transactionId": "9a021fa6-2061-4332-bdb7-b1358b3430c2",
    "message": "payment processing successful and order placed"
}

```
```bash
URL : http://localhost:8989/payment/26
HTTP Method : GET
```
Json Response :
```json
{
    "paymentId": 1,
    "transactionId": "d86cfeca-0b26-455e-a1a2-ac3e53707829",
    "orderId": 103,
    "paymentStatus": "SUCCESS",
    "amount":4000
}
```

```
Technologies in this project :
1. Create 2 microservice from scratch 
2. Register microservice in Eureka Service Discovery
3. integrate Spring Cloud Gateway for routing user request
4. Integrate Hystrix & Hystrix Dashboard to identify failure for downstream services
5. Spring cloud config server using Git to Centralize configuration across application
6. ELK Stack to centralize logging across all microservices
7. Zipkin & Sleuth to centralize tracing in microservice architecture
```

Youtube Link:
```
https://www.youtube.com/watch?v=tljuDMmfJz8&t=1s
```
