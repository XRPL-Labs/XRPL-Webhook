# CSCL Webhook

Register Apps and add CSCL account subscriptions + Webhook endpoint URL's. The service will watch the CSC ledger for `payment` transactions, and HTTP POST Webhooks will be sent to the subscribed apps + endpoints.

## Start & run manually

  * Install dependencies with `mix deps.get`
  * Check your database setting at `config/dev.exs` and match your postgresql credential
  * Create and migrate your databmixase with `mix ecto.create && mix ecto.migrate`
  * Install Node.js dependencies with `cd assets && npm install`
  * Add env variables to your environment
    * `GITHUB_CLIENT_ID` and  `GITHUB_CLIENT_SECRET` Github Sign-in
    * `TWITTER_CONSUMER_KEY` and  `TWITTER_CONSUMER_SECRET` Twitter-Sign-in
  * Start Phoenix endpoint with `mix phx.server`

## Start & run with Docker Compose

The attached docker-compose definition will run `postgres:alpine` and this application.

Run the platform:

```
docker-compose up
```

If you made changes to this reposority, you may need to rebuild the Docker image:

```
docker-compose build
```
