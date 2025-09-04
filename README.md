# docker-frontend-backend-db-to_do_app
Simple Application with Frontend + Backend + DB


A demonstration of Docker to implement a simple 3-tier architecture
The 
frontend will be able to access the mid-tier
Mid-tier will be able to access the DB
In order to run this in Docker, simply type docker-compose up at the command prompt. Docker will then create the MongoDB from the stock mongo image. The api uses NodeJS with Express and is built from a node:alpine image. The front end uses ReactJS and built from a node:alpine image.

Steps:
~~~~~~
1. Clone the repository to the local.
2. Edit the env file /docker-frontend-backend-db/frontend/.env with your IP. If you are testing in a remote server, try the public IP address. If you are local, you can use the local host.
3. docker compose up -d
4. docker ps -a and verify the containers.
~~~
~/docker-frontend-backend-db/frontend# docker ps -a
CONTAINER ID   IMAGE                            COMMAND                  CREATED         STATUS         PORTS                                         NAMES
fa0f1ca1c84d   docker-frontend-backend-db-web   "docker-entrypoint.s…"   8 minutes ago   Up 8 minutes   0.0.0.0:3000->3000/tcp, [::]:3000->3000/tcp   docker-frontend-backend-db-web-1
76ea499a4471   docker-frontend-backend-db-api   "docker-entrypoint.s…"   8 minutes ago   Up 8 minutes   0.0.0.0:3001->3001/tcp, [::]:3001->3001/tcp   docker-frontend-backend-db-api-1
96e05160e1c9   mongo                            "docker-entrypoint.s…"   8 minutes ago   Up 8 minutes   27017/tcp                                     docker-frontend-backend-db-mongo-1
~~~ 
