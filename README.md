# Theo Clonathon



## Creating the database

This project uses PostgreSQL for the database, the easiest way to get it up and running is by using Docker. Start the database with this command:

```sh
docker compose up -d
```

Create a `.env.local` file in your project folder (parent of src/).

And add the following environment variable:

```sh
DATABASE_URL='postgresql://nextjsuser:nextjspassword@localhost:5432/nextjs-hackathon'
```

If for some reason you want to start the database from scratch you can use the following command (this will erase all the data!):

```sh
docker compose down -v
```