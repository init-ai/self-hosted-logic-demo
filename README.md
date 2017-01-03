# Self-hosted Logic Demo

This repo contains the basic scaffolded files and configuration of an [Init.ai](https://init.ai) project with a custom web server included to handle webhooks for processing logic in your own environment.

To assignt the webhook via the Init.ai console, you will need to expose the webhook server publicly. This repo contains a Procfile for use with [Heroku](https://heroku.com), however you may deploy this server on any service.

To test your webhook server locally, you may use a tool such as [ngrok](https://ngrok.com/) or [localtunnel.me](https://localtunnel.github.io/www/) to expose your `localhost` to the internet. But remember, _*DO NOT*_ rely on a locally running service for production!

See [this guide](https://docs.init.ai/docs/self-hosted-logic) for details on setup and deployment.

# Installation

## Node.js version

> **Note:** The recommendation for Node.js version 4.3.2 does not apply to self hosted logic. You may use the version of Node.js best suited for your environment.

To [run your scripts locally](http://docs.init.ai/docs/dev-server#section-local-testing), you should make sure to use Node.js version 4.3.2.

We recommend using [nvm](https://github.com/creationix/nvm) to easily manage Node.js versions on your machine. This project is pre-provisioned with an `.nvmrc` file so you may simply run:

```bash
$ nvm use
```

## Install dependencies.

```bash
$ npm i
```

# Usage

## Start Dev Server

```bash
$ npm start
```

## Start webhook server

```bash
$ npm run server
```

This will start the webhook server on at localhost:4044. You may override this using the `PORT` environment variable.

To run the server in watch mode using [nodemon](https://nodemon.io):

```bash
$ npm run server:watch
```
