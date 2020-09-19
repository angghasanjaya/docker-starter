# docker-starter
My default docker settings for laravel project. Based on my project team settings

## How to use
- Install Docker compose (https://docs.docker.com/compose/install/)
- Put your project directory into ct_app
- rename it as "app" folder
- run `docker-compose up --build` to build webapp

## Services
- Your webapp: `localhost:18080`
- adminer: `localhost:18081` (user: root, pass: 1husf88sad)
- redis (port: 16379)
- mysql 5.7 (port:13306)

You can easily config services inside `docker-compose.yaml`


### NOTES FOR WINDOWS USER. IMPORTANT!
This project must be clone inside `C:\Users\yourusername` folder. If not, your project WILL NOT BE COPIED into your docker containers.
