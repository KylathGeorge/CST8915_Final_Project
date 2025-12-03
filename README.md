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

These microserves make up the demo app for the Best Buy cloud-native store. These microservices will be deployed to the Azure Kubernetes Service and will have automatic CI/CD pipelines which will automatically deploy any changes made to the store.

## Deployment instructions

## Links Table: Repository links and Docker Hub image links for all services

| Repository Link | Docker Hub Link |
|----------       |----------       |
| <https://github.com/KylathGeorge/CST8915-store-front-final-project>           | <https://hub.docker.com/r/kmgeorge/store-front-final-project/tags>               |
| <https://github.com/KylathGeorge/CST8915-store-admin-final-project>           | <https://hub.docker.com/r/kmgeorge/store-admin-final-project/tags>                |
| <https://github.com/KylathGeorge/CST8915-product-service-final-project>           | <https://hub.docker.com/r/kmgeorge/product-service-final-project/tags>                |
| <https://github.com/KylathGeorge/CST8915-order-service-final-project>           | <https://hub.docker.com/r/kmgeorge/order-service-final-project/tags>                |
| <https://github.com/KylathGeorge/CST8915-makeline-service-final-project>           | <https://hub.docker.com/r/kmgeorge/makeline-service-final-project/tags>                |
