
# ASP.NET Core - Load balancing with Nginx and Docker

This project aims to exemplify the scaling of a Web API built on ASP.NET Core with the increase in the number of instances and how to control load balancing using Nginx.



## Author

- [Rahiyan Safin](https://www.github.com/rahiyansafz)

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/rahiyansafin/)
[![twitter](https://img.shields.io/badge/twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/rahiyan_safin)
[![email](https://img.shields.io/static/v1?label=&message=E-mail&color=007722&style=for-the-badge&logo=mail.ru)](mailto:rahiaynsafin@gmail.com)

## Running the Project

Clone the repository

```shell
git clone git@github.com:rahiyansafz/netcore-load-balancing.git
```

Go to the directory

```shell
cd netcore-load-balancing
```

Upload the containers

```shell
docker compose up -d --build
```

## Demonstration

The architecture of this application can be seen below. We will have a request for the load balancer, managed by Nginx. It will send requests in order to all replicas of the ToDo API.

![diagram](./imgs/diagram.png)

After uploading the docker compose, it will create 04 containers, 03 of which are the replicas of the Web API and one for nginx.

![containers](./imgs/containers.png)

You will be able to see that each request is made to one of the containers.

![request](./imgs/load-balancing.gif)

## Reference

- [HTTP Load Balancing](https://docs.nginx.com/nginx/admin-guide/load-balancer/http-load-balancer/)
- [Host ASP.NET Core on Linux with Nginx](https://learn.microsoft.com/en-us/aspnet/core/host-and-deploy/linux-nginx?view=aspnetcore-8.0&tabs=linux-ubuntu)




