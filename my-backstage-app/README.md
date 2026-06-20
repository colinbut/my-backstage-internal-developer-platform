# My Internal Developer Platform

Internal Developer Platform (IDP) - based on [Backstage](https://backstage.io) by Spotify

## Fire up Backend DB

A Postgres db is setup as a docker container using Docker Compose. 

Environments variable are expected to be supplied via an `.env` file locally.

Create an `.env` file locally with the required Postgres credentials as Environment Variables.

_see the `docker-compose.yaml` file for required details_

Run following Docker Compose command to start up the db first.

```sh
docker-compose -f docker-compose.yaml up
```

## Start App

Then, to start the app, run:

```sh
yarn install
yarn start
```

## Author

Colin But.
