# XRPL Webhook

Register Apps and add XRPL account subscriptions + Webhook endpoint URLs. The service will watch the XRP Ledger for `payment` transactions, and HTTP POST Webhooks will be sent to the subscribed apps + endpoints.

## Start & run manually

- Install dependencies with `mix deps.get`.
- Check your database setting at `config/dev.exs` and match your PostgreSQL credential.
- Create and migrate your database with `mix ecto.create && mix ecto.migrate`.
- Install Node.js dependencies with `cd assets && npm install`.
- Add env variables to your environment.
  - `GITHUB_CLIENT_ID` and `GITHUB_CLIENT_SECRET` GitHub Sign-in
  - `TWITTER_CONSUMER_KEY` and `TWITTER_CONSUMER_SECRET` Twitter Sign-in
  - `TWITTER_REDIRECT_URI` Twitter app callback URL (IE: `https://webhook.xrpayments.com/auth/twitter/callback`). This callback URL also needs to be set in your Twitter app configuration.
- Start Phoenix endpoint with `mix phx.server`.

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
