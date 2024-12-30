# Instructions to Run MySQL and App Containers


## Running MySQL Container with Volume Attached
```bash
docker run -d --name mysql-container -v ~/mysql-data:/var/lib/MySQL -e MYSQL_DATABASE=app_db -e MYSQL_USER=app_user -e MYSQL_PASSWORD=1234 -e MYSQL_ROOT_PASSWORD=rootpassword -p 3306:3306 mysql-local:1.0.0
```

## Running App Container with Volume Attached
```bash
docker run -d --name todoapp-container --env DB_HOST=172.17.0.2 --env DB_USER=app_user --env DB_PASSWORD=1234 --env DB_NAME=app_db -p 8000:8080 todoapp:2.0.0
```
## Accessing the Application

Open your browser and go to: http://localhost:8000

## Docker Hub Repositories
MySQL Image: 88victory88/mysql-local
App Image: 88victory88/todoapp