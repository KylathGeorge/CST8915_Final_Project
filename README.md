# CST8915: Final Project

## Name: Kylath Mamman George

## Student Number: 041198835

## Youtube Link

[Final Project Youtube Link]()

## Updated Architecture Diagram

Diagram:

![Architecture Diagram](CST8915-final-project-architecture.drawio.svg)

## Brief application explanation

This is a demo of a cloud-native application that contains 5 microservices:

- **Store-Front**: Customer web app.
- **Store-Admin**: Employee web app.
- **Order-Service**: Order processing API.
- **Product-Service**: Product management API.
- **Makeline-Service**: Background worker for order processing.
- **Database**: MongoDB (Stateful).

These microserves make up the demo app for the Best Buy cloud-native store. These microservices will be deployed to the Azure Kubernetes Service and will have automatic CI/CD pipelines which will automatically deploy any changes made to the store. From the architecture diagram, we can see tehre are two actors: Customers and Employees. The customers interact with the Store Front which is a customer web application, which sends requests to the Order Service to place orders and the Product Service to fetch information on the products. The Store admin is a employee web interface and allows employees to send requests to the Makeline Service for order processing  and Product Service for managing the products.

On the Back End, Order Service handles orders and pushes orders to the RabbitMQ service for asynchronous processing. The Makeline Service processes orders from the queue adn updates the order database with the processed orders.

## Deployment instructions

1. Provision AKS with one servernode and one worker node.
2. Run the following command in /Deployment Files/aps-all-in-one.yaml directory:

```kubernetes
kubectl apply -f config-maps.yaml
kubectl apply -f aps-all-in-one.yaml
```

## Links Table: Repository links and Docker Hub image links for all services

| Repository Link | Docker Hub Link |
|----------       |----------       |
| <https://github.com/KylathGeorge/CST8915-store-front-final-project>           | <https://hub.docker.com/r/kmgeorge/store-front-final-project/tags>               |
| <https://github.com/KylathGeorge/CST8915-store-admin-final-project>           | <https://hub.docker.com/r/kmgeorge/store-admin-final-project/tags>                |
| <https://github.com/KylathGeorge/CST8915-product-service-final-project>           | <https://hub.docker.com/r/kmgeorge/product-service-final-project/tags>                |
| <https://github.com/KylathGeorge/CST8915-order-service-final-project>           | <https://hub.docker.com/r/kmgeorge/order-service-final-project/tags>                |
| <https://github.com/KylathGeorge/CST8915-makeline-service-final-project>           | <https://hub.docker.com/r/kmgeorge/makeline-service-final-project/tags>                |
