# Turborepo starter

This Turborepo starter is maintained by the Turborepo core team.

```sh
bunx create-turbo@latest
```

start db from docker via:

DATABASE_URL="postgresql://postgres:yourpassword@localhost:5432/mydb?schema=public"

```sh
docker run --name codeforces \
          -e POSTGRES_USER=postgres \
          -e POSTGRES_PASSWORD=postgres \
          -e POSTGRES_DB=mydb \
          -p 5432:5432 \
          -d postgres:16
```
