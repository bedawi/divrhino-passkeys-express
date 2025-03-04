# Divrhino Passkeys Express

This is a fork of the original demo app from Divrhino. This app demonstrates how to implement FIDO2 Passkey authentication in a Node.js web app. The primary change in this fork is the ability to use more authenticators than in the original version. Additionally, this version supports the registration of USB FIDO2 Passkeys.

-   Text tutorial: https://divrhino.com/articles/passkeys-express
-   YouTube tutorial: https://youtu.be/1R68BRM5dyA

# How to get this running fast

## Create Env-File

Create a file named `.env` in the project folder and add the following content:

```
PGHOST=db
PGPORT=5432
PGUSER=passkey-example-db-user
PGPASSWORD=DATABASE_PASSWORD_DROP_HERE
PGDATABASE=passkey-example

SESSION_SECRET=SESSION_SECRET_ADD_HERE
```

## Start docker-containers

```
docker compose up
```

## Create Database Tables

Open a second shell and run this command, while your containers are already up and running:

```
docker compose exec web npx sequelize-cli db:migrate
```
