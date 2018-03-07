# DMDB pgAdmin & PostgreSQL for Docker

`docker-compose.yml` modified from [khezen/compose-postgres](https://github.com/khezen/compose-postgres).

## Setup
1) [Install Docker and Docker-Compose](https://docs.docker.com/compose/install/)
2) Download the `docker-compose.yml` file
3) run `docker volume create pgdata` and `docker volume create pgadmin` to create the volumes

## Using
1) Open the command-line and navigate to the directory where you have the `docker-compose.yml` file
2) run `docker-compose up -d` to start the app
3) Go to `localhost:5050` with your favourite browser.
4) log-in with E-Mail `dmdb@example.com` and Password `admin`
![Step 1](https://i.imgur.com/ICIaVdQ.png)
5) On the dashboard, click on `Add New Server`
![Step 2](https://i.imgur.com/2jnCWKA.png)
6) Give the server any name, and go to the Connection tab. As the hostname, use `postgres`, username and role are `postgres` as well, and the password is `password`.
Click on Save to connect to the server.
![Step 3](https://i.imgur.com/PP593JU.png)
7) Navigate to the database you just created and click on Tools in the navbar and then on Query Tool.
![Step 4](https://i.imgur.com/GqvaRSD.png)
8) Now you can use the SQL prompt window!
![Step 5](https://i.imgur.com/ZTUBbei.png)

## Stopping the application
To stop the application, just enter `docker-compose down` in the terminal, when you are in the folder with the `docker-compose.yml` file.

## Restarting again
Just follow the steps in the Using chapter to use the app to any later point again. Thanks to the docker volumes, the databases will be persistens even when you shut down Postgres.