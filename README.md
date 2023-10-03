# README

This is an example of how to use Docker and Docker compose for spinning up your development enviroment.

## Requirements
- 8GB ram and 4 cores CPU is enough
- (Install Docker Desktop)[https://docs.docker.com/desktop/]
- Nothing else

## How to use
- Clone this repo
- Copy `.env.dev.example` to `.env.dev`
- Run `docker-compose up --build` to build containers in your terminal
- Wait for the containers to be up and running
- Open your browser and go to `http://localhost:3000`
- `crtl+c` to stop the containers

## Workflow
- `docker-compose up` to start de containers. Add `-d` to run in background
- `bin/dc bundle`  to install gems if needed
- `bin/dc rails db:create db:setup` to setup the database
- And in separate tabls
  - `bin/dc rails server` to start de rails server
  - `bin/dc rails console` to start de rails console
  - `bin/dc yarn build --watch` to compile Javascript
  - `bin/dc yarn build:css --watch` to compile CSS
  - `bin/dc bundle exec sidekiq` to start sidekiq 

Thanks

