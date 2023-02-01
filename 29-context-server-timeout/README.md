# Steps to install postgres in docker

1. Install docker

2. Download image postgres:latest

3. Create container: docker run --name [name-container] -p 5432:5432 -e POSTGRES_PASSWORD=[password] -d postgres

4. Enter container to create database: docker exec -it [name-container] psql -U postgres

5. Create database: CREATE DATABASE wonderland;

6. Create user and assign permissions:

    - CREATE USER alice WITH ENCRYPTED PASSWORD 'pa$$word';
    
    - GRANT ALL PRIVILEGES ON DATABASE wonderland TO alice;