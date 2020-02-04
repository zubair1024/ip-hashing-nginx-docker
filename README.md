![stable](https://img.shields.io/badge/build-stable-green) ![zubair1024](https://img.shields.io/badge/author-zubair1024-cyan)

# Dockerized HTTP NodeJS Server Load Balance with NGINX 🐳

## Get Started:

### NodeJS HTTP Server

1. Build the service

```bash
docker build -t test-app .
```
2. Run docker instances

```bash
docker run -e "MESSAGE=First" -p 8081:8080 -d test-app
docker run -e "MESSAGE=Second" -p 8082:8080 -d test-app
```

### NGINX Server

1. Build the service

```bash
docker build -t nginx-server .
```

2. Run the service
```bash
docker run -p 8080:80 -d nginx-server
```

Note: The load balancing strategy is using IP hashing to maintain sessions

## Built With

- [NodeJS](https://nodejs.org/en/)
- [Docker](https://www.docker.com/)

## Authors

- **Zubair Ahmed** - [Grizzlybit](https://grizzlybit.info) 👋


