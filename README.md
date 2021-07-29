# phoenix_demo_app


Support code for blog article: https://iacobson.medium.com/phx-gen-auth-and-oauth-for-a-phoenix-liveview-app-a19a27e6befa

## reqirements

* docker
* Erlang/OTP 24
* elixir 

## setup

start the database:

    docker-compose up -d

create the secrets file:

    cp config/dev.secret.exs.template config/dev.secret.exs

Create an Google OAuth Client: https://support.google.com/cloud/answer/6158849?hl=en
and replace "MY CLIENT ID" and "MY CLIENT SECRET" in config/dev.secret.exs.

compile Javascript libraries

    cd assets
    npm install

Setup phenix:
    
    mix deps.get
    mix ecto.migrate

Start server:
    
    iex -S mix phx.server
