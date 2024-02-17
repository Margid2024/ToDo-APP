Command for the Project

step-1
Create a Docker Network: docker network create network1

step2
Create a Docker Volume: docker volume create volume1

step3
Create a container:

1. here we create 2 Container one is for mongodb container and second is node container

create 1st Container: docker run -d -p 27017:27017 -e MONGO_INITDB_ROOT_USERNAME=myuser -e MONGO_INITDB_ROOT_PASSWORD=mypassword -e MONGO_INITDB_DATABASE=mydatabase --hostname my_host --name mongo_con --network network1 -v /var/lib/docker/volumes/volume1/\_data mongo:latest

step-4
After Creating a mongo container open mongo container open mongo compass and click on New connection >> go to Advance connection option and add your Username and Password and establish your connection

step-5
Build the image: docker build -t my-node-app

step-6
create a node docker container: docker run -d -p 3000:3000 --name node-container --network network1 my-node-app:latest

step-7
go to browser the port for node application 3000 and run your application

---

Run the Project using Docker Compose

1. docker compose build
2. docker compose up -d

# ToDo-app-node-js-express-js-mongodb

![](screenshots/wallpaper.png)

Technology Stack:
Node js
Express js
Mongo DB
Html
CSS

The project uses express routes to post update and delete the data in the mongodb database and subsequently render results on the website for the user.

Features:
Add a new task
Delete a tasks
Update tasks as done
Delete all the tasks

# ToDo-app-node-js-express-js-mongodb

# ToDo-app-node-js-express-js-mongodb
