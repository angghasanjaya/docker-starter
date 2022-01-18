# docker-starter
My default docker settings for laravel project. Based on my project team settings (https://github.com/angghasanjaya/docker-starter)

## How to use
- Install Docker compose (https://docs.docker.com/compose/install/)
- Put your project directory into ct_app
- rename your project folder to "app"
- set your laravel `.env` : <br />

  DB_CONNECTION=mysql

  DB_HOST=dbmaster

  DB_PORT=3306

  DB_DATABASE=appdb

  DB_USERNAME=root

  DB_PASSWORD=1husf88sad

  REDIS_HOST=omniredis

  REDIS_PASSWORD=ij129Ias01

  REDIS_PORT=6379

  CACHE_DRIVER=redis
  
- if your project doesnt include vendors on it, please run this command inside your project "app" folder to install laravel dependencies 
  https://pastebin.com/raw/n2JvfyCV
- run `docker-compose up --build` to build webapp

## Services
- Your webapp: `localhost:18080`
- adminer: `localhost:18081` (user: root, pass: 1husf88sad)
- redis
- mysql 5.7

You can easily config services at `docker-compose.yaml`


### NOTES FOR WINDOWS USER. IMPORTANT!
USE POWERSHELL FOR RUNNING ALL DOCKER COMMANDS!
