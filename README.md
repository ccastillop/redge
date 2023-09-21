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
- `docker-compose up` to start de containers
- `bin/dc bundle`  to install gems
- `bin/dc rails db:create db:setup` to setup the database

- Run all at once
  - `bin/dev`

- Or, you can run each process in separate tabls
  - `bin/dc rails server` to start de rails server
  - `bin/dc rails console` to start de rails console
  - `bin/dc yarn build --watch` to compile Javascript
  - `bin/dc yarn build:css --watch` to compile CSS
  - `bin/dc sidekiq` to start sidekiq


## Pending task
- [ ] Review initial permisisions for Bundle and Yarn
- [ ] Set database from the begining 
- [ ] Other?

Thanks

