# README

This is an example of how to use Docker and Docker compose for spinning up your development enviroment.

## Requirements
- 8GB ram and 4 cores CPU is enough
- [Install Docker Desktop](https://docs.docker.com/desktop/)
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

- Run all at once
  - `bin/dev`

  Usually, the script will install foreman gem using your local ruby. 
  (Ok, a paradox :))


- Or, you can run each process in separate tabls
  - `bin/dc bin/rails server -b 0.0.0.0` to start de rails server at port 3000
  - `bin/dc bin/rails console` to start de rails console
  - `bin/dc yarn build --watch` to compile Javascript
  - `bin/dc yarn build:css --watch` to compile CSS
  - `bin/dc sidekiq` to start sidekiq 
  - `bin/dc bash` to open a console in your container
  - `bin/dc bundle` to install any new gem added to Gemfile
  - and so on ...

Luckly you can go to http://localhost:3000/ 

## Pending task
- [ ] Review initial permisisions for Bundle and Yarn
- [ ] Set database from the begining 
- [ ] Other?

Thanks

